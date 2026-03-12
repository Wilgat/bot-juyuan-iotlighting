/*     */ package com.ruoyi.iotlighting.domain;
/*     */ public class TerInfo extends BaseEntity { private static final long serialVersionUID = 1L; @JsonSerialize(using = ToStringSerializer.class)
/*     */   private Long id; @JsonFormat(pattern = "yyyy-MM-dd HH:mm:ss")
/*     */   @Excel(name = "安装日期", dateFormat = "yyyy-MM-dd")
/*     */   private Date createdTime; @Excel(name = "大厦名称")
/*     */   private String buildingName; @Excel(name = "座")
/*     */   private String block; @Excel(name = "楼层")
/*     */   private String floorName; @Excel(name = "区域")
/*     */   private String zone; @Excel(name = "区域(分类)")
/*     */   private String zoneSub; @Excel(name = "确实位置")
/*     */   private String pointName; @Excel(name = "LED", dictType = "ter_module_type")
/*     */   private String led;
/*     */   @Excel(name = "灯管插口1", dictType = "ter_module_type")
/*     */   private String module1;
/*     */   @Excel(name = "灯管插口2", dictType = "ter_module_type")
/*     */   private String module2;
/*     */   @Excel(name = "灯管插口3", dictType = "ter_module_type")
/*     */   private String module3;
/*     */   @Excel(name = "灯管插口4", dictType = "ter_module_type")
/*     */   private String module4;
/*     */   private String sn;
/*     */   private String upc;
/*     */   private String terStatus;
/*     */   
/*  25 */   public void setId(Long id) { this.id = id; } private String createdBy; private String updatedBy; @JsonFormat(pattern = "yyyy-MM-dd HH:mm:ss") private Date updatedTime; private String delFlag; private Long deptId; @JsonSerialize(using = ToStringSerializer.class) private Long buildingId; @JsonSerialize(using = ToStringSerializer.class) private Long floorId; @JsonSerialize(using = ToStringSerializer.class) private Long pointId; private Integer pointX; private Integer pointY; private String linkageStatus; private String gateway; private String gatewayName; private String licenseNumberOne; private String licenseNumberTwo; private String licenseNumberThree; private List<TerSensorStatus> terSensorStatusList; @JsonFormat(pattern = "yyyy-MM-dd HH:mm:ss") public void setCreatedTime(Date createdTime) { this.createdTime = createdTime; } public void setBuildingName(String buildingName) { this.buildingName = buildingName; } public void setBlock(String block) { this.block = block; } public void setFloorName(String floorName) { this.floorName = floorName; } public void setZone(String zone) { this.zone = zone; } public void setZoneSub(String zoneSub) { this.zoneSub = zoneSub; } public void setPointName(String pointName) { this.pointName = pointName; } public void setLed(String led) { this.led = led; } public void setModule1(String module1) { this.module1 = module1; } public void setModule2(String module2) { this.module2 = module2; } public void setModule3(String module3) { this.module3 = module3; } public void setModule4(String module4) { this.module4 = module4; } public void setSn(String sn) { this.sn = sn; } public void setUpc(String upc) { this.upc = upc; } public void setTerStatus(String terStatus) { this.terStatus = terStatus; } public void setCreatedBy(String createdBy) { this.createdBy = createdBy; } public void setUpdatedBy(String updatedBy) { this.updatedBy = updatedBy; } @JsonFormat(pattern = "yyyy-MM-dd HH:mm:ss") public void setUpdatedTime(Date updatedTime) { this.updatedTime = updatedTime; } public void setDelFlag(String delFlag) { this.delFlag = delFlag; } public void setDeptId(Long deptId) { this.deptId = deptId; } public void setBuildingId(Long buildingId) { this.buildingId = buildingId; } public void setFloorId(Long floorId) { this.floorId = floorId; } public void setPointId(Long pointId) { this.pointId = pointId; } public void setPointX(Integer pointX) { this.pointX = pointX; } public void setPointY(Integer pointY) { this.pointY = pointY; } public void setLinkageStatus(String linkageStatus) { this.linkageStatus = linkageStatus; } public void setGateway(String gateway) { this.gateway = gateway; } public void setGatewayName(String gatewayName) { this.gatewayName = gatewayName; } public void setLicenseNumberOne(String licenseNumberOne) { this.licenseNumberOne = licenseNumberOne; } public void setLicenseNumberTwo(String licenseNumberTwo) { this.licenseNumberTwo = licenseNumberTwo; } public void setLicenseNumberThree(String licenseNumberThree) { this.licenseNumberThree = licenseNumberThree; } public void setTerSensorStatusList(List<TerSensorStatus> terSensorStatusList) { this.terSensorStatusList = terSensorStatusList; } public boolean equals(Object o) { if (o == this) return true;  if (!(o instanceof TerInfo)) return false;  TerInfo other = (TerInfo)o; if (!other.canEqual(this)) return false;  Object this$id = getId(), other$id = other.getId(); if ((this$id == null) ? (other$id != null) : !this$id.equals(other$id)) return false;  Object this$deptId = getDeptId(), other$deptId = other.getDeptId(); if ((this$deptId == null) ? (other$deptId != null) : !this$deptId.equals(other$deptId)) return false;  Object this$buildingId = getBuildingId(), other$buildingId = other.getBuildingId(); if ((this$buildingId == null) ? (other$buildingId != null) : !this$buildingId.equals(other$buildingId)) return false;  Object this$floorId = getFloorId(), other$floorId = other.getFloorId(); if ((this$floorId == null) ? (other$floorId != null) : !this$floorId.equals(other$floorId)) return false;  Object this$pointId = getPointId(), other$pointId = other.getPointId(); if ((this$pointId == null) ? (other$pointId != null) : !this$pointId.equals(other$pointId)) return false;  Object this$pointX = getPointX(), other$pointX = other.getPointX(); if ((this$pointX == null) ? (other$pointX != null) : !this$pointX.equals(other$pointX)) return false;  Object this$pointY = getPointY(), other$pointY = other.getPointY(); if ((this$pointY == null) ? (other$pointY != null) : !this$pointY.equals(other$pointY)) return false;  Object this$createdTime = getCreatedTime(), other$createdTime = other.getCreatedTime(); if ((this$createdTime == null) ? (other$createdTime != null) : !this$createdTime.equals(other$createdTime)) return false;  Object this$buildingName = getBuildingName(), other$buildingName = other.getBuildingName(); if ((this$buildingName == null) ? (other$buildingName != null) : !this$buildingName.equals(other$buildingName)) return false;  Object this$block = getBlock(), other$block = other.getBlock(); if ((this$block == null) ? (other$block != null) : !this$block.equals(other$block)) return false;  Object this$floorName = getFloorName(), other$floorName = other.getFloorName(); if ((this$floorName == null) ? (other$floorName != null) : !this$floorName.equals(other$floorName)) return false;  Object this$zone = getZone(), other$zone = other.getZone(); if ((this$zone == null) ? (other$zone != null) : !this$zone.equals(other$zone)) return false;  Object this$zoneSub = getZoneSub(), other$zoneSub = other.getZoneSub(); if ((this$zoneSub == null) ? (other$zoneSub != null) : !this$zoneSub.equals(other$zoneSub)) return false;  Object this$pointName = getPointName(), other$pointName = other.getPointName(); if ((this$pointName == null) ? (other$pointName != null) : !this$pointName.equals(other$pointName)) return false;  Object this$led = getLed(), other$led = other.getLed(); if ((this$led == null) ? (other$led != null) : !this$led.equals(other$led)) return false;  Object this$module1 = getModule1(), other$module1 = other.getModule1(); if ((this$module1 == null) ? (other$module1 != null) : !this$module1.equals(other$module1)) return false;  Object this$module2 = getModule2(), other$module2 = other.getModule2(); if ((this$module2 == null) ? (other$module2 != null) : !this$module2.equals(other$module2)) return false;  Object this$module3 = getModule3(), other$module3 = other.getModule3(); if ((this$module3 == null) ? (other$module3 != null) : !this$module3.equals(other$module3)) return false;  Object this$module4 = getModule4(), other$module4 = other.getModule4(); if ((this$module4 == null) ? (other$module4 != null) : !this$module4.equals(other$module4)) return false;  Object this$sn = getSn(), other$sn = other.getSn(); if ((this$sn == null) ? (other$sn != null) : !this$sn.equals(other$sn)) return false;  Object this$upc = getUpc(), other$upc = other.getUpc(); if ((this$upc == null) ? (other$upc != null) : !this$upc.equals(other$upc)) return false;  Object this$terStatus = getTerStatus(), other$terStatus = other.getTerStatus(); if ((this$terStatus == null) ? (other$terStatus != null) : !this$terStatus.equals(other$terStatus)) return false;  Object this$createdBy = getCreatedBy(), other$createdBy = other.getCreatedBy(); if ((this$createdBy == null) ? (other$createdBy != null) : !this$createdBy.equals(other$createdBy)) return false;  Object this$updatedBy = getUpdatedBy(), other$updatedBy = other.getUpdatedBy(); if ((this$updatedBy == null) ? (other$updatedBy != null) : !this$updatedBy.equals(other$updatedBy)) return false;  Object this$updatedTime = getUpdatedTime(), other$updatedTime = other.getUpdatedTime(); if ((this$updatedTime == null) ? (other$updatedTime != null) : !this$updatedTime.equals(other$updatedTime)) return false;  Object this$delFlag = getDelFlag(), other$delFlag = other.getDelFlag(); if ((this$delFlag == null) ? (other$delFlag != null) : !this$delFlag.equals(other$delFlag)) return false;  Object this$linkageStatus = getLinkageStatus(), other$linkageStatus = other.getLinkageStatus(); if ((this$linkageStatus == null) ? (other$linkageStatus != null) : !this$linkageStatus.equals(other$linkageStatus)) return false;  Object this$gateway = getGateway(), other$gateway = other.getGateway(); if ((this$gateway == null) ? (other$gateway != null) : !this$gateway.equals(other$gateway)) return false;  Object this$gatewayName = getGatewayName(), other$gatewayName = other.getGatewayName(); if ((this$gatewayName == null) ? (other$gatewayName != null) : !this$gatewayName.equals(other$gatewayName)) return false;  Object this$licenseNumberOne = getLicenseNumberOne(), other$licenseNumberOne = other.getLicenseNumberOne(); if ((this$licenseNumberOne == null) ? (other$licenseNumberOne != null) : !this$licenseNumberOne.equals(other$licenseNumberOne)) return false;  Object this$licenseNumberTwo = getLicenseNumberTwo(), other$licenseNumberTwo = other.getLicenseNumberTwo(); if ((this$licenseNumberTwo == null) ? (other$licenseNumberTwo != null) : !this$licenseNumberTwo.equals(other$licenseNumberTwo)) return false;  Object this$licenseNumberThree = getLicenseNumberThree(), other$licenseNumberThree = other.getLicenseNumberThree(); if ((this$licenseNumberThree == null) ? (other$licenseNumberThree != null) : !this$licenseNumberThree.equals(other$licenseNumberThree)) return false;  Object<TerSensorStatus> this$terSensorStatusList = (Object<TerSensorStatus>)getTerSensorStatusList(), other$terSensorStatusList = (Object<TerSensorStatus>)other.getTerSensorStatusList(); return !((this$terSensorStatusList == null) ? (other$terSensorStatusList != null) : !this$terSensorStatusList.equals(other$terSensorStatusList)); } protected boolean canEqual(Object other) { return other instanceof TerInfo; } public int hashCode() { int PRIME = 59; result = 1; Object $id = getId(); result = result * 59 + (($id == null) ? 43 : $id.hashCode()); Object $deptId = getDeptId(); result = result * 59 + (($deptId == null) ? 43 : $deptId.hashCode()); Object $buildingId = getBuildingId(); result = result * 59 + (($buildingId == null) ? 43 : $buildingId.hashCode()); Object $floorId = getFloorId(); result = result * 59 + (($floorId == null) ? 43 : $floorId.hashCode()); Object $pointId = getPointId(); result = result * 59 + (($pointId == null) ? 43 : $pointId.hashCode()); Object $pointX = getPointX(); result = result * 59 + (($pointX == null) ? 43 : $pointX.hashCode()); Object $pointY = getPointY(); result = result * 59 + (($pointY == null) ? 43 : $pointY.hashCode()); Object $createdTime = getCreatedTime(); result = result * 59 + (($createdTime == null) ? 43 : $createdTime.hashCode()); Object $buildingName = getBuildingName(); result = result * 59 + (($buildingName == null) ? 43 : $buildingName.hashCode()); Object $block = getBlock(); result = result * 59 + (($block == null) ? 43 : $block.hashCode()); Object $floorName = getFloorName(); result = result * 59 + (($floorName == null) ? 43 : $floorName.hashCode()); Object $zone = getZone(); result = result * 59 + (($zone == null) ? 43 : $zone.hashCode()); Object $zoneSub = getZoneSub(); result = result * 59 + (($zoneSub == null) ? 43 : $zoneSub.hashCode()); Object $pointName = getPointName(); result = result * 59 + (($pointName == null) ? 43 : $pointName.hashCode()); Object $led = getLed(); result = result * 59 + (($led == null) ? 43 : $led.hashCode()); Object $module1 = getModule1(); result = result * 59 + (($module1 == null) ? 43 : $module1.hashCode()); Object $module2 = getModule2(); result = result * 59 + (($module2 == null) ? 43 : $module2.hashCode()); Object $module3 = getModule3(); result = result * 59 + (($module3 == null) ? 43 : $module3.hashCode()); Object $module4 = getModule4(); result = result * 59 + (($module4 == null) ? 43 : $module4.hashCode()); Object $sn = getSn(); result = result * 59 + (($sn == null) ? 43 : $sn.hashCode()); Object $upc = getUpc(); result = result * 59 + (($upc == null) ? 43 : $upc.hashCode()); Object $terStatus = getTerStatus(); result = result * 59 + (($terStatus == null) ? 43 : $terStatus.hashCode()); Object $createdBy = getCreatedBy(); result = result * 59 + (($createdBy == null) ? 43 : $createdBy.hashCode()); Object $updatedBy = getUpdatedBy(); result = result * 59 + (($updatedBy == null) ? 43 : $updatedBy.hashCode()); Object $updatedTime = getUpdatedTime(); result = result * 59 + (($updatedTime == null) ? 43 : $updatedTime.hashCode()); Object $delFlag = getDelFlag(); result = result * 59 + (($delFlag == null) ? 43 : $delFlag.hashCode()); Object $linkageStatus = getLinkageStatus(); result = result * 59 + (($linkageStatus == null) ? 43 : $linkageStatus.hashCode()); Object $gateway = getGateway(); result = result * 59 + (($gateway == null) ? 43 : $gateway.hashCode()); Object $gatewayName = getGatewayName(); result = result * 59 + (($gatewayName == null) ? 43 : $gatewayName.hashCode()); Object $licenseNumberOne = getLicenseNumberOne(); result = result * 59 + (($licenseNumberOne == null) ? 43 : $licenseNumberOne.hashCode()); Object $licenseNumberTwo = getLicenseNumberTwo(); result = result * 59 + (($licenseNumberTwo == null) ? 43 : $licenseNumberTwo.hashCode()); Object $licenseNumberThree = getLicenseNumberThree(); result = result * 59 + (($licenseNumberThree == null) ? 43 : $licenseNumberThree.hashCode()); Object<TerSensorStatus> $terSensorStatusList = (Object<TerSensorStatus>)getTerSensorStatusList(); return result * 59 + (($terSensorStatusList == null) ? 43 : $terSensorStatusList.hashCode()); } public String toString() { return "TerInfo(id=" + getId() + ", createdTime=" + getCreatedTime() + ", buildingName=" + getBuildingName() + ", block=" + getBlock() + ", floorName=" + getFloorName() + ", zone=" + getZone() + ", zoneSub=" + getZoneSub() + ", pointName=" + getPointName() + ", led=" + getLed() + ", module1=" + getModule1() + ", module2=" + getModule2() + ", module3=" + getModule3() + ", module4=" + getModule4() + ", sn=" + getSn() + ", upc=" + getUpc() + ", terStatus=" + getTerStatus() + ", createdBy=" + getCreatedBy() + ", updatedBy=" + getUpdatedBy() + ", updatedTime=" + getUpdatedTime() + ", delFlag=" + getDelFlag() + ", deptId=" + getDeptId() + ", buildingId=" + getBuildingId() + ", floorId=" + getFloorId() + ", pointId=" + getPointId() + ", pointX=" + getPointX() + ", pointY=" + getPointY() + ", linkageStatus=" + getLinkageStatus() + ", gateway=" + getGateway() + ", gatewayName=" + getGatewayName() + ", licenseNumberOne=" + getLicenseNumberOne() + ", licenseNumberTwo=" + getLicenseNumberTwo() + ", licenseNumberThree=" + getLicenseNumberThree() + ", terSensorStatusList=" + getTerSensorStatusList() + ")"; }
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */   
/*     */   public Long getId() {
/*  33 */     return this.id;
/*     */   }
/*     */ 
/*     */ 
/*     */ 
/*     */   
/*     */   public Date getCreatedTime() {
/*  40 */     return this.createdTime;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getBuildingName() {
/*  46 */     return this.buildingName;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getBlock() {
/*  52 */     return this.block;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getFloorName() {
/*  58 */     return this.floorName;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getZone() {
/*  64 */     return this.zone;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getZoneSub() {
/*  70 */     return this.zoneSub;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getPointName() {
/*  76 */     return this.pointName;
/*     */   }
/*     */   public String getLed() {
/*  79 */     return this.led;
/*     */   }
/*     */   public String getModule1() {
/*  82 */     return this.module1;
/*     */   }
/*     */   public String getModule2() {
/*  85 */     return this.module2;
/*     */   }
/*     */   public String getModule3() {
/*  88 */     return this.module3;
/*     */   }
/*     */   public String getModule4() {
/*  91 */     return this.module4;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getSn() {
/*  96 */     return this.sn;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getUpc() {
/* 101 */     return this.upc;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getTerStatus() {
/* 106 */     return this.terStatus;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getCreatedBy() {
/* 112 */     return this.createdBy;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getUpdatedBy() {
/* 118 */     return this.updatedBy;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Date getUpdatedTime() {
/* 124 */     return this.updatedTime;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getDelFlag() {
/* 129 */     return this.delFlag;
/*     */   }
/*     */ 
/*     */   
/*     */   public Long getDeptId() {
/* 134 */     return this.deptId;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Long getBuildingId() {
/* 140 */     return this.buildingId;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Long getFloorId() {
/* 146 */     return this.floorId;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Long getPointId() {
/* 152 */     return this.pointId;
/*     */   }
/*     */ 
/*     */   
/*     */   public Integer getPointX() {
/* 157 */     return this.pointX;
/*     */   }
/*     */ 
/*     */   
/*     */   public Integer getPointY() {
/* 162 */     return this.pointY;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getLinkageStatus() {
/* 167 */     return this.linkageStatus;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getGateway() {
/* 172 */     return this.gateway;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getGatewayName() {
/* 177 */     return this.gatewayName;
/*     */   }
/* 179 */   public String getLicenseNumberOne() { return this.licenseNumberOne; }
/* 180 */   public String getLicenseNumberTwo() { return this.licenseNumberTwo; } public String getLicenseNumberThree() {
/* 181 */     return this.licenseNumberThree;
/*     */   }
/*     */ 
/*     */   
/*     */   public List<TerSensorStatus> getTerSensorStatusList() {
/* 186 */     return this.terSensorStatusList;
/*     */   }
/*     */   
/*     */   public String buildingPayload() {
/* 190 */     String payload = "";
/* 191 */     if (!ObjectUtils.isEmpty(getPointY())) {
/* 192 */       payload = payload + "bind," + getPointX() + "," + getPointY() + "," + getFloorId() + "," + getBuildingId();
/*     */     } else {
/*     */       
/* 195 */       payload = payload + "unbind";
/*     */     } 
/* 197 */     List<TerSensorStatus> terSensorStatusList = getTerSensorStatusList();
/* 198 */     String ledCode = getLedCodeFromUpc(getUpc());
/* 199 */     List<String> terSensorStatusArray = new ArrayList<>();
/* 200 */     List<String> lightConfigArray = new ArrayList<>();
/* 201 */     lightConfigArray.add(ledCode);
/* 202 */     for (TerSensorStatus terSensorStatus : terSensorStatusList) {
/* 203 */       String sensorType = terSensorStatus.getSensorType();
/* 204 */       String sensorConfig = terSensorStatus.getSensorConfig();
/*     */ 
/*     */       
/* 207 */       if (StringUtils.isEmpty(sensorConfig)) {
/*     */         continue;
/*     */       }
/*     */ 
/*     */       
/* 212 */       if (StringUtils.equals(sensorType, "light")) {
/* 213 */         JSONObject jsonObject = JSON.parseObject(sensorConfig);
/* 214 */         if (StringUtils.equals(jsonObject.getString("mode"), "2")) {
/* 215 */           lightConfigArray.add("00:00");
/* 216 */           lightConfigArray.add("00:00");
/* 217 */           lightConfigArray.add(jsonObject.getJSONObject("auto").getString("lux"));
/* 218 */           lightConfigArray.add(jsonObject.getJSONObject("auto").getString("wait"));
/* 219 */           lightConfigArray.add(jsonObject.getJSONObject("auto").getString("high"));
/*     */           
/* 221 */           lightConfigArray.add("00:00");
/* 222 */           lightConfigArray.add("00:00");
/* 223 */           lightConfigArray.add("60");
/* 224 */           lightConfigArray.add("60");
/* 225 */           lightConfigArray.add("60"); continue;
/*     */         } 
/* 227 */         lightConfigArray.add(jsonObject.getJSONObject("day").getString("start"));
/* 228 */         lightConfigArray.add(jsonObject.getJSONObject("day").getString("end"));
/* 229 */         lightConfigArray.add(jsonObject.getJSONObject("day").getString("high"));
/* 230 */         lightConfigArray.add(jsonObject.getJSONObject("day").getString("wait"));
/* 231 */         lightConfigArray.add(jsonObject.getJSONObject("day").getString("low"));
/*     */         
/* 233 */         lightConfigArray.add(jsonObject.getJSONObject("night").getString("start"));
/* 234 */         lightConfigArray.add(jsonObject.getJSONObject("night").getString("end"));
/* 235 */         lightConfigArray.add(jsonObject.getJSONObject("night").getString("high"));
/* 236 */         lightConfigArray.add(jsonObject.getJSONObject("night").getString("wait"));
/* 237 */         lightConfigArray.add(jsonObject.getJSONObject("night").getString("low"));
/*     */         
/*     */         continue;
/*     */       } 
/* 241 */       if (StringUtils.equals(sensorType, "post")) {
/* 242 */         terSensorStatusArray.add(sensorType);
/* 243 */         terSensorStatusArray.add(sensorConfig);
/* 244 */         terSensorStatusArray.add(StringUtils.isEmpty(this.licenseNumberOne) ? "0" : this.licenseNumberOne);
/* 245 */         terSensorStatusArray.add(StringUtils.isEmpty(this.licenseNumberTwo) ? "0" : this.licenseNumberTwo);
/* 246 */         terSensorStatusArray.add(StringUtils.isEmpty(this.licenseNumberThree) ? "0" : this.licenseNumberThree); continue;
/* 247 */       }  if (StringUtils.equals(sensorType, "smoke") || StringUtils.equals(sensorType, "h2s")) {
/* 248 */         String[] sensorConfigArray = sensorConfig.split(",");
/* 249 */         int time = 0;
/* 250 */         int percent = 30;
/* 251 */         if (sensorConfigArray.length == 1) {
/* 252 */           percent = Integer.parseInt(sensorConfigArray[0]);
/* 253 */         } else if (sensorConfigArray.length == 2) {
/* 254 */           time = Integer.parseInt(sensorConfigArray[0]);
/* 255 */           percent = Integer.parseInt(sensorConfigArray[1]);
/*     */         } 
/*     */         
/* 258 */         String timeBinary = Integer.toBinaryString(time);
/*     */         
/* 260 */         while (timeBinary.length() < 8) {
/* 261 */           timeBinary = "0" + timeBinary;
/*     */         }
/* 263 */         String percentBinary = Integer.toBinaryString(percent);
/* 264 */         while (percentBinary.length() < 8) {
/* 265 */           percentBinary = "0" + percentBinary;
/*     */         }
/*     */         
/* 268 */         sensorConfig = String.valueOf(Integer.parseInt(timeBinary + percentBinary, 2));
/* 269 */         terSensorStatusArray.add(sensorType);
/* 270 */         terSensorStatusArray.add(sensorConfig); continue;
/* 271 */       }  if (StringUtils.equals(sensorType, "flooding")) {
/* 272 */         if (StringUtils.isEmpty(sensorConfig)) {
/* 273 */           sensorConfig = "0";
/*     */         }
/* 275 */         terSensorStatusArray.add(sensorType);
/* 276 */         String[] sensorConfigArray = sensorConfig.split(",");
/* 277 */         if (sensorConfigArray.length == 2 && StringUtils.equals(sensorConfigArray[1], "0")) {
/* 278 */           terSensorStatusArray.add("0"); continue;
/*     */         } 
/* 280 */         terSensorStatusArray.add(sensorConfigArray[0]); continue;
/*     */       } 
/* 282 */       if (StringUtils.equals(sensorType, "park") || StringUtils.equals(sensorType, "height")) {
/* 283 */         terSensorStatusArray.add(sensorType);
/* 284 */         String[] sensorConfigArray = sensorConfig.split(",");
/* 285 */         if (sensorConfigArray.length == 2) {
/* 286 */           terSensorStatusArray.add(sensorConfig); continue;
/* 287 */         }  if (sensorConfigArray.length == 3) {
/* 288 */           int config = 536 - Integer.parseInt(sensorConfigArray[2]) + Integer.parseInt(sensorConfigArray[0]);
/* 289 */           config = Math.max(config, 0);
/* 290 */           terSensorStatusArray.add(config + "," + sensorConfigArray[1]);
/*     */         }  continue;
/*     */       } 
/* 293 */       terSensorStatusArray.add(sensorType);
/* 294 */       terSensorStatusArray.add(sensorConfig);
/*     */     } 
/*     */ 
/*     */     
/* 298 */     terSensorStatusArray.addAll(lightConfigArray);
/* 299 */     payload = payload + "," + StringUtils.join(terSensorStatusArray, ",");
/* 300 */     return payload;
/*     */   }
/*     */   
/*     */   private String getLedCodeFromUpc(String upc) {
/* 304 */     String ledCode = (upc.length() > 16) ? upc.substring(2, 5) : upc.substring(0, 3);
/* 305 */     return ledCode;
/*     */   }
/*     */ 
/*     */   
/*     */   public static void main(String[] args) {
/* 310 */     String sensorConfig = "30";
/* 311 */     String[] sensorConfigArray = sensorConfig.split(",");
/* 312 */     int time = 0;
/* 313 */     int percent = 30;
/* 314 */     if (sensorConfigArray.length == 1) {
/* 315 */       percent = Integer.parseInt(sensorConfigArray[0]);
/* 316 */     } else if (sensorConfigArray.length == 2) {
/* 317 */       time = Integer.parseInt(sensorConfigArray[0]);
/* 318 */       percent = Integer.parseInt(sensorConfigArray[1]);
/*     */     } 
/*     */     
/* 321 */     String timeBinary = Integer.toBinaryString(time);
/*     */     
/* 323 */     while (timeBinary.length() < 8) {
/* 324 */       timeBinary = "0" + timeBinary;
/*     */     }
/* 326 */     String percentBinary = Integer.toBinaryString(percent);
/* 327 */     while (percentBinary.length() < 8) {
/* 328 */       percentBinary = "0" + percentBinary;
/*     */     }
/*     */     
/* 331 */     sensorConfig = String.valueOf(Integer.parseInt(timeBinary + percentBinary, 2));
/* 332 */     System.out.println(sensorConfig);
/*     */   } }


/* Location:              /juyuan-iotlighting-3.8.6/!/com/ruoyi/iotlighting/domain/TerInfo.class
 * Java compiler version: 8 (52.0)
 * JD-Core Version:       1.1.3
 */