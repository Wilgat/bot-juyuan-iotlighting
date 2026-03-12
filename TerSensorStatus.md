/*     */ package com.ruoyi.iotlighting.domain;
/*     */ public class TerSensorStatus extends BaseEntity implements Serializable { private static final long serialVersionUID = 1L; @JsonFormat(pattern = "yyyy-MM-dd HH:mm:ss")
/*     */   @Excel(name = "安装日期", dateFormat = "yyyy-MM-dd")
/*     */   private Date createdTime; @Excel(name = "产品独立代码", width = 20.0D)
/*     */   private String upc; @Excel(name = "大厦名称")
/*     */   private String buildingName; @Excel(name = "座")
/*     */   private String block; @Excel(name = "楼层")
/*     */   private String floorName;
/*     */   @Excel(name = "区域")
/*     */   private String zone;
/*     */   @Excel(name = "区域(分类)")
/*     */   private String zoneSub;
/*     */   @Excel(name = "确实位置")
/*     */   private String pointName;
/*     */   @Excel(name = "模组", dictType = "ter_sensor_type")
/*     */   private String sensorType;
/*     */   private String terSn;
/*     */   private Integer moduleNumber;
/*     */   
/*     */   @JsonFormat(pattern = "yyyy-MM-dd HH:mm:ss")
/*  21 */   public void setCreatedTime(Date createdTime) { this.createdTime = createdTime; } private String sensorStatus; @Excel(name = "设定值", handler = SensorConfigExcelHandlerAdapter.class, width = 45.0D) private String sensorConfig; private String data; private String dealFlag; @JsonFormat(pattern = "yyyy-MM-dd HH:mm:ss") private Date updatedTime; @JsonSerialize(using = ToStringSerializer.class) private Long buildingId; @JsonSerialize(using = ToStringSerializer.class) private Long floorId; private String gateway; private String checkSensorType; private List<String> terSnList; @JsonFormat(pattern = "yyyy-MM-dd HH:mm:dd") private Date createdTimeStart; @JsonFormat(pattern = "yyyy-MM-dd HH:mm:dd") private Date createdTimeEnd; public void setUpc(String upc) { this.upc = upc; } public void setBuildingName(String buildingName) { this.buildingName = buildingName; } public void setBlock(String block) { this.block = block; } public void setFloorName(String floorName) { this.floorName = floorName; } public void setZone(String zone) { this.zone = zone; } public void setZoneSub(String zoneSub) { this.zoneSub = zoneSub; } public void setPointName(String pointName) { this.pointName = pointName; } public void setSensorType(String sensorType) { this.sensorType = sensorType; } public void setTerSn(String terSn) { this.terSn = terSn; } public void setModuleNumber(Integer moduleNumber) { this.moduleNumber = moduleNumber; } public void setSensorStatus(String sensorStatus) { this.sensorStatus = sensorStatus; } public void setSensorConfig(String sensorConfig) { this.sensorConfig = sensorConfig; } public void setData(String data) { this.data = data; } public void setDealFlag(String dealFlag) { this.dealFlag = dealFlag; } @JsonFormat(pattern = "yyyy-MM-dd HH:mm:ss") public void setUpdatedTime(Date updatedTime) { this.updatedTime = updatedTime; } public void setBuildingId(Long buildingId) { this.buildingId = buildingId; } public void setFloorId(Long floorId) { this.floorId = floorId; } public void setGateway(String gateway) { this.gateway = gateway; } public void setCheckSensorType(String checkSensorType) { this.checkSensorType = checkSensorType; } public void setTerSnList(List<String> terSnList) { this.terSnList = terSnList; } @JsonFormat(pattern = "yyyy-MM-dd HH:mm:dd") public void setCreatedTimeStart(Date createdTimeStart) { this.createdTimeStart = createdTimeStart; } @JsonFormat(pattern = "yyyy-MM-dd HH:mm:dd") public void setCreatedTimeEnd(Date createdTimeEnd) { this.createdTimeEnd = createdTimeEnd; } public boolean equals(Object o) { if (o == this) return true;  if (!(o instanceof TerSensorStatus)) return false;  TerSensorStatus other = (TerSensorStatus)o; if (!other.canEqual(this)) return false;  Object this$moduleNumber = getModuleNumber(), other$moduleNumber = other.getModuleNumber(); if ((this$moduleNumber == null) ? (other$moduleNumber != null) : !this$moduleNumber.equals(other$moduleNumber)) return false;  Object this$buildingId = getBuildingId(), other$buildingId = other.getBuildingId(); if ((this$buildingId == null) ? (other$buildingId != null) : !this$buildingId.equals(other$buildingId)) return false;  Object this$floorId = getFloorId(), other$floorId = other.getFloorId(); if ((this$floorId == null) ? (other$floorId != null) : !this$floorId.equals(other$floorId)) return false;  Object this$createdTime = getCreatedTime(), other$createdTime = other.getCreatedTime(); if ((this$createdTime == null) ? (other$createdTime != null) : !this$createdTime.equals(other$createdTime)) return false;  Object this$upc = getUpc(), other$upc = other.getUpc(); if ((this$upc == null) ? (other$upc != null) : !this$upc.equals(other$upc)) return false;  Object this$buildingName = getBuildingName(), other$buildingName = other.getBuildingName(); if ((this$buildingName == null) ? (other$buildingName != null) : !this$buildingName.equals(other$buildingName)) return false;  Object this$block = getBlock(), other$block = other.getBlock(); if ((this$block == null) ? (other$block != null) : !this$block.equals(other$block)) return false;  Object this$floorName = getFloorName(), other$floorName = other.getFloorName(); if ((this$floorName == null) ? (other$floorName != null) : !this$floorName.equals(other$floorName)) return false;  Object this$zone = getZone(), other$zone = other.getZone(); if ((this$zone == null) ? (other$zone != null) : !this$zone.equals(other$zone)) return false;  Object this$zoneSub = getZoneSub(), other$zoneSub = other.getZoneSub(); if ((this$zoneSub == null) ? (other$zoneSub != null) : !this$zoneSub.equals(other$zoneSub)) return false;  Object this$pointName = getPointName(), other$pointName = other.getPointName(); if ((this$pointName == null) ? (other$pointName != null) : !this$pointName.equals(other$pointName)) return false;  Object this$sensorType = getSensorType(), other$sensorType = other.getSensorType(); if ((this$sensorType == null) ? (other$sensorType != null) : !this$sensorType.equals(other$sensorType)) return false;  Object this$terSn = getTerSn(), other$terSn = other.getTerSn(); if ((this$terSn == null) ? (other$terSn != null) : !this$terSn.equals(other$terSn)) return false;  Object this$sensorStatus = getSensorStatus(), other$sensorStatus = other.getSensorStatus(); if ((this$sensorStatus == null) ? (other$sensorStatus != null) : !this$sensorStatus.equals(other$sensorStatus)) return false;  Object this$sensorConfig = getSensorConfig(), other$sensorConfig = other.getSensorConfig(); if ((this$sensorConfig == null) ? (other$sensorConfig != null) : !this$sensorConfig.equals(other$sensorConfig)) return false;  Object this$data = getData(), other$data = other.getData(); if ((this$data == null) ? (other$data != null) : !this$data.equals(other$data)) return false;  Object this$dealFlag = getDealFlag(), other$dealFlag = other.getDealFlag(); if ((this$dealFlag == null) ? (other$dealFlag != null) : !this$dealFlag.equals(other$dealFlag)) return false;  Object this$updatedTime = getUpdatedTime(), other$updatedTime = other.getUpdatedTime(); if ((this$updatedTime == null) ? (other$updatedTime != null) : !this$updatedTime.equals(other$updatedTime)) return false;  Object this$gateway = getGateway(), other$gateway = other.getGateway(); if ((this$gateway == null) ? (other$gateway != null) : !this$gateway.equals(other$gateway)) return false;  Object this$checkSensorType = getCheckSensorType(), other$checkSensorType = other.getCheckSensorType(); if ((this$checkSensorType == null) ? (other$checkSensorType != null) : !this$checkSensorType.equals(other$checkSensorType)) return false;  Object<String> this$terSnList = (Object<String>)getTerSnList(), other$terSnList = (Object<String>)other.getTerSnList(); if ((this$terSnList == null) ? (other$terSnList != null) : !this$terSnList.equals(other$terSnList)) return false;  Object this$createdTimeStart = getCreatedTimeStart(), other$createdTimeStart = other.getCreatedTimeStart(); if ((this$createdTimeStart == null) ? (other$createdTimeStart != null) : !this$createdTimeStart.equals(other$createdTimeStart)) return false;  Object this$createdTimeEnd = getCreatedTimeEnd(), other$createdTimeEnd = other.getCreatedTimeEnd(); return !((this$createdTimeEnd == null) ? (other$createdTimeEnd != null) : !this$createdTimeEnd.equals(other$createdTimeEnd)); } protected boolean canEqual(Object other) { return other instanceof TerSensorStatus; } public int hashCode() { int PRIME = 59; result = 1; Object $moduleNumber = getModuleNumber(); result = result * 59 + (($moduleNumber == null) ? 43 : $moduleNumber.hashCode()); Object $buildingId = getBuildingId(); result = result * 59 + (($buildingId == null) ? 43 : $buildingId.hashCode()); Object $floorId = getFloorId(); result = result * 59 + (($floorId == null) ? 43 : $floorId.hashCode()); Object $createdTime = getCreatedTime(); result = result * 59 + (($createdTime == null) ? 43 : $createdTime.hashCode()); Object $upc = getUpc(); result = result * 59 + (($upc == null) ? 43 : $upc.hashCode()); Object $buildingName = getBuildingName(); result = result * 59 + (($buildingName == null) ? 43 : $buildingName.hashCode()); Object $block = getBlock(); result = result * 59 + (($block == null) ? 43 : $block.hashCode()); Object $floorName = getFloorName(); result = result * 59 + (($floorName == null) ? 43 : $floorName.hashCode()); Object $zone = getZone(); result = result * 59 + (($zone == null) ? 43 : $zone.hashCode()); Object $zoneSub = getZoneSub(); result = result * 59 + (($zoneSub == null) ? 43 : $zoneSub.hashCode()); Object $pointName = getPointName(); result = result * 59 + (($pointName == null) ? 43 : $pointName.hashCode()); Object $sensorType = getSensorType(); result = result * 59 + (($sensorType == null) ? 43 : $sensorType.hashCode()); Object $terSn = getTerSn(); result = result * 59 + (($terSn == null) ? 43 : $terSn.hashCode()); Object $sensorStatus = getSensorStatus(); result = result * 59 + (($sensorStatus == null) ? 43 : $sensorStatus.hashCode()); Object $sensorConfig = getSensorConfig(); result = result * 59 + (($sensorConfig == null) ? 43 : $sensorConfig.hashCode()); Object $data = getData(); result = result * 59 + (($data == null) ? 43 : $data.hashCode()); Object $dealFlag = getDealFlag(); result = result * 59 + (($dealFlag == null) ? 43 : $dealFlag.hashCode()); Object $updatedTime = getUpdatedTime(); result = result * 59 + (($updatedTime == null) ? 43 : $updatedTime.hashCode()); Object $gateway = getGateway(); result = result * 59 + (($gateway == null) ? 43 : $gateway.hashCode()); Object $checkSensorType = getCheckSensorType(); result = result * 59 + (($checkSensorType == null) ? 43 : $checkSensorType.hashCode()); Object<String> $terSnList = (Object<String>)getTerSnList(); result = result * 59 + (($terSnList == null) ? 43 : $terSnList.hashCode()); Object $createdTimeStart = getCreatedTimeStart(); result = result * 59 + (($createdTimeStart == null) ? 43 : $createdTimeStart.hashCode()); Object $createdTimeEnd = getCreatedTimeEnd(); return result * 59 + (($createdTimeEnd == null) ? 43 : $createdTimeEnd.hashCode()); } public String toString() { return "TerSensorStatus(createdTime=" + getCreatedTime() + ", upc=" + getUpc() + ", buildingName=" + getBuildingName() + ", block=" + getBlock() + ", floorName=" + getFloorName() + ", zone=" + getZone() + ", zoneSub=" + getZoneSub() + ", pointName=" + getPointName() + ", sensorType=" + getSensorType() + ", terSn=" + getTerSn() + ", moduleNumber=" + getModuleNumber() + ", sensorStatus=" + getSensorStatus() + ", sensorConfig=" + getSensorConfig() + ", data=" + getData() + ", dealFlag=" + getDealFlag() + ", updatedTime=" + getUpdatedTime() + ", buildingId=" + getBuildingId() + ", floorId=" + getFloorId() + ", gateway=" + getGateway() + ", checkSensorType=" + getCheckSensorType() + ", terSnList=" + getTerSnList() + ", createdTimeStart=" + getCreatedTimeStart() + ", createdTimeEnd=" + getCreatedTimeEnd() + ")"; }
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */   
/*     */   public Date getCreatedTime() {
/*  30 */     return this.createdTime;
/*     */   }
/*     */   public String getUpc() {
/*  33 */     return this.upc;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getBuildingName() {
/*  39 */     return this.buildingName;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getBlock() {
/*  45 */     return this.block;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getFloorName() {
/*  51 */     return this.floorName;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getZone() {
/*  57 */     return this.zone;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getZoneSub() {
/*  63 */     return this.zoneSub;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getPointName() {
/*  69 */     return this.pointName;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getSensorType() {
/*  75 */     return this.sensorType;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getTerSn() {
/*  80 */     return this.terSn;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Integer getModuleNumber() {
/*  86 */     return this.moduleNumber;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getSensorStatus() {
/*  91 */     return this.sensorStatus;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getSensorConfig() {
/*  97 */     return this.sensorConfig;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getData() {
/* 102 */     return this.data;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getDealFlag() {
/* 107 */     return this.dealFlag;
/*     */   }
/*     */ 
/*     */ 
/*     */ 
/*     */   
/*     */   public Date getUpdatedTime() {
/* 114 */     return this.updatedTime;
/*     */   }
/*     */   public Long getBuildingId() {
/* 117 */     return this.buildingId;
/*     */   }
/*     */   
/*     */   public Long getFloorId() {
/* 121 */     return this.floorId;
/*     */   } public String getGateway() {
/* 123 */     return this.gateway;
/*     */   } public String getCheckSensorType() {
/* 125 */     return this.checkSensorType;
/*     */   } public List<String> getTerSnList() {
/* 127 */     return this.terSnList;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Date getCreatedTimeStart() {
/* 133 */     return this.createdTimeStart;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Date getCreatedTimeEnd() {
/* 139 */     return this.createdTimeEnd;
/*     */   } }


/* Location:              /juyuan-iotlighting-3.8.6/!/com/ruoyi/iotlighting/domain/TerSensorStatus.class
 * Java compiler version: 8 (52.0)
 * JD-Core Version:       1.1.3
 */