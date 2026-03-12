/*     */ package com.ruoyi.iotlighting.domain;
/*     */ public class TerAlert extends BaseEntity { private static final long serialVersionUID = 1L; @JsonSerialize(using = ToStringSerializer.class)
/*     */   private Long id; @JsonFormat(pattern = "yyyy-MM-dd HH:mm:dd")
/*     */   private Date createdTime; @JsonFormat(pattern = "yyyy-MM-dd HH:mm:dd")
/*     */   private Date createdTimeStart; @JsonFormat(pattern = "yyyy-MM-dd HH:mm:dd")
/*     */   private Date createdTimeEnd; @JsonFormat(pattern = "yyyy-MM-dd HH:mm:dd")
/*     */   @Excel(name = "日期", dateFormat = "yyyy-MM-dd")
/*     */   private Date createdTimeDate; @JsonFormat(pattern = "yyyy-MM-dd HH:mm:dd")
/*     */   @Excel(name = "时间", dateFormat = "HH:mm")
/*     */   private Date createdTimeTime; @Excel(name = "大厦名称")
/*     */   private String buildingName; @Excel(name = "座")
/*     */   private String block; @Excel(name = "楼层")
/*     */   private String floorName; @Excel(name = "区域")
/*     */   private String zone; @Excel(name = "区域(分类)")
/*     */   private String zoneSub; @Excel(name = "确实位置")
/*     */   private String pointName; @Excel(name = "传感器类型", dictType = "ter_sensor_type")
/*     */   private String sensorType;
/*  18 */   public void setId(Long id) { this.id = id; } @Excel(name = "处理状态", readConverterExp = "0=未处理,1=已处理") private String dealFlag; @JsonFormat(pattern = "yyyy-MM-dd HH:mm:dd") @Excel(name = "处理时间", width = 30.0D, dateFormat = "yyyy-MM-dd HH:mm:dd") private Date dealTime; private String terSn; private String sensorStatus; private String data; private String delFlag; @JsonSerialize(using = ToStringSerializer.class) private Long buildingId; @JsonSerialize(using = ToStringSerializer.class) private Long floorId; @JsonSerialize(using = ToStringSerializer.class) private Long backgroundImgId; private Integer floorLength; private Integer floorWidth; private Integer pointX; private Integer pointY; private String checkSensorType; private String[] alertSensorType; @JsonFormat(pattern = "yyyy-MM-dd HH:mm:dd") public void setCreatedTime(Date createdTime) { this.createdTime = createdTime; } @JsonFormat(pattern = "yyyy-MM-dd HH:mm:dd") public void setCreatedTimeStart(Date createdTimeStart) { this.createdTimeStart = createdTimeStart; } @JsonFormat(pattern = "yyyy-MM-dd HH:mm:dd") public void setCreatedTimeEnd(Date createdTimeEnd) { this.createdTimeEnd = createdTimeEnd; } @JsonFormat(pattern = "yyyy-MM-dd HH:mm:dd") public void setCreatedTimeDate(Date createdTimeDate) { this.createdTimeDate = createdTimeDate; } @JsonFormat(pattern = "yyyy-MM-dd HH:mm:dd") public void setCreatedTimeTime(Date createdTimeTime) { this.createdTimeTime = createdTimeTime; } public void setBuildingName(String buildingName) { this.buildingName = buildingName; } public void setBlock(String block) { this.block = block; } public void setFloorName(String floorName) { this.floorName = floorName; } public void setZone(String zone) { this.zone = zone; } public void setZoneSub(String zoneSub) { this.zoneSub = zoneSub; } public void setPointName(String pointName) { this.pointName = pointName; } public void setSensorType(String sensorType) { this.sensorType = sensorType; } public void setDealFlag(String dealFlag) { this.dealFlag = dealFlag; } @JsonFormat(pattern = "yyyy-MM-dd HH:mm:dd") public void setDealTime(Date dealTime) { this.dealTime = dealTime; } public void setTerSn(String terSn) { this.terSn = terSn; } public void setSensorStatus(String sensorStatus) { this.sensorStatus = sensorStatus; } public void setData(String data) { this.data = data; } public void setDelFlag(String delFlag) { this.delFlag = delFlag; } public void setBuildingId(Long buildingId) { this.buildingId = buildingId; } public void setFloorId(Long floorId) { this.floorId = floorId; } public void setBackgroundImgId(Long backgroundImgId) { this.backgroundImgId = backgroundImgId; } public void setFloorLength(Integer floorLength) { this.floorLength = floorLength; } public void setFloorWidth(Integer floorWidth) { this.floorWidth = floorWidth; } public void setPointX(Integer pointX) { this.pointX = pointX; } public void setPointY(Integer pointY) { this.pointY = pointY; } public void setCheckSensorType(String checkSensorType) { this.checkSensorType = checkSensorType; } public void setAlertSensorType(String[] alertSensorType) { this.alertSensorType = alertSensorType; } public boolean equals(Object o) { if (o == this) return true;  if (!(o instanceof TerAlert)) return false;  TerAlert other = (TerAlert)o; if (!other.canEqual(this)) return false;  Object this$id = getId(), other$id = other.getId(); if ((this$id == null) ? (other$id != null) : !this$id.equals(other$id)) return false;  Object this$buildingId = getBuildingId(), other$buildingId = other.getBuildingId(); if ((this$buildingId == null) ? (other$buildingId != null) : !this$buildingId.equals(other$buildingId)) return false;  Object this$floorId = getFloorId(), other$floorId = other.getFloorId(); if ((this$floorId == null) ? (other$floorId != null) : !this$floorId.equals(other$floorId)) return false;  Object this$backgroundImgId = getBackgroundImgId(), other$backgroundImgId = other.getBackgroundImgId(); if ((this$backgroundImgId == null) ? (other$backgroundImgId != null) : !this$backgroundImgId.equals(other$backgroundImgId)) return false;  Object this$floorLength = getFloorLength(), other$floorLength = other.getFloorLength(); if ((this$floorLength == null) ? (other$floorLength != null) : !this$floorLength.equals(other$floorLength)) return false;  Object this$floorWidth = getFloorWidth(), other$floorWidth = other.getFloorWidth(); if ((this$floorWidth == null) ? (other$floorWidth != null) : !this$floorWidth.equals(other$floorWidth)) return false;  Object this$pointX = getPointX(), other$pointX = other.getPointX(); if ((this$pointX == null) ? (other$pointX != null) : !this$pointX.equals(other$pointX)) return false;  Object this$pointY = getPointY(), other$pointY = other.getPointY(); if ((this$pointY == null) ? (other$pointY != null) : !this$pointY.equals(other$pointY)) return false;  Object this$createdTime = getCreatedTime(), other$createdTime = other.getCreatedTime(); if ((this$createdTime == null) ? (other$createdTime != null) : !this$createdTime.equals(other$createdTime)) return false;  Object this$createdTimeStart = getCreatedTimeStart(), other$createdTimeStart = other.getCreatedTimeStart(); if ((this$createdTimeStart == null) ? (other$createdTimeStart != null) : !this$createdTimeStart.equals(other$createdTimeStart)) return false;  Object this$createdTimeEnd = getCreatedTimeEnd(), other$createdTimeEnd = other.getCreatedTimeEnd(); if ((this$createdTimeEnd == null) ? (other$createdTimeEnd != null) : !this$createdTimeEnd.equals(other$createdTimeEnd)) return false;  Object this$createdTimeDate = getCreatedTimeDate(), other$createdTimeDate = other.getCreatedTimeDate(); if ((this$createdTimeDate == null) ? (other$createdTimeDate != null) : !this$createdTimeDate.equals(other$createdTimeDate)) return false;  Object this$createdTimeTime = getCreatedTimeTime(), other$createdTimeTime = other.getCreatedTimeTime(); if ((this$createdTimeTime == null) ? (other$createdTimeTime != null) : !this$createdTimeTime.equals(other$createdTimeTime)) return false;  Object this$buildingName = getBuildingName(), other$buildingName = other.getBuildingName(); if ((this$buildingName == null) ? (other$buildingName != null) : !this$buildingName.equals(other$buildingName)) return false;  Object this$block = getBlock(), other$block = other.getBlock(); if ((this$block == null) ? (other$block != null) : !this$block.equals(other$block)) return false;  Object this$floorName = getFloorName(), other$floorName = other.getFloorName(); if ((this$floorName == null) ? (other$floorName != null) : !this$floorName.equals(other$floorName)) return false;  Object this$zone = getZone(), other$zone = other.getZone(); if ((this$zone == null) ? (other$zone != null) : !this$zone.equals(other$zone)) return false;  Object this$zoneSub = getZoneSub(), other$zoneSub = other.getZoneSub(); if ((this$zoneSub == null) ? (other$zoneSub != null) : !this$zoneSub.equals(other$zoneSub)) return false;  Object this$pointName = getPointName(), other$pointName = other.getPointName(); if ((this$pointName == null) ? (other$pointName != null) : !this$pointName.equals(other$pointName)) return false;  Object this$sensorType = getSensorType(), other$sensorType = other.getSensorType(); if ((this$sensorType == null) ? (other$sensorType != null) : !this$sensorType.equals(other$sensorType)) return false;  Object this$dealFlag = getDealFlag(), other$dealFlag = other.getDealFlag(); if ((this$dealFlag == null) ? (other$dealFlag != null) : !this$dealFlag.equals(other$dealFlag)) return false;  Object this$dealTime = getDealTime(), other$dealTime = other.getDealTime(); if ((this$dealTime == null) ? (other$dealTime != null) : !this$dealTime.equals(other$dealTime)) return false;  Object this$terSn = getTerSn(), other$terSn = other.getTerSn(); if ((this$terSn == null) ? (other$terSn != null) : !this$terSn.equals(other$terSn)) return false;  Object this$sensorStatus = getSensorStatus(), other$sensorStatus = other.getSensorStatus(); if ((this$sensorStatus == null) ? (other$sensorStatus != null) : !this$sensorStatus.equals(other$sensorStatus)) return false;  Object this$data = getData(), other$data = other.getData(); if ((this$data == null) ? (other$data != null) : !this$data.equals(other$data)) return false;  Object this$delFlag = getDelFlag(), other$delFlag = other.getDelFlag(); if ((this$delFlag == null) ? (other$delFlag != null) : !this$delFlag.equals(other$delFlag)) return false;  Object this$checkSensorType = getCheckSensorType(), other$checkSensorType = other.getCheckSensorType(); return ((this$checkSensorType == null) ? (other$checkSensorType != null) : !this$checkSensorType.equals(other$checkSensorType)) ? false : (!!Arrays.deepEquals((Object[])getAlertSensorType(), (Object[])other.getAlertSensorType())); } protected boolean canEqual(Object other) { return other instanceof TerAlert; } public int hashCode() { int PRIME = 59; result = 1; Object $id = getId(); result = result * 59 + (($id == null) ? 43 : $id.hashCode()); Object $buildingId = getBuildingId(); result = result * 59 + (($buildingId == null) ? 43 : $buildingId.hashCode()); Object $floorId = getFloorId(); result = result * 59 + (($floorId == null) ? 43 : $floorId.hashCode()); Object $backgroundImgId = getBackgroundImgId(); result = result * 59 + (($backgroundImgId == null) ? 43 : $backgroundImgId.hashCode()); Object $floorLength = getFloorLength(); result = result * 59 + (($floorLength == null) ? 43 : $floorLength.hashCode()); Object $floorWidth = getFloorWidth(); result = result * 59 + (($floorWidth == null) ? 43 : $floorWidth.hashCode()); Object $pointX = getPointX(); result = result * 59 + (($pointX == null) ? 43 : $pointX.hashCode()); Object $pointY = getPointY(); result = result * 59 + (($pointY == null) ? 43 : $pointY.hashCode()); Object $createdTime = getCreatedTime(); result = result * 59 + (($createdTime == null) ? 43 : $createdTime.hashCode()); Object $createdTimeStart = getCreatedTimeStart(); result = result * 59 + (($createdTimeStart == null) ? 43 : $createdTimeStart.hashCode()); Object $createdTimeEnd = getCreatedTimeEnd(); result = result * 59 + (($createdTimeEnd == null) ? 43 : $createdTimeEnd.hashCode()); Object $createdTimeDate = getCreatedTimeDate(); result = result * 59 + (($createdTimeDate == null) ? 43 : $createdTimeDate.hashCode()); Object $createdTimeTime = getCreatedTimeTime(); result = result * 59 + (($createdTimeTime == null) ? 43 : $createdTimeTime.hashCode()); Object $buildingName = getBuildingName(); result = result * 59 + (($buildingName == null) ? 43 : $buildingName.hashCode()); Object $block = getBlock(); result = result * 59 + (($block == null) ? 43 : $block.hashCode()); Object $floorName = getFloorName(); result = result * 59 + (($floorName == null) ? 43 : $floorName.hashCode()); Object $zone = getZone(); result = result * 59 + (($zone == null) ? 43 : $zone.hashCode()); Object $zoneSub = getZoneSub(); result = result * 59 + (($zoneSub == null) ? 43 : $zoneSub.hashCode()); Object $pointName = getPointName(); result = result * 59 + (($pointName == null) ? 43 : $pointName.hashCode()); Object $sensorType = getSensorType(); result = result * 59 + (($sensorType == null) ? 43 : $sensorType.hashCode()); Object $dealFlag = getDealFlag(); result = result * 59 + (($dealFlag == null) ? 43 : $dealFlag.hashCode()); Object $dealTime = getDealTime(); result = result * 59 + (($dealTime == null) ? 43 : $dealTime.hashCode()); Object $terSn = getTerSn(); result = result * 59 + (($terSn == null) ? 43 : $terSn.hashCode()); Object $sensorStatus = getSensorStatus(); result = result * 59 + (($sensorStatus == null) ? 43 : $sensorStatus.hashCode()); Object $data = getData(); result = result * 59 + (($data == null) ? 43 : $data.hashCode()); Object $delFlag = getDelFlag(); result = result * 59 + (($delFlag == null) ? 43 : $delFlag.hashCode()); Object $checkSensorType = getCheckSensorType(); result = result * 59 + (($checkSensorType == null) ? 43 : $checkSensorType.hashCode()); return result * 59 + Arrays.deepHashCode((Object[])getAlertSensorType()); } public String toString() { return "TerAlert(id=" + getId() + ", createdTime=" + getCreatedTime() + ", createdTimeStart=" + getCreatedTimeStart() + ", createdTimeEnd=" + getCreatedTimeEnd() + ", createdTimeDate=" + getCreatedTimeDate() + ", createdTimeTime=" + getCreatedTimeTime() + ", buildingName=" + getBuildingName() + ", block=" + getBlock() + ", floorName=" + getFloorName() + ", zone=" + getZone() + ", zoneSub=" + getZoneSub() + ", pointName=" + getPointName() + ", sensorType=" + getSensorType() + ", dealFlag=" + getDealFlag() + ", dealTime=" + getDealTime() + ", terSn=" + getTerSn() + ", sensorStatus=" + getSensorStatus() + ", data=" + getData() + ", delFlag=" + getDelFlag() + ", buildingId=" + getBuildingId() + ", floorId=" + getFloorId() + ", backgroundImgId=" + getBackgroundImgId() + ", floorLength=" + getFloorLength() + ", floorWidth=" + getFloorWidth() + ", pointX=" + getPointX() + ", pointY=" + getPointY() + ", checkSensorType=" + getCheckSensorType() + ", alertSensorType=" + Arrays.deepToString((Object[])getAlertSensorType()) + ")"; }
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */   
/*     */   public Long getId() {
/*  26 */     return this.id;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Date getCreatedTime() {
/*  32 */     return this.createdTime;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Date getCreatedTimeStart() {
/*  38 */     return this.createdTimeStart;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Date getCreatedTimeEnd() {
/*  44 */     return this.createdTimeEnd;
/*     */   }
/*     */ 
/*     */ 
/*     */ 
/*     */   
/*     */   public Date getCreatedTimeDate() {
/*  51 */     return this.createdTimeDate;
/*     */   }
/*     */ 
/*     */ 
/*     */ 
/*     */   
/*     */   public Date getCreatedTimeTime() {
/*  58 */     return this.createdTimeTime;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getBuildingName() {
/*  64 */     return this.buildingName;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getBlock() {
/*  70 */     return this.block;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getFloorName() {
/*  76 */     return this.floorName;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getZone() {
/*  82 */     return this.zone;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getZoneSub() {
/*  88 */     return this.zoneSub;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getPointName() {
/*  94 */     return this.pointName;
/*     */   }
/*     */ 
/*     */ 
/*     */ 
/*     */   
/*     */   public String getSensorType() {
/* 101 */     return this.sensorType;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getDealFlag() {
/* 107 */     return this.dealFlag;
/*     */   }
/*     */ 
/*     */ 
/*     */ 
/*     */   
/*     */   public Date getDealTime() {
/* 114 */     return this.dealTime;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getTerSn() {
/* 119 */     return this.terSn;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getSensorStatus() {
/* 125 */     return this.sensorStatus;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getData() {
/* 130 */     return this.data;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getDelFlag() {
/* 136 */     return this.delFlag;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Long getBuildingId() {
/* 142 */     return this.buildingId;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Long getFloorId() {
/* 148 */     return this.floorId;
/*     */   }
/*     */   public Long getBackgroundImgId() {
/* 151 */     return this.backgroundImgId;
/*     */   } public Integer getFloorLength() {
/* 153 */     return this.floorLength;
/*     */   } public Integer getFloorWidth() {
/* 155 */     return this.floorWidth;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Integer getPointX() {
/* 161 */     return this.pointX;
/*     */   }
/*     */ 
/*     */   
/*     */   public Integer getPointY() {
/* 166 */     return this.pointY;
/*     */   }
/*     */   public String getCheckSensorType() {
/* 169 */     return this.checkSensorType;
/*     */   } public String[] getAlertSensorType() {
/* 171 */     return this.alertSensorType;
/*     */   } }


/* Location:              /juyuan-iotlighting-3.8.6/!/com/ruoyi/iotlighting/domain/TerAlert.class
 * Java compiler version: 8 (52.0)
 * JD-Core Version:       1.1.3
 */