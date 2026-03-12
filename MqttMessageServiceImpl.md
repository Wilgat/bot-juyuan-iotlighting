/*     */ package com.ruoyi.iotlighting.service.impl;
/*     */ import com.ruoyi.common.exception.ServiceException;
/*     */ import com.ruoyi.common.utils.StringUtils;
/*     */ import com.ruoyi.iotlighting.domain.Diagnosis;
/*     */ import com.ruoyi.iotlighting.domain.IotMessage;
/*     */ import com.ruoyi.iotlighting.domain.TerAlert;
/*     */ import com.ruoyi.iotlighting.domain.TerDataLog;
/*     */ import com.ruoyi.iotlighting.domain.TerInfo;
/*     */ import com.ruoyi.iotlighting.domain.TerSensorStatus;
/*     */ import com.ruoyi.iotlighting.service.ITerSensorStatusService;
/*     */ import java.util.ArrayList;
/*     */ import java.util.Date;
/*     */ import java.util.HashMap;
/*     */ import java.util.List;
/*     */ import java.util.Map;
/*     */ import org.springframework.beans.factory.annotation.Autowired;
/*     */ import org.springframework.transaction.annotation.Transactional;
/*     */ import org.springframework.util.CollectionUtils;
/*     */ import org.springframework.util.ObjectUtils;
/*     */ 
/*     */ @Service
/*     */ public class MqttMessageServiceImpl implements IMqttMessageService {
/*  23 */   private static final Logger log = LoggerFactory.getLogger(MqttMessageServiceImpl.class);
/*     */ 
/*     */   
/*     */   @Autowired
/*     */   private ITerInfoService terInfoService;
/*     */   
/*     */   @Autowired
/*     */   private ITerSensorStatusService terSensorStatusService;
/*     */   
/*     */   @Autowired
/*     */   private ITerDataLogService terDataLogService;
/*     */   
/*     */   @Autowired
/*     */   private ITerAlertService terAlertService;
/*     */   
/*     */   @Autowired
/*     */   private IBuildingPatrolLogService buildingPatrolLogService;
/*     */   
/*     */   @Autowired
/*     */   private ISysConfigService configService;
/*     */   
/*     */   @Autowired
/*     */   private IDiagnosisService diagnosisService;
/*     */   
/*  47 */   private static final Map<String, String> SENSOR_TYPE_MAP = new HashMap<>();
/*  48 */   private static final Map<String, String> SENSOR_TYPE_EXTEND_MAP = new HashMap<>();
/*     */   
/*     */   static {
/*  51 */     SENSOR_TYPE_MAP.put("211", "light");
/*  52 */     SENSOR_TYPE_MAP.put("212", "light");
/*  53 */     SENSOR_TYPE_MAP.put("221", "light");
/*  54 */     SENSOR_TYPE_MAP.put("222", "light");
/*  55 */     SENSOR_TYPE_MAP.put("11", "motion");
/*  56 */     SENSOR_TYPE_MAP.put("12", "speed");
/*  57 */     SENSOR_TYPE_MAP.put("13", "height");
/*  58 */     SENSOR_TYPE_MAP.put("14", "park");
/*  59 */     SENSOR_TYPE_MAP.put("21", "smoke");
/*  60 */     SENSOR_TYPE_MAP.put("22", "h2s");
/*  61 */     SENSOR_TYPE_MAP.put("31", "com");
/*  62 */     SENSOR_TYPE_MAP.put("41", "post");
/*  63 */     SENSOR_TYPE_MAP.put("42", "patrol");
/*  64 */     SENSOR_TYPE_MAP.put("43", "flooding");
/*  65 */     SENSOR_TYPE_EXTEND_MAP.put("43#1", "flooding_1");
/*     */   }
/*     */ 
/*     */   
/*     */   public TerAlert handlSensorData(IotMessage message) {
/*  70 */     if (StringUtils.isEmpty(message.getSn()) || StringUtils.isEmpty(message.getType())) {
/*  71 */       log.error("处理失败，未匹配到灯管数据：{}", JSONObject.toJSONString(message, new com.alibaba.fastjson2.JSONWriter.Feature[0]));
/*  72 */       throw new ServiceException("处理失败，未匹配到灯管数据");
/*     */     } 
/*  74 */     TerSensorStatus oldTerSensorStatus = this.terSensorStatusService.selectTerSensorByType(message.getSn(), message.getType());
/*  75 */     String sn = message.getSn();
/*  76 */     TerInfo terInfo = this.terInfoService.selectTerInfoBySn(sn);
/*     */ 
/*     */     
/*  79 */     if (ObjectUtils.isEmpty(terInfo)) {
/*  80 */       throw new ServiceException("设备未注册，请注册后在发送数据");
/*     */     }
/*     */ 
/*     */     
/*  84 */     message.setGateway(terInfo.getGateway());
/*     */     
/*  86 */     String sensorStatus = genSensorStatus(message);
/*  87 */     TerSensorStatus terSensorStatus = new TerSensorStatus();
/*  88 */     terSensorStatus.setData(message.getData());
/*  89 */     terSensorStatus.setSensorStatus(sensorStatus);
/*  90 */     terSensorStatus.setSensorType(message.getType());
/*  91 */     terSensorStatus.setTerSn(message.getSn());
/*  92 */     terSensorStatus.setUpdatedTime(new Date());
/*  93 */     if (StringUtils.equals("alarm", sensorStatus)) {
/*  94 */       terSensorStatus.setDealFlag("0");
/*     */     }
/*     */ 
/*     */     
/*  98 */     this.terSensorStatusService.updateSertTerSensorStatus(terSensorStatus);
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */     
/* 105 */     boolean alertFlag = false;
/*     */     
/* 107 */     if (StringUtils.equals(message.getType(), "motion")) {
/*     */ 
/*     */ 
/*     */       
/* 111 */       alertFlag = (!ObjectUtils.isEmpty(oldTerSensorStatus) && StringUtils.equals(oldTerSensorStatus.getSensorConfig(), "1") && StringUtils.equals("alarm", sensorStatus));
/* 112 */     } else if (StringUtils.equals(message.getType(), "park")) {
/*     */       
/* 114 */       boolean newParkFlag = (ObjectUtils.isEmpty(oldTerSensorStatus) && StringUtils.equals("alarm", sensorStatus));
/*     */ 
/*     */       
/* 117 */       boolean startParkFlag = (!ObjectUtils.isEmpty(oldTerSensorStatus) && !StringUtils.equals("alarm", oldTerSensorStatus.getSensorStatus()) && StringUtils.equals("alarm", sensorStatus));
/*     */ 
/*     */       
/* 120 */       boolean endParkFlag = (!ObjectUtils.isEmpty(oldTerSensorStatus) && StringUtils.equals("alarm", oldTerSensorStatus.getSensorStatus()) && !StringUtils.equals("alarm", sensorStatus));
/* 121 */       alertFlag = (newParkFlag || startParkFlag || endParkFlag);
/*     */     } else {
/*     */       
/* 124 */       boolean newSensorTypeAlert = (ObjectUtils.isEmpty(oldTerSensorStatus) && StringUtils.equals("alarm", sensorStatus));
/*     */ 
/*     */       
/* 127 */       boolean normalAlertFlag = (!ObjectUtils.isEmpty(oldTerSensorStatus) && !StringUtils.equals("alarm", oldTerSensorStatus.getSensorStatus()) && StringUtils.equals("alarm", sensorStatus));
/* 128 */       alertFlag = (newSensorTypeAlert || normalAlertFlag);
/*     */     } 
/*     */     
/* 131 */     Long alertId = null;
/* 132 */     if (alertFlag) {
/* 133 */       TerAlert terAlert = new TerAlert();
/* 134 */       terAlert.setId(Long.valueOf(IdUtil.getSnowflakeNextId()));
/* 135 */       terAlert.setTerSn(message.getSn());
/* 136 */       terAlert.setCreatedTime(new Date());
/* 137 */       terAlert.setData(message.getData());
/* 138 */       terAlert.setDealFlag("0");
/* 139 */       terAlert.setSensorType(message.getType());
/* 140 */       this.terAlertService.insertTerAlert(terAlert);
/* 141 */       alertId = terAlert.getId();
/*     */     } 
/*     */ 
/*     */     
/* 145 */     String terStatus = genTerStatus(message);
/* 146 */     terInfo.setTerStatus(terStatus);
/* 147 */     terInfo.setUpdatedTime(new Date());
/* 148 */     this.terInfoService.updateTerStatus(terInfo);
/* 149 */     TerDataLog terDataLog = new TerDataLog();
/* 150 */     BeanUtils.copyBeanProp(terDataLog, terSensorStatus);
/* 151 */     terDataLog.setCreatedTime(new Date());
/* 152 */     this.terDataLogService.insertTerDataLog(terDataLog);
/*     */     
/* 154 */     if (alertFlag && !ObjectUtils.isEmpty(alertId)) {
/* 155 */       TerAlert param = new TerAlert();
/* 156 */       param.setId(alertId);
/* 157 */       List<TerAlert> terAlertList = this.terAlertService.selectTerAlertListNotLogin(param);
/* 158 */       if (CollectionUtils.isEmpty(terAlertList)) {
/* 159 */         return null;
/*     */       }
/* 161 */       return terAlertList.get(0);
/*     */     } 
/* 163 */     return null;
/*     */   }
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */   
/*     */   @Transactional
/*     */   public TerInfo handlTerOnline(String sn) {
/* 177 */     TerInfo terInfo = this.terInfoService.selectTerInfoBySn(sn);
/* 178 */     boolean newTerFlag = false;
/*     */     
/* 180 */     if (ObjectUtils.isEmpty(terInfo)) {
/* 181 */       terInfo = buildNewTer(sn);
/* 182 */       newTerFlag = true;
/* 183 */       return null;
/*     */     } 
/* 185 */     terInfo.setUpdatedTime(new Date());
/*     */     
/* 187 */     terInfo.setTerStatus("online");
/* 188 */     if (newTerFlag) {
/* 189 */       this.terInfoService.insertTerInfo(terInfo);
/*     */     } else {
/* 191 */       terInfo.setUpdatedTime(new Date());
/* 192 */       this.terInfoService.updateTerStatus(terInfo);
/*     */     } 
/*     */     
/* 195 */     TerSensorStatus terSensorStatus = new TerSensorStatus();
/* 196 */     terSensorStatus.setTerSn(sn);
/* 197 */     terSensorStatus.setSensorStatus("online");
/* 198 */     terSensorStatus.setUpdatedTime(new Date());
/* 199 */     this.terSensorStatusService.updateTerSensorStatus(terSensorStatus);
/*     */     
/* 201 */     TerDataLog terDataLog = new TerDataLog();
/* 202 */     terDataLog.setTerSn(sn);
/* 203 */     terDataLog.setDelFlag("0");
/* 204 */     terDataLog.setSensorType("connected");
/* 205 */     terDataLog.setCreatedTime(new Date());
/* 206 */     this.terDataLogService.insertTerDataLog(terDataLog);
/*     */     
/* 208 */     if (!newTerFlag) {
/* 209 */       return terInfo;
/*     */     }
/* 211 */     return null;
/*     */   }
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */   
/*     */   public void handlTerOffline(String sn) {
/* 224 */     TerInfo terInfo = this.terInfoService.selectTerInfoBySn(sn);
/* 225 */     boolean newTerFlag = false;
/*     */     
/* 227 */     if (ObjectUtils.isEmpty(terInfo)) {
/*     */       return;
/*     */     }
/*     */ 
/*     */     
/* 232 */     terInfo.setUpdatedTime(new Date());
/*     */     
/* 234 */     terInfo.setTerStatus("offline");
/* 235 */     if (newTerFlag) {
/* 236 */       this.terInfoService.insertTerInfo(terInfo);
/*     */     } else {
/* 238 */       terInfo.setUpdatedTime(new Date());
/* 239 */       this.terInfoService.updateTerStatus(terInfo);
/*     */     } 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */     
/* 249 */     TerDataLog terDataLog = new TerDataLog();
/* 250 */     terDataLog.setTerSn(sn);
/* 251 */     terDataLog.setDelFlag("0");
/* 252 */     terDataLog.setSensorType("disconnected");
/* 253 */     terDataLog.setCreatedTime(new Date());
/* 254 */     this.terDataLogService.insertTerDataLog(terDataLog);
/*     */   }
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */   
/*     */   @Transactional(rollbackFor = {Exception.class})
/*     */   public void handleDiagnosis(IotMessage message) {
/* 268 */     List<String> data = Arrays.asList(message.getData().split(","));
/* 269 */     if (CollectionUtils.isEmpty(data) || data.size() < 4) {
/* 270 */       throw new ServiceException("诊断数据格式异常");
/*     */     }
/*     */     
/* 273 */     Diagnosis diagnosis = new Diagnosis();
/* 274 */     diagnosis.setTerSn(message.getSn());
/* 275 */     diagnosis.setGateway(message.getGateway());
/*     */ 
/*     */     
/* 278 */     String channel = data.get(0);
/* 279 */     String wifiSsid = data.get(1);
/* 280 */     String gatewayRssi = data.get(2);
/* 281 */     diagnosis.setWifiSsid(wifiSsid);
/* 282 */     diagnosis.setGatewayRssi(gatewayRssi);
/*     */     
/* 284 */     if (StringUtils.length(channel) == 1) {
/* 285 */       channel = "0" + channel;
/*     */     }
/* 287 */     diagnosis.setChannel(channel);
/* 288 */     diagnosis.setGatewayOnlineStatus("1");
/* 289 */     diagnosis.setGatewayDiagnosisUpdateTime(new Date());
/* 290 */     this.diagnosisService.updateGatewayStatus(diagnosis);
/*     */ 
/*     */     
/* 293 */     String terOnlineStatus = data.get(3);
/* 294 */     diagnosis.setTerOnlineStatus(terOnlineStatus);
/*     */     
/* 296 */     if (StringUtils.isNotEmpty(terOnlineStatus) && StringUtils.equals(terOnlineStatus, "0")) {
/* 297 */       this.diagnosisService.updateTerStatusOffline(diagnosis);
/*     */       return;
/*     */     } 
/* 300 */     String terRssi = data.get(4);
/* 301 */     String hopCount = data.get(5);
/* 302 */     if (StringUtils.length(hopCount) == 1) {
/* 303 */       hopCount = "0" + hopCount;
/*     */     }
/* 305 */     diagnosis.setTerRssi(terRssi);
/* 306 */     diagnosis.setHopCount(hopCount);
/* 307 */     diagnosis.setTerDiagnosisUpdateTime(new Date());
/* 308 */     this.diagnosisService.updateTerStatus(diagnosis);
/*     */ 
/*     */     
/* 311 */     List<String> sensorTypeList = new ArrayList<>();
/* 312 */     List<String> sensorTypeExtendList = new ArrayList<>();
/* 313 */     for (int i = 6; i < data.size(); i++) {
/* 314 */       if (SENSOR_TYPE_MAP.containsKey(data.get(i))) {
/* 315 */         sensorTypeList.add(SENSOR_TYPE_MAP.get(data.get(i)));
/*     */       }
/*     */       
/* 318 */       if (SENSOR_TYPE_EXTEND_MAP.containsKey(data.get(i))) {
/* 319 */         sensorTypeExtendList.add(SENSOR_TYPE_EXTEND_MAP.get(data.get(i)));
/*     */       }
/*     */     } 
/*     */     
/* 323 */     sensorTypeList.add("light");
/* 324 */     sensorTypeList.add("com");
/* 325 */     this.diagnosisService.updateSensorStatus(message.getSn(), sensorTypeList);
/*     */ 
/*     */     
/* 328 */     this.diagnosisService.updateSensorExtendStatus(message.getSn(), sensorTypeExtendList);
/*     */   }
/*     */ 
/*     */   
/*     */   private TerInfo buildNewTer(String sn) {
/* 333 */     TerInfo terInfo = new TerInfo();
/* 334 */     terInfo.setSn(sn);
/* 335 */     terInfo.setCreatedTime(new Date());
/* 336 */     terInfo.setUpdatedTime(new Date());
/* 337 */     terInfo.setDelFlag("0");
/* 338 */     return terInfo;
/*     */   }
/*     */   
/*     */   private String genTerStatus(IotMessage message) {
/* 342 */     List<TerSensorStatus> terSensorStatusList = this.terSensorStatusService.selectTerSensorStatusByTerSn(message.getSn());
/* 343 */     terSensorStatusList = (List<TerSensorStatus>)terSensorStatusList.stream().filter(terSensorStatus -> StringUtils.equalsIgnoreCase(terSensorStatus.getSensorStatus(), "alarm")).collect(Collectors.toList());
/* 344 */     if (CollectionUtils.isEmpty(terSensorStatusList))
/*     */     {
/* 346 */       return "online";
/*     */     }
/* 348 */     return "alarm";
/*     */   }
/*     */   
/*     */   private String genSensorStatus(IotMessage message) {
/* 352 */     String type = message.getType();
/* 353 */     String data = message.getData();
/* 354 */     if (StringUtils.equals("park", type) && 
/* 355 */       !StringUtils.equalsIgnoreCase("0", data) && 
/* 356 */       !StringUtils.equalsIgnoreCase("1", data)) {
/* 357 */       throw new ServiceException("发送数据不合法，处理失败");
/*     */     }
/* 359 */     message.setData(data);
/* 360 */     String status = "online";
/*     */     
/* 362 */     if (StringUtils.equalsIgnoreCase("post", type) && 
/* 363 */       StringUtils.isNotEmpty(data) && !StringUtils.equalsIgnoreCase("0", data)) {
/* 364 */       status = "alarm";
/* 365 */     } else if (StringUtils.equalsIgnoreCase("patrol", type)) {
/*     */       
/* 367 */       if (!StringUtils.equalsIgnoreCase("0", data)) {
/* 368 */         this.buildingPatrolLogService.handlePatrolDetailData(message.getGateway(), message.getSn());
/*     */       }
/* 370 */     } else if (StringUtils.equalsIgnoreCase("speed", type)) {
/*     */       
/* 372 */       if (!StringUtils.equalsIgnoreCase("0", data)) {
/* 373 */         status = "alarm";
/*     */         try {
/* 375 */           if (!StringUtils.equalsIgnoreCase("1", data)) {
/* 376 */             String speedMacList = this.configService.selectConfigByKey("speed.mac.list");
/* 377 */             data = extractAndConvertBinaryParts(data, speedMacList);
/* 378 */             message.setData(data);
/*     */           } 
/* 380 */         } catch (Exception e) {
/* 381 */           log.error("解析data数据错误", e);
/*     */         }
/*     */       
/*     */       } 
/* 385 */     } else if (StringUtils.equalsIgnoreCase("1", data)) {
/* 386 */       status = "alarm";
/*     */     } 
/*     */     
/* 389 */     return status;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public static String extractAndConvertBinaryParts(String data, String speedMacList) {
/* 395 */     String binaryString = Integer.toBinaryString(Integer.parseInt(data));
/*     */ 
/*     */     
/* 398 */     while (binaryString.length() < 16) {
/* 399 */       binaryString = "0" + binaryString;
/*     */     }
/*     */ 
/*     */     
/* 403 */     String firstEight = binaryString.substring(0, 8);
/* 404 */     String lastEight = binaryString.substring(8, 16);
/*     */ 
/*     */     
/* 407 */     int firstPartDecimal = Integer.parseInt(firstEight, 2);
/* 408 */     int lastPartDecimal = Integer.parseInt(lastEight, 2);
/*     */ 
/*     */     
/* 411 */     String[] macList = speedMacList.split(",");
/*     */     
/* 413 */     return macList[firstPartDecimal - 1].trim() + "," + lastPartDecimal;
/*     */   }
/*     */ }


/* Location:              /juyuan-iotlighting-3.8.6/!/com/ruoyi/iotlighting/service/impl/MqttMessageServiceImpl.class
 * Java compiler version: 8 (52.0)
 * JD-Core Version:       1.1.3
 */