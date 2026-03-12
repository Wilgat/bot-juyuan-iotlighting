/*     */ package com.ruoyi.iotlighting.domain;public class TerAlertSystem extends BaseEntity { @JsonSerialize(using = ToStringSerializer.class)
/*     */   private Long id; private Date createTime; @Excel(name = "日期", dateFormat = "yyyy-MM-dd")
/*     */   private Date createTimeDate; @Excel(name = "时间", dateFormat = "HH:mm")
/*     */   private Date createTimeTime; private String terSn; @Excel(name = "大厦名称")
/*     */   private String buildingName; @Excel(name = "座")
/*     */   private String block; @Excel(name = "楼层")
/*     */   private String floorName; @Excel(name = "区域")
/*     */   private String zone; @Excel(name = "区域(分类)")
/*     */   private String zoneSub; @Excel(name = "确实位置")
/*     */   private String pointName; @Excel(name = "告警类型", dictType = "ter_system_alert_type")
/*  11 */   private String alertType; private String sensorType; private String wifiType; private String wifiSsid; public void setId(Long id) { this.id = id; } @JsonSerialize(using = ToStringSerializer.class) private Long buildingId; @JsonSerialize(using = ToStringSerializer.class) private Long floorId; @JsonSerialize(using = ToStringSerializer.class) private Long pointId; private String delFlag; @Excel(name = "处理状态", readConverterExp = "0=未处理,1=已处理") private String dealFlag; @Excel(name = "处理时间", width = 30.0D, dateFormat = "yyyy-MM-dd HH:mm:dd") private Date dealTime; private Date createTimeStart; private Date createTimeEnd; private String checkAlertType; private String backgroundImgId; private Integer floorLength; private Integer floorWidth; private Integer pointX; private Integer pointY; private String gatewayName; public void setCreateTime(Date createTime) { this.createTime = createTime; } public void setCreateTimeDate(Date createTimeDate) { this.createTimeDate = createTimeDate; } public void setCreateTimeTime(Date createTimeTime) { this.createTimeTime = createTimeTime; } public void setTerSn(String terSn) { this.terSn = terSn; } public void setBuildingName(String buildingName) { this.buildingName = buildingName; } public void setBlock(String block) { this.block = block; } public void setFloorName(String floorName) { this.floorName = floorName; } public void setZone(String zone) { this.zone = zone; } public void setZoneSub(String zoneSub) { this.zoneSub = zoneSub; } public void setPointName(String pointName) { this.pointName = pointName; } public void setAlertType(String alertType) { this.alertType = alertType; } public void setSensorType(String sensorType) { this.sensorType = sensorType; } public void setWifiType(String wifiType) { this.wifiType = wifiType; } public void setWifiSsid(String wifiSsid) { this.wifiSsid = wifiSsid; } public void setBuildingId(Long buildingId) { this.buildingId = buildingId; } public void setFloorId(Long floorId) { this.floorId = floorId; } public void setPointId(Long pointId) { this.pointId = pointId; } public void setDelFlag(String delFlag) { this.delFlag = delFlag; } public void setDealFlag(String dealFlag) { this.dealFlag = dealFlag; } public void setDealTime(Date dealTime) { this.dealTime = dealTime; } public void setCreateTimeStart(Date createTimeStart) { this.createTimeStart = createTimeStart; } public void setCreateTimeEnd(Date createTimeEnd) { this.createTimeEnd = createTimeEnd; } public void setCheckAlertType(String checkAlertType) { this.checkAlertType = checkAlertType; } public void setBackgroundImgId(String backgroundImgId) { this.backgroundImgId = backgroundImgId; } public void setFloorLength(Integer floorLength) { this.floorLength = floorLength; } public void setFloorWidth(Integer floorWidth) { this.floorWidth = floorWidth; } public void setPointX(Integer pointX) { this.pointX = pointX; } public void setPointY(Integer pointY) { this.pointY = pointY; } public void setGatewayName(String gatewayName) { this.gatewayName = gatewayName; } public boolean equals(Object o) { if (o == this) return true;  if (!(o instanceof TerAlertSystem)) return false;  TerAlertSystem other = (TerAlertSystem)o; if (!other.canEqual(this)) return false;  Object this$id = getId(), other$id = other.getId(); if ((this$id == null) ? (other$id != null) : !this$id.equals(other$id)) return false;  Object this$buildingId = getBuildingId(), other$buildingId = other.getBuildingId(); if ((this$buildingId == null) ? (other$buildingId != null) : !this$buildingId.equals(other$buildingId)) return false;  Object this$floorId = getFloorId(), other$floorId = other.getFloorId(); if ((this$floorId == null) ? (other$floorId != null) : !this$floorId.equals(other$floorId)) return false;  Object this$pointId = getPointId(), other$pointId = other.getPointId(); if ((this$pointId == null) ? (other$pointId != null) : !this$pointId.equals(other$pointId)) return false;  Object this$floorLength = getFloorLength(), other$floorLength = other.getFloorLength(); if ((this$floorLength == null) ? (other$floorLength != null) : !this$floorLength.equals(other$floorLength)) return false;  Object this$floorWidth = getFloorWidth(), other$floorWidth = other.getFloorWidth(); if ((this$floorWidth == null) ? (other$floorWidth != null) : !this$floorWidth.equals(other$floorWidth)) return false;  Object this$pointX = getPointX(), other$pointX = other.getPointX(); if ((this$pointX == null) ? (other$pointX != null) : !this$pointX.equals(other$pointX)) return false;  Object this$pointY = getPointY(), other$pointY = other.getPointY(); if ((this$pointY == null) ? (other$pointY != null) : !this$pointY.equals(other$pointY)) return false;  Object this$createTime = getCreateTime(), other$createTime = other.getCreateTime(); if ((this$createTime == null) ? (other$createTime != null) : !this$createTime.equals(other$createTime)) return false;  Object this$createTimeDate = getCreateTimeDate(), other$createTimeDate = other.getCreateTimeDate(); if ((this$createTimeDate == null) ? (other$createTimeDate != null) : !this$createTimeDate.equals(other$createTimeDate)) return false;  Object this$createTimeTime = getCreateTimeTime(), other$createTimeTime = other.getCreateTimeTime(); if ((this$createTimeTime == null) ? (other$createTimeTime != null) : !this$createTimeTime.equals(other$createTimeTime)) return false;  Object this$terSn = getTerSn(), other$terSn = other.getTerSn(); if ((this$terSn == null) ? (other$terSn != null) : !this$terSn.equals(other$terSn)) return false;  Object this$buildingName = getBuildingName(), other$buildingName = other.getBuildingName(); if ((this$buildingName == null) ? (other$buildingName != null) : !this$buildingName.equals(other$buildingName)) return false;  Object this$block = getBlock(), other$block = other.getBlock(); if ((this$block == null) ? (other$block != null) : !this$block.equals(other$block)) return false;  Object this$floorName = getFloorName(), other$floorName = other.getFloorName(); if ((this$floorName == null) ? (other$floorName != null) : !this$floorName.equals(other$floorName)) return false;  Object this$zone = getZone(), other$zone = other.getZone(); if ((this$zone == null) ? (other$zone != null) : !this$zone.equals(other$zone)) return false;  Object this$zoneSub = getZoneSub(), other$zoneSub = other.getZoneSub(); if ((this$zoneSub == null) ? (other$zoneSub != null) : !this$zoneSub.equals(other$zoneSub)) return false;  Object this$pointName = getPointName(), other$pointName = other.getPointName(); if ((this$pointName == null) ? (other$pointName != null) : !this$pointName.equals(other$pointName)) return false;  Object this$alertType = getAlertType(), other$alertType = other.getAlertType(); if ((this$alertType == null) ? (other$alertType != null) : !this$alertType.equals(other$alertType)) return false;  Object this$sensorType = getSensorType(), other$sensorType = other.getSensorType(); if ((this$sensorType == null) ? (other$sensorType != null) : !this$sensorType.equals(other$sensorType)) return false;  Object this$wifiType = getWifiType(), other$wifiType = other.getWifiType(); if ((this$wifiType == null) ? (other$wifiType != null) : !this$wifiType.equals(other$wifiType)) return false;  Object this$wifiSsid = getWifiSsid(), other$wifiSsid = other.getWifiSsid(); if ((this$wifiSsid == null) ? (other$wifiSsid != null) : !this$wifiSsid.equals(other$wifiSsid)) return false;  Object this$delFlag = getDelFlag(), other$delFlag = other.getDelFlag(); if ((this$delFlag == null) ? (other$delFlag != null) : !this$delFlag.equals(other$delFlag)) return false;  Object this$dealFlag = getDealFlag(), other$dealFlag = other.getDealFlag(); if ((this$dealFlag == null) ? (other$dealFlag != null) : !this$dealFlag.equals(other$dealFlag)) return false;  Object this$dealTime = getDealTime(), other$dealTime = other.getDealTime(); if ((this$dealTime == null) ? (other$dealTime != null) : !this$dealTime.equals(other$dealTime)) return false;  Object this$createTimeStart = getCreateTimeStart(), other$createTimeStart = other.getCreateTimeStart(); if ((this$createTimeStart == null) ? (other$createTimeStart != null) : !this$createTimeStart.equals(other$createTimeStart)) return false;  Object this$createTimeEnd = getCreateTimeEnd(), other$createTimeEnd = other.getCreateTimeEnd(); if ((this$createTimeEnd == null) ? (other$createTimeEnd != null) : !this$createTimeEnd.equals(other$createTimeEnd)) return false;  Object this$checkAlertType = getCheckAlertType(), other$checkAlertType = other.getCheckAlertType(); if ((this$checkAlertType == null) ? (other$checkAlertType != null) : !this$checkAlertType.equals(other$checkAlertType)) return false;  Object this$backgroundImgId = getBackgroundImgId(), other$backgroundImgId = other.getBackgroundImgId(); if ((this$backgroundImgId == null) ? (other$backgroundImgId != null) : !this$backgroundImgId.equals(other$backgroundImgId)) return false;  Object this$gatewayName = getGatewayName(), other$gatewayName = other.getGatewayName(); return !((this$gatewayName == null) ? (other$gatewayName != null) : !this$gatewayName.equals(other$gatewayName)); } protected boolean canEqual(Object other) { return other instanceof TerAlertSystem; } public int hashCode() { int PRIME = 59; result = 1; Object $id = getId(); result = result * 59 + (($id == null) ? 43 : $id.hashCode()); Object $buildingId = getBuildingId(); result = result * 59 + (($buildingId == null) ? 43 : $buildingId.hashCode()); Object $floorId = getFloorId(); result = result * 59 + (($floorId == null) ? 43 : $floorId.hashCode()); Object $pointId = getPointId(); result = result * 59 + (($pointId == null) ? 43 : $pointId.hashCode()); Object $floorLength = getFloorLength(); result = result * 59 + (($floorLength == null) ? 43 : $floorLength.hashCode()); Object $floorWidth = getFloorWidth(); result = result * 59 + (($floorWidth == null) ? 43 : $floorWidth.hashCode()); Object $pointX = getPointX(); result = result * 59 + (($pointX == null) ? 43 : $pointX.hashCode()); Object $pointY = getPointY(); result = result * 59 + (($pointY == null) ? 43 : $pointY.hashCode()); Object $createTime = getCreateTime(); result = result * 59 + (($createTime == null) ? 43 : $createTime.hashCode()); Object $createTimeDate = getCreateTimeDate(); result = result * 59 + (($createTimeDate == null) ? 43 : $createTimeDate.hashCode()); Object $createTimeTime = getCreateTimeTime(); result = result * 59 + (($createTimeTime == null) ? 43 : $createTimeTime.hashCode()); Object $terSn = getTerSn(); result = result * 59 + (($terSn == null) ? 43 : $terSn.hashCode()); Object $buildingName = getBuildingName(); result = result * 59 + (($buildingName == null) ? 43 : $buildingName.hashCode()); Object $block = getBlock(); result = result * 59 + (($block == null) ? 43 : $block.hashCode()); Object $floorName = getFloorName(); result = result * 59 + (($floorName == null) ? 43 : $floorName.hashCode()); Object $zone = getZone(); result = result * 59 + (($zone == null) ? 43 : $zone.hashCode()); Object $zoneSub = getZoneSub(); result = result * 59 + (($zoneSub == null) ? 43 : $zoneSub.hashCode()); Object $pointName = getPointName(); result = result * 59 + (($pointName == null) ? 43 : $pointName.hashCode()); Object $alertType = getAlertType(); result = result * 59 + (($alertType == null) ? 43 : $alertType.hashCode()); Object $sensorType = getSensorType(); result = result * 59 + (($sensorType == null) ? 43 : $sensorType.hashCode()); Object $wifiType = getWifiType(); result = result * 59 + (($wifiType == null) ? 43 : $wifiType.hashCode()); Object $wifiSsid = getWifiSsid(); result = result * 59 + (($wifiSsid == null) ? 43 : $wifiSsid.hashCode()); Object $delFlag = getDelFlag(); result = result * 59 + (($delFlag == null) ? 43 : $delFlag.hashCode()); Object $dealFlag = getDealFlag(); result = result * 59 + (($dealFlag == null) ? 43 : $dealFlag.hashCode()); Object $dealTime = getDealTime(); result = result * 59 + (($dealTime == null) ? 43 : $dealTime.hashCode()); Object $createTimeStart = getCreateTimeStart(); result = result * 59 + (($createTimeStart == null) ? 43 : $createTimeStart.hashCode()); Object $createTimeEnd = getCreateTimeEnd(); result = result * 59 + (($createTimeEnd == null) ? 43 : $createTimeEnd.hashCode()); Object $checkAlertType = getCheckAlertType(); result = result * 59 + (($checkAlertType == null) ? 43 : $checkAlertType.hashCode()); Object $backgroundImgId = getBackgroundImgId(); result = result * 59 + (($backgroundImgId == null) ? 43 : $backgroundImgId.hashCode()); Object $gatewayName = getGatewayName(); return result * 59 + (($gatewayName == null) ? 43 : $gatewayName.hashCode()); } public String toString() { return "TerAlertSystem(id=" + getId() + ", createTime=" + getCreateTime() + ", createTimeDate=" + getCreateTimeDate() + ", createTimeTime=" + getCreateTimeTime() + ", terSn=" + getTerSn() + ", buildingName=" + getBuildingName() + ", block=" + getBlock() + ", floorName=" + getFloorName() + ", zone=" + getZone() + ", zoneSub=" + getZoneSub() + ", pointName=" + getPointName() + ", alertType=" + getAlertType() + ", sensorType=" + getSensorType() + ", wifiType=" + getWifiType() + ", wifiSsid=" + getWifiSsid() + ", buildingId=" + getBuildingId() + ", floorId=" + getFloorId() + ", pointId=" + getPointId() + ", delFlag=" + getDelFlag() + ", dealFlag=" + getDealFlag() + ", dealTime=" + getDealTime() + ", createTimeStart=" + getCreateTimeStart() + ", createTimeEnd=" + getCreateTimeEnd() + ", checkAlertType=" + getCheckAlertType() + ", backgroundImgId=" + getBackgroundImgId() + ", floorLength=" + getFloorLength() + ", floorWidth=" + getFloorWidth() + ", pointX=" + getPointX() + ", pointY=" + getPointY() + ", gatewayName=" + getGatewayName() + ")"; }
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */   
/*     */   public Long getId() {
/*  18 */     return this.id;
/*     */   } public Date getCreateTime() {
/*  20 */     return this.createTime;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Date getCreateTimeDate() {
/*  26 */     return this.createTimeDate;
/*     */   }
/*     */   public Date getCreateTimeTime() {
/*  29 */     return this.createTimeTime;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getTerSn() {
/*  34 */     return this.terSn;
/*     */   }
/*     */   public String getBuildingName() {
/*  37 */     return this.buildingName;
/*     */   }
/*     */   public String getBlock() {
/*  40 */     return this.block;
/*     */   }
/*     */   public String getFloorName() {
/*  43 */     return this.floorName;
/*     */   }
/*     */   public String getZone() {
/*  46 */     return this.zone;
/*     */   }
/*     */   public String getZoneSub() {
/*  49 */     return this.zoneSub;
/*     */   }
/*     */   public String getPointName() {
/*  52 */     return this.pointName;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getAlertType() {
/*  58 */     return this.alertType;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getSensorType() {
/*  63 */     return this.sensorType;
/*     */   } public String getWifiType() {
/*  65 */     return this.wifiType;
/*     */   } public String getWifiSsid() {
/*  67 */     return this.wifiSsid;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Long getBuildingId() {
/*  73 */     return this.buildingId;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Long getFloorId() {
/*  79 */     return this.floorId;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Long getPointId() {
/*  85 */     return this.pointId;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getDelFlag() {
/*  90 */     return this.delFlag;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getDealFlag() {
/*  96 */     return this.dealFlag;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Date getDealTime() {
/* 102 */     return this.dealTime;
/*     */   }
/*     */ 
/*     */ 
/*     */ 
/*     */   
/*     */   public Date getCreateTimeStart() {
/* 109 */     return this.createTimeStart;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Date getCreateTimeEnd() {
/* 115 */     return this.createTimeEnd;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getCheckAlertType() {
/* 121 */     return this.checkAlertType;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getBackgroundImgId() {
/* 127 */     return this.backgroundImgId;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Integer getFloorLength() {
/* 133 */     return this.floorLength;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Integer getFloorWidth() {
/* 139 */     return this.floorWidth;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Integer getPointX() {
/* 145 */     return this.pointX;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Integer getPointY() {
/* 151 */     return this.pointY;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getGatewayName() {
/* 157 */     return this.gatewayName;
/*     */   } }


/* Location:              /juyuan-iotlighting-3.8.6/!/com/ruoyi/iotlighting/domain/TerAlertSystem.class
 * Java compiler version: 8 (52.0)
 * JD-Core Version:       1.1.3
 */