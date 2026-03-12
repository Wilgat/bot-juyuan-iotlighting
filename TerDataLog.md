/*     */ package com.ruoyi.iotlighting.domain;
/*     */ 
/*     */ 
/*     */ public class TerDataLog extends BaseEntity {
/*     */   private static final long serialVersionUID = 1L;
/*     */   @JsonSerialize(using = ToStringSerializer.class)
/*     */   private Long id;
/*     */   @Excel(name = "设备SN")
/*     */   private String terSn;
/*     */   @Excel(name = "传感器类型")
/*     */   private String sensorType;
/*     */   private String sensorStatus;
/*     */   @Excel(name = "数据")
/*     */   private String data;
/*     */   @JsonFormat(pattern = "yyyy-MM-dd HH:mm:dd")
/*     */   @Excel(name = "创建时间", width = 30.0D, dateFormat = "yyyy-MM-dd HH:mm:dd")
/*     */   private Date createdTime;
/*     */   private String delFlag;
/*     */   
/*  20 */   public void setId(Long id) { this.id = id; } private String floorName; @JsonSerialize(using = ToStringSerializer.class) private Long buildingId; @JsonSerialize(using = ToStringSerializer.class) private Long floorId; private Integer pointX; private Integer pointY; private String pointName; @JsonSerialize(using = ToStringSerializer.class) private Long gateway; private String gatewayName; public void setTerSn(String terSn) { this.terSn = terSn; } public void setSensorType(String sensorType) { this.sensorType = sensorType; } public void setSensorStatus(String sensorStatus) { this.sensorStatus = sensorStatus; } public void setData(String data) { this.data = data; } @JsonFormat(pattern = "yyyy-MM-dd HH:mm:dd") public void setCreatedTime(Date createdTime) { this.createdTime = createdTime; } public void setDelFlag(String delFlag) { this.delFlag = delFlag; } public void setFloorName(String floorName) { this.floorName = floorName; } public void setBuildingId(Long buildingId) { this.buildingId = buildingId; } public void setFloorId(Long floorId) { this.floorId = floorId; } public void setPointX(Integer pointX) { this.pointX = pointX; } public void setPointY(Integer pointY) { this.pointY = pointY; } public void setPointName(String pointName) { this.pointName = pointName; } public void setGateway(Long gateway) { this.gateway = gateway; } public void setGatewayName(String gatewayName) { this.gatewayName = gatewayName; } public boolean equals(Object o) { if (o == this) return true;  if (!(o instanceof TerDataLog)) return false;  TerDataLog other = (TerDataLog)o; if (!other.canEqual(this)) return false;  Object this$id = getId(), other$id = other.getId(); if ((this$id == null) ? (other$id != null) : !this$id.equals(other$id)) return false;  Object this$buildingId = getBuildingId(), other$buildingId = other.getBuildingId(); if ((this$buildingId == null) ? (other$buildingId != null) : !this$buildingId.equals(other$buildingId)) return false;  Object this$floorId = getFloorId(), other$floorId = other.getFloorId(); if ((this$floorId == null) ? (other$floorId != null) : !this$floorId.equals(other$floorId)) return false;  Object this$pointX = getPointX(), other$pointX = other.getPointX(); if ((this$pointX == null) ? (other$pointX != null) : !this$pointX.equals(other$pointX)) return false;  Object this$pointY = getPointY(), other$pointY = other.getPointY(); if ((this$pointY == null) ? (other$pointY != null) : !this$pointY.equals(other$pointY)) return false;  Object this$gateway = getGateway(), other$gateway = other.getGateway(); if ((this$gateway == null) ? (other$gateway != null) : !this$gateway.equals(other$gateway)) return false;  Object this$terSn = getTerSn(), other$terSn = other.getTerSn(); if ((this$terSn == null) ? (other$terSn != null) : !this$terSn.equals(other$terSn)) return false;  Object this$sensorType = getSensorType(), other$sensorType = other.getSensorType(); if ((this$sensorType == null) ? (other$sensorType != null) : !this$sensorType.equals(other$sensorType)) return false;  Object this$sensorStatus = getSensorStatus(), other$sensorStatus = other.getSensorStatus(); if ((this$sensorStatus == null) ? (other$sensorStatus != null) : !this$sensorStatus.equals(other$sensorStatus)) return false;  Object this$data = getData(), other$data = other.getData(); if ((this$data == null) ? (other$data != null) : !this$data.equals(other$data)) return false;  Object this$createdTime = getCreatedTime(), other$createdTime = other.getCreatedTime(); if ((this$createdTime == null) ? (other$createdTime != null) : !this$createdTime.equals(other$createdTime)) return false;  Object this$delFlag = getDelFlag(), other$delFlag = other.getDelFlag(); if ((this$delFlag == null) ? (other$delFlag != null) : !this$delFlag.equals(other$delFlag)) return false;  Object this$floorName = getFloorName(), other$floorName = other.getFloorName(); if ((this$floorName == null) ? (other$floorName != null) : !this$floorName.equals(other$floorName)) return false;  Object this$pointName = getPointName(), other$pointName = other.getPointName(); if ((this$pointName == null) ? (other$pointName != null) : !this$pointName.equals(other$pointName)) return false;  Object this$gatewayName = getGatewayName(), other$gatewayName = other.getGatewayName(); return !((this$gatewayName == null) ? (other$gatewayName != null) : !this$gatewayName.equals(other$gatewayName)); } protected boolean canEqual(Object other) { return other instanceof TerDataLog; } public int hashCode() { int PRIME = 59; result = 1; Object $id = getId(); result = result * 59 + (($id == null) ? 43 : $id.hashCode()); Object $buildingId = getBuildingId(); result = result * 59 + (($buildingId == null) ? 43 : $buildingId.hashCode()); Object $floorId = getFloorId(); result = result * 59 + (($floorId == null) ? 43 : $floorId.hashCode()); Object $pointX = getPointX(); result = result * 59 + (($pointX == null) ? 43 : $pointX.hashCode()); Object $pointY = getPointY(); result = result * 59 + (($pointY == null) ? 43 : $pointY.hashCode()); Object $gateway = getGateway(); result = result * 59 + (($gateway == null) ? 43 : $gateway.hashCode()); Object $terSn = getTerSn(); result = result * 59 + (($terSn == null) ? 43 : $terSn.hashCode()); Object $sensorType = getSensorType(); result = result * 59 + (($sensorType == null) ? 43 : $sensorType.hashCode()); Object $sensorStatus = getSensorStatus(); result = result * 59 + (($sensorStatus == null) ? 43 : $sensorStatus.hashCode()); Object $data = getData(); result = result * 59 + (($data == null) ? 43 : $data.hashCode()); Object $createdTime = getCreatedTime(); result = result * 59 + (($createdTime == null) ? 43 : $createdTime.hashCode()); Object $delFlag = getDelFlag(); result = result * 59 + (($delFlag == null) ? 43 : $delFlag.hashCode()); Object $floorName = getFloorName(); result = result * 59 + (($floorName == null) ? 43 : $floorName.hashCode()); Object $pointName = getPointName(); result = result * 59 + (($pointName == null) ? 43 : $pointName.hashCode()); Object $gatewayName = getGatewayName(); return result * 59 + (($gatewayName == null) ? 43 : $gatewayName.hashCode()); } public String toString() { return "TerDataLog(id=" + getId() + ", terSn=" + getTerSn() + ", sensorType=" + getSensorType() + ", sensorStatus=" + getSensorStatus() + ", data=" + getData() + ", createdTime=" + getCreatedTime() + ", delFlag=" + getDelFlag() + ", floorName=" + getFloorName() + ", buildingId=" + getBuildingId() + ", floorId=" + getFloorId() + ", pointX=" + getPointX() + ", pointY=" + getPointY() + ", pointName=" + getPointName() + ", gateway=" + getGateway() + ", gatewayName=" + getGatewayName() + ")"; }
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */ 
/*     */   
/*     */   public Long getId() {
/*  28 */     return this.id;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getTerSn() {
/*  34 */     return this.terSn;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getSensorType() {
/*  40 */     return this.sensorType;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getSensorStatus() {
/*  45 */     return this.sensorStatus;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public String getData() {
/*  51 */     return this.data;
/*     */   }
/*     */ 
/*     */ 
/*     */ 
/*     */   
/*     */   public Date getCreatedTime() {
/*  58 */     return this.createdTime;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getDelFlag() {
/*  63 */     return this.delFlag;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getFloorName() {
/*  68 */     return this.floorName;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Long getBuildingId() {
/*  74 */     return this.buildingId;
/*     */   }
/*     */ 
/*     */ 
/*     */   
/*     */   public Long getFloorId() {
/*  80 */     return this.floorId;
/*     */   }
/*     */ 
/*     */   
/*     */   public Integer getPointX() {
/*  85 */     return this.pointX;
/*     */   }
/*     */ 
/*     */   
/*     */   public Integer getPointY() {
/*  90 */     return this.pointY;
/*     */   }
/*     */ 
/*     */   
/*     */   public String getPointName() {
/*  95 */     return this.pointName;
/*     */   }
/*     */   public Long getGateway() {
/*  98 */     return this.gateway;
/*     */   } public String getGatewayName() {
/* 100 */     return this.gatewayName;
/*     */   }
/*     */ }


/* Location:              /juyuan-iotlighting-3.8.6/!/com/ruoyi/iotlighting/domain/TerDataLog.class
 * Java compiler version: 8 (52.0)
 * JD-Core Version:       1.1.3
 */