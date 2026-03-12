/*    */ package com.ruoyi.iotlighting.domain;
/*    */ 
/*    */ import com.fasterxml.jackson.databind.ser.std.ToStringSerializer;
/*    */ 
/*    */ public class BuildingTerStatus extends BaseEntity {
/*    */   private static final long serialVersionUID = 1L;
/*    */   @JsonSerialize(using = ToStringSerializer.class)
/*    */   private Long id;
/*    */   @JsonSerialize(using = ToStringSerializer.class)
/*    */   private Long buildingId;
/*    */   private String floorName;
/*    */   private String delFlag;
/*    */   private String terSn;
/*    */   private String terStatus;
/*    */   private String sensorType;
/*    */   private String sensorStatus;
/*    */   
/* 18 */   public void setId(Long id) { this.id = id; } public void setBuildingId(Long buildingId) { this.buildingId = buildingId; } public void setFloorName(String floorName) { this.floorName = floorName; } public void setDelFlag(String delFlag) { this.delFlag = delFlag; } public void setTerSn(String terSn) { this.terSn = terSn; } public void setTerStatus(String terStatus) { this.terStatus = terStatus; } public void setSensorType(String sensorType) { this.sensorType = sensorType; } public void setSensorStatus(String sensorStatus) { this.sensorStatus = sensorStatus; } public boolean equals(Object o) { if (o == this) return true;  if (!(o instanceof BuildingTerStatus)) return false;  BuildingTerStatus other = (BuildingTerStatus)o; if (!other.canEqual(this)) return false;  Object this$id = getId(), other$id = other.getId(); if ((this$id == null) ? (other$id != null) : !this$id.equals(other$id)) return false;  Object this$buildingId = getBuildingId(), other$buildingId = other.getBuildingId(); if ((this$buildingId == null) ? (other$buildingId != null) : !this$buildingId.equals(other$buildingId)) return false;  Object this$floorName = getFloorName(), other$floorName = other.getFloorName(); if ((this$floorName == null) ? (other$floorName != null) : !this$floorName.equals(other$floorName)) return false;  Object this$delFlag = getDelFlag(), other$delFlag = other.getDelFlag(); if ((this$delFlag == null) ? (other$delFlag != null) : !this$delFlag.equals(other$delFlag)) return false;  Object this$terSn = getTerSn(), other$terSn = other.getTerSn(); if ((this$terSn == null) ? (other$terSn != null) : !this$terSn.equals(other$terSn)) return false;  Object this$terStatus = getTerStatus(), other$terStatus = other.getTerStatus(); if ((this$terStatus == null) ? (other$terStatus != null) : !this$terStatus.equals(other$terStatus)) return false;  Object this$sensorType = getSensorType(), other$sensorType = other.getSensorType(); if ((this$sensorType == null) ? (other$sensorType != null) : !this$sensorType.equals(other$sensorType)) return false;  Object this$sensorStatus = getSensorStatus(), other$sensorStatus = other.getSensorStatus(); return !((this$sensorStatus == null) ? (other$sensorStatus != null) : !this$sensorStatus.equals(other$sensorStatus)); } protected boolean canEqual(Object other) { return other instanceof BuildingTerStatus; } public int hashCode() { int PRIME = 59; result = 1; Object $id = getId(); result = result * 59 + (($id == null) ? 43 : $id.hashCode()); Object $buildingId = getBuildingId(); result = result * 59 + (($buildingId == null) ? 43 : $buildingId.hashCode()); Object $floorName = getFloorName(); result = result * 59 + (($floorName == null) ? 43 : $floorName.hashCode()); Object $delFlag = getDelFlag(); result = result * 59 + (($delFlag == null) ? 43 : $delFlag.hashCode()); Object $terSn = getTerSn(); result = result * 59 + (($terSn == null) ? 43 : $terSn.hashCode()); Object $terStatus = getTerStatus(); result = result * 59 + (($terStatus == null) ? 43 : $terStatus.hashCode()); Object $sensorType = getSensorType(); result = result * 59 + (($sensorType == null) ? 43 : $sensorType.hashCode()); Object $sensorStatus = getSensorStatus(); return result * 59 + (($sensorStatus == null) ? 43 : $sensorStatus.hashCode()); } public String toString() { return "BuildingTerStatus(id=" + getId() + ", buildingId=" + getBuildingId() + ", floorName=" + getFloorName() + ", delFlag=" + getDelFlag() + ", terSn=" + getTerSn() + ", terStatus=" + getTerStatus() + ", sensorType=" + getSensorType() + ", sensorStatus=" + getSensorStatus() + ")"; }
/*    */ 
/*    */ 
/*    */ 
/*    */ 
/*    */ 
/*    */   
/*    */   public Long getId() {
/* 26 */     return this.id;
/*    */   }
/*    */ 
/*    */ 
/*    */   
/*    */   public Long getBuildingId() {
/* 32 */     return this.buildingId;
/*    */   }
/*    */   public String getFloorName() {
/* 35 */     return this.floorName;
/*    */   }
/*    */ 
/*    */   
/*    */   public String getDelFlag() {
/* 40 */     return this.delFlag;
/*    */   }
/*    */ 
/*    */   
/*    */   public String getTerSn() {
/* 45 */     return this.terSn;
/*    */   }
/*    */ 
/*    */   
/*    */   public String getTerStatus() {
/* 50 */     return this.terStatus;
/*    */   }
/*    */ 
/*    */   
/*    */   public String getSensorType() {
/* 55 */     return this.sensorType;
/*    */   }
/*    */ 
/*    */   
/*    */   public String getSensorStatus() {
/* 60 */     return this.sensorStatus;
/*    */   }
/*    */ }


/* Location:              /juyuan-iotlighting-3.8.6/!/com/ruoyi/iotlighting/domain/BuildingTerStatus.class
 * Java compiler version: 8 (52.0)
 * JD-Core Version:       1.1.3
 */