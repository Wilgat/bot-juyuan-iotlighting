/*    */ package com.ruoyi.iotlighting.task;
/*    */ import cn.hutool.core.date.DateTime;
/*    */ import cn.hutool.core.date.DateUnit;
/*    */ import cn.hutool.core.date.DateUtil;
/*    */ import com.ruoyi.iotlighting.mapper.TerSensorStatusMapper;
/*    */ import com.ruoyi.system.service.ISysConfigService;
/*    */ import com.ruoyi.system.service.ISysEmailService;
/*    */ import java.util.Date;
/*    */ import org.apache.commons.io.FileUtils;
/*    */ import org.slf4j.Logger;
/*    */ import org.slf4j.LoggerFactory;
/*    */ import org.springframework.beans.factory.annotation.Autowired;
/*    */ import org.springframework.stereotype.Component;
/*    */ 
/*    */ @Component("monitorTask")
/*    */ public class MonitorTast {
/* 17 */   private static final Logger log = LoggerFactory.getLogger(MonitorTast.class);
/*    */ 
/*    */   
/*    */   @Autowired
/*    */   private ISysEmailService sysEmailService;
/*    */ 
/*    */   
/*    */   @Autowired
/*    */   private TerSensorStatusMapper terSensorStatusMapper;
/*    */   
/*    */   @Autowired
/*    */   private ISysConfigService sysConfigService;
/*    */ 
/*    */   
/*    */   public void monitorIosPackage() {
/* 32 */     String dateConfig = this.sysConfigService.selectConfigByKey("ios.package.date");
/*    */     
/* 34 */     String expiredConfig = this.sysConfigService.selectConfigByKey("ios.package.expired");
/*    */     
/* 36 */     DateTime dateTime = DateUtil.offsetDay((Date)DateUtil.parse(dateConfig), 90);
/*    */     
/* 38 */     if (DateUtil.between((Date)dateTime, new Date(), DateUnit.DAY) <= Integer.parseInt(expiredConfig)) {
/*    */       
/* 40 */       String emailConfig = this.sysConfigService.selectConfigByKey("email.alert.address");
/* 41 */       String[] emailArray = emailConfig.split(",");
/* 42 */       String text = "【Dr.sense】ios包还有" + expiredConfig + "天到期，请及时更新！";
/* 43 */       String title = "【Dr.sense】ios包到期提醒";
/* 44 */       this.sysEmailService.sendEmail(emailArray, title, text);
/*    */     } 
/*    */   }
/*    */ 
/*    */   
/*    */   public void monitorDataUpdate() {
/* 50 */     String dataConfig = this.sysConfigService.selectConfigByKey("data.update.expired");
/* 51 */     Date lastUpdateTime = this.terSensorStatusMapper.getTerLightStatusUpdateTime();
/* 52 */     log.info("告警配置：{}，数据更新时间：{}", dataConfig, lastUpdateTime);
/*    */     
/* 54 */     int updatelFlag = 0;
/* 55 */     if (lastUpdateTime != null && System.currentTimeMillis() - lastUpdateTime.getTime() > Integer.parseInt(dataConfig) * 60L * 1000L) {
/*    */       
/* 57 */       String emailStr = this.sysConfigService.selectConfigByKey("email.alert.address");
/* 58 */       String[] emailArray = emailStr.split(",");
/* 59 */       String text = "【Dr.sense】数据更新时间超过" + dataConfig + "分钟，请及时处理！";
/* 60 */       String title = "【Dr.sense】数据更新异常提醒";
/* 61 */       this.sysEmailService.sendEmail(emailArray, title, text);
/* 62 */       updatelFlag = 1;
/*    */     } 
/*    */     
/*    */     try {
/* 66 */       FileUtils.writeStringToFile(new File("/app/server/updateFlag"), updatelFlag + "");
/* 67 */     } catch (Exception e) {
/* 68 */       log.error("保存数据更新标记异常", e);
/*    */     } 
/*    */   }
/*    */ }


/* Location:              /juyuan-iotlighting-3.8.6/!/com/ruoyi/iotlighting/task/MonitorTast.class
 * Java compiler version: 8 (52.0)
 * JD-Core Version:       1.1.3
 */