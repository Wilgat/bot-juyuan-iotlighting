/*     */ package com.ruoyi.iotlighting.domain;
/*     */ public class BuildingPointInfo extends BaseEntity { private static final long serialVersionUID = 1L;
/*     */   @JsonSerialize(using = ToStringSerializer.class)
/*     */   private Long id;
/*     */   @Excel(name = "建筑编号")
/*     */   @JsonSerialize(using = ToStringSerializer.class)
/*     */   private Long buildingId;
/*     */   @Excel(name = "层号")
/*     */   @JsonSerialize(using = ToStringSerializer.class)
/*     */   private Long floorId;
/*     */   private String block;
/*     */   private String zone;
/*     */   private String zoneSub;
/*     */   @Excel(name = "点位名称")
/*     */   private String pointName;
/*     */   @Excel(name = "设备类型")
/*     */   private String terType;
/*     */   @Excel(name = "X轴位置")
/*     */   private Integer pointX;
/*     */   
/*  21 */   public void setId(Long id) { this.id = id; } @Excel(name = "Y轴位置") private Integer pointY; @Excel(name = "创建人") private String createdBy; @JsonFormat(pattern = "yyyy-MM-dd") @Excel(name = "创建时间", width = 30.0D, dateFormat = "yyyy-MM-dd") private Date createdTime; @Excel(name = "更新人") private String updatedBy; @JsonFormat(pattern = "yyyy-MM-dd") @Excel(name = "更新时间", width = 30.0D, dateFormat = "yyyy-MM-dd") private Date updatedTime; private String delFlag; private String linkageStatus; private String terSn; private String terStatus; private List<TerSensorStatus> terSensorStatusList; public void setBuildingId(Long buildingId) { this.buildingId = buildingId; } public void setFloorId(Long floorId) { this.floorId = floorId; } public void setBlock(String block) { this.block = block; } public void setZone(String zone) { this.zone = zone; } public void setZoneSub(String zoneSub) { this.zoneSub = zoneSub; } public void setPointName(String pointName) { this.pointName = pointName; } public void setTerType(String terType) { this.terType = terType; } public void setPointX(Integer pointX) { this.pointX = pointX; } public void setPointY(Integer pointY) { this.pointY = pointY; } public void setCreatedBy(String createdBy) { this.createdBy = createdBy; } @JsonFormat(pattern = "yyyy-MM-dd") public void setCreatedTime(Date createdTime) { this.createdTime = createdTime; } public void setUpdatedBy(String updatedBy) { this.updatedBy = updatedBy; } @JsonFormat(pattern = "yyyy-MM-dd") public void setUpdatedTime(Date updatedTime) { this.updatedTime = updatedTime; } public void setDelFlag(String delFlag) { this.delFlag = delFlag; } public void setLinkageStatus(String linkageStatus) { this.linkageStatus = linkageStatus; } public void setTerSn(String terSn) { this.terSn = terSn; } public void setTerStatus(String terStatus) { this.terStatus = terStatus; } public void setTerSensorStatusList(List<TerSensorStatus> terSensorStatusList) { this.terSensorStatusList = terSensorStatusList; } public boolean equals(Object o) { if (o == this) return true;  if (!(o instanceof BuildingPointInfo)) return false;  BuildingPointInfo other = (BuildingPointInfo)o; if (!other.canEqual(this)) return false;  Object this$id = getId(), other$id = other.getId(); if ((this$id == null) ? (other$id != null) : !this$id.equals(other$id)) return false;  Object this$buildingId = getBuildingId(), other$buildingId = other.getBuildingId(); if ((this$buildingId == null) ? (other$buildingId != null) : !this$buildingId.equals(other$buildingId)) return false;  Object this$floorId = getFloorId(), other$floorId = other.getFloorId(); if ((this$floorId == null) ? (other$floorId != null) : !this$floorId.equals(other$floorId)) return false;  Object this$pointX = getPointX(), other$pointX = other.getPointX(); if ((this$pointX == null) ? (other$pointX != null) : !this$pointX.equals(other$pointX)) return false;  Object this$pointY = getPointY(), other$pointY = other.getPointY(); if ((this$pointY == null) ? (other$pointY != null) : !this$pointY.equals(other$pointY)) return false;  Object this$block = getBlock(), other$block = other.getBlock(); if ((this$block == null) ? (other$block != null) : !this$block.equals(other$block)) return false;  Object this$zone = getZone(), other$zone = other.getZone(); if ((this$zone == null) ? (other$zone != null) : !this$zone.equals(other$zone)) return false;  Object this$zoneSub = getZoneSub(), other$zoneSub = other.getZoneSub(); if ((this$zoneSub == null) ? (other$zoneSub != null) : !this$zoneSub.equals(other$zoneSub)) return false;  Object this$pointName = getPointName(), other$pointName = other.getPointName(); if ((this$pointName == null) ? (other$pointName != null) : !this$pointName.equals(other$pointName)) return false;  Object this$terType = getTerType(), other$terType = other.getTerType(); if ((this$terType == null) ? (other$terType != null) : !this$terType.equals(other$terType)) return false;  Object this$createdBy = getCreatedBy(), other$createdBy = other.getCreatedBy(); if ((this$createdBy == null) ? (other$createdBy != null) : !this$createdBy.equals(other$createdBy)) return false;  Object this$createdTime = getCreatedTime(), other$createdTime = other.getCreatedTime(); if ((this$createdTime == null) ? (other$createdTime != null) : !this$createdTime.equals(other$createdTime)) return false;  Object this$updatedBy = getUpdatedBy(), other$updatedBy = other.getUpdatedBy(); if ((this$updatedBy == null) ? (other$updatedBy != null) : !this$updatedBy.equals(other$updatedBy)) return false;  Object this$updatedTime = getUpdatedTime(), other$updatedTime = other.getUpdatedTime(); if ((this$updatedTime == null) ? (other$updatedTime != null) : !this$updatedTime.equals(other$updatedTime)) return false;  Object this$delFlag = getDelFlag(), other$delFlag = other.getDelFlag(); if ((this$delFlag == null) ? (other$delFlag != null) : !this$delFlag.equals(other$delFlag)) return false;  Object this$linkageStatus = getLinkageStatus(), other$linkageStatus = other.getLinkageStatus(); if ((this$linkageStatus == null) ? (other$linkageStatus != null) : !this$linkageStatus.equals(other$linkageStatus)) return false;  Object this$terSn = getTerSn(), other$terSn = other.getTerSn(); if ((this$terSn == null) ? (other$terSn != null) : !this$terSn.equals(other$terSn)) return false;  Object this$terStatus = getTerStatus(), other$terStatus = other.getTerStatus(); if ((this$terStatus == null) ? (other$terStatus != null) : !this$terStatus.equals(other$terStatus)) return false;  Object<TerSensorStatus> this$terSensorStatusList = (Object<TerSensorStatus>)getTerSensorStatusList(), other$terSensorStatusList = (Object<TerSensorStatus>)other.getTerSensorStatusList(); return !((this$terSensorStatusList == null) ? (other$terSensorStatusList != null) : !this$terSensorStatusList.equals(other$terSensorStatusList)); } protected boolean canEqual(Object other) { return other instanceof BuildingPointInfo; } public int hashCode() { int PRIME = 59; result = 1; Object $id = getId(); result = result * 59 + (($id == null) ? 43 : $id.hashCode()); Object $buildingId = getBuildingId(); result = result * 59 + (($buildingId == null) ? 43 : $buildingId.hashCode()); Object $floorId = getFloorId(); result = result * 59 + (($floorId == null) ? 43 : $floorId.hashCode()); Object $pointX = getPointX(); result = result * 59 + (($pointX == null) ? 43 : $pointX.hashCode()); Object $pointY = getPointY(); result = result * 59 + (($pointY == null) ? 43 : $pointY.hashCode()); Object $block = getBlock(); result = result * 59 + (($block == null) ? 43 : $block.hashCode()); Object $zone = getZone(); result = result * 59 + (($zone == null) ? 43 : $zone.hashCode()); Object $zoneSub = getZoneSub(); result = result * 59 + (($zoneSub == null) ? 43 : $zoneSub.hashCode()); Object $pointName = getPointName(); result = result * 59 + (($pointName == null) ? 43 : $pointName.hashCode()); Object $terType = getTerType(); result = result * 59 + (($terType == null) ? 43 : $terType.hashCode()); Object $createdBy = getCreatedBy(); result = result * 59 + (($createdBy == null) ? 43 : $createdBy.hashCode()); Object $createdTime = getCreatedTime(); result = result * 59 + (($createdTime == null) ? 43 : $createdTime.hashCode()); Object $updatedBy = getUpdatedBy(); result = result * 59 + (($updatedBy == null) ? 43 : $updatedBy.hashCode()); Object $updatedTime = getUpdatedTime(); result = result * 59 + (($updatedTime == null) ? 43 : $updatedTime.hashCode()); Object $delFlag = getDelFlag(); result = result * 59 + (($delFlag == null) ? 43 : $delFlag.hashCode()); Object $linkageStatus = getLinkageStatus(); result = result * 59 + (($linkageStatus == null) ? 43 : $linkageStatus.hashCode()); Object $terSn = getTerSn(); result = result * 59 + (($terSn == null) ? 43 : $terSn.hashCode()); Object $terStatus = getTerStatus(); result = result * 59 + (($terStatus == null) ? 43 : $terStatus.hashCode()); Object<TerSensorStatus> $terSensorStatusList = (Object<TerSensorStatus>)getTerSensorStatusList(); return result * 59 + (($terSensorStatusList == null) ? 43 : $terSensorStatusList.hashCode()); } public String toString() { return "BuildingPointInfo(id=" + getId() + ", buildingId=" + getBuildingId() + ", floorId=" + getFloorId() + ", block=" + getBlock() + ", zone=" + getZone() + ", zoneSub=" + getZoneSub() + ", pointName=" + getPointName() + ", terType=" + getTerType() + ", pointX=" + getPointX() + ", pointY=" + getPointY() + ", createdBy=" + getCreatedBy() + ", createdTime=" + getCreatedTime() + ", updatedBy=" + getUpdatedBy() + ", updatedTime=" + getUpdatedTime() + ", delFlag=" + getDelFlag() + ", linkageStatus=" + getLinkageStatus() + ", terSn=" + getTerSn() + ", terStatus=" + getTerStatus() + ", terSensorStatusList=" + getTerSensorStatusList() + ")"; }
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */   
/*     */   public Long getId() {
/*  29 */     return this.id;
/*     */   }
/*     */ 
/*     */ 
/*     */ 
/*     */   
/*     */   public Long getBuildingId() {
/*  36 */     return this.buildingId;
/*     */   }
/*     */ 
/*     */ 
/*     */ 
/*     */   
/*     */   public Long getFloorId() {
/*  43 */     return this.floorId;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getBlock() {
/*  48 */     return this.block;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getZone() {
/*  53 */     return this.zone;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getZoneSub() {
/*  58 */     return this.zoneSub;
/*     */   }
/*     */   
/*     */   public String getPointName() {
/*  62 */     return this.pointName;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getTerType() {
/*  68 */     return this.terType;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Integer getPointX() {
/*  74 */     return this.pointX;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Integer getPointY() {
/*  80 */     return this.pointY;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getCreatedBy() {
/*  86 */     return this.createdBy;
/*     */   }
/*     */ 
/*     */ 
/*     */ 
/*     */   
/*     */   public Date getCreatedTime() {
/*  93 */     return this.createdTime;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getUpdatedBy() {
/*  99 */     return this.updatedBy;
/*     */   }
/*     */ 
/*     */ 
/*     */ 
/*     */   
/*     */   public Date getUpdatedTime() {
/* 106 */     return this.updatedTime;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getDelFlag() {
/* 111 */     return this.delFlag;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getLinkageStatus() {
/* 116 */     return this.linkageStatus;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getTerSn() {
/* 121 */     return this.terSn;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getTerStatus() {
/* 126 */     return this.terStatus;
/*     */   }
/*     */ 
/*     */   
/*     */   public List<TerSensorStatus> getTerSensorStatusList() {
/* 131 */     return this.terSensorStatusList;
/*     */   } }


/* Location:              /juyuan-iotlighting-3.8.6/!/com/ruoyi/iotlighting/domain/BuildingPointInfo.class
 * Java compiler version: 8 (52.0)
 * JD-Core Version:       1.1.3
 */