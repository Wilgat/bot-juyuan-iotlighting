/*    */ package com.ruoyi.iotlighting.domain;
/*    */ 
/*    */ import com.fasterxml.jackson.annotation.JsonFormat;
/*    */ import com.fasterxml.jackson.databind.annotation.JsonSerialize;
/*    */ import com.fasterxml.jackson.databind.ser.std.ToStringSerializer;
/*    */ import com.ruoyi.common.annotation.Excel;
/*    */ import com.ruoyi.common.core.domain.BaseEntity;
/*    */ import java.util.Date;
/*    */ 
/*    */ public class TerBuildingPointInfo extends BaseEntity {
/*    */   private static final long serialVersionUID = 1L;
/*    */   @Excel(name = "设备SN")
/*    */   private String terSn;
/*    */   @Excel(name = "点位编号")
/*    */   @JsonSerialize(using = ToStringSerializer.class)
/*    */   private Long pointId;
/*    */   
/* 18 */   public void setTerSn(String terSn) { this.terSn = terSn; } @Excel(name = "创建人") private String createdBy; @JsonFormat(pattern = "yyyy-MM-dd") @Excel(name = "创建时间", width = 30.0D, dateFormat = "yyyy-MM-dd") private Date createdTime; private String gateway; public void setPointId(Long pointId) { this.pointId = pointId; } public void setCreatedBy(String createdBy) { this.createdBy = createdBy; } @JsonFormat(pattern = "yyyy-MM-dd") public void setCreatedTime(Date createdTime) { this.createdTime = createdTime; } public void setGateway(String gateway) { this.gateway = gateway; } public boolean equals(Object o) { if (o == this) return true;  if (!(o instanceof TerBuildingPointInfo)) return false;  TerBuildingPointInfo other = (TerBuildingPointInfo)o; if (!other.canEqual(this)) return false;  Object this$pointId = getPointId(), other$pointId = other.getPointId(); if ((this$pointId == null) ? (other$pointId != null) : !this$pointId.equals(other$pointId)) return false;  Object this$terSn = getTerSn(), other$terSn = other.getTerSn(); if ((this$terSn == null) ? (other$terSn != null) : !this$terSn.equals(other$terSn)) return false;  Object this$createdBy = getCreatedBy(), other$createdBy = other.getCreatedBy(); if ((this$createdBy == null) ? (other$createdBy != null) : !this$createdBy.equals(other$createdBy)) return false;  Object this$createdTime = getCreatedTime(), other$createdTime = other.getCreatedTime(); if ((this$createdTime == null) ? (other$createdTime != null) : !this$createdTime.equals(other$createdTime)) return false;  Object this$gateway = getGateway(), other$gateway = other.getGateway(); return !((this$gateway == null) ? (other$gateway != null) : !this$gateway.equals(other$gateway)); } protected boolean canEqual(Object other) { return other instanceof TerBuildingPointInfo; } public int hashCode() { int PRIME = 59; result = 1; Object $pointId = getPointId(); result = result * 59 + (($pointId == null) ? 43 : $pointId.hashCode()); Object $terSn = getTerSn(); result = result * 59 + (($terSn == null) ? 43 : $terSn.hashCode()); Object $createdBy = getCreatedBy(); result = result * 59 + (($createdBy == null) ? 43 : $createdBy.hashCode()); Object $createdTime = getCreatedTime(); result = result * 59 + (($createdTime == null) ? 43 : $createdTime.hashCode()); Object $gateway = getGateway(); return result * 59 + (($gateway == null) ? 43 : $gateway.hashCode()); } public String toString() { return "TerBuildingPointInfo(terSn=" + getTerSn() + ", pointId=" + getPointId() + ", createdBy=" + getCreatedBy() + ", createdTime=" + getCreatedTime() + ", gateway=" + getGateway() + ")"; }
/*    */ 
/*    */ 
/*    */ 
/*    */ 
/*    */ 
/*    */   
/*    */   public String getTerSn() {
/* 26 */     return this.terSn;
/*    */   }
/*    */ 
/*    */ 
/*    */ 
/*    */   
/*    */   public Long getPointId() {
/* 33 */     return this.pointId;
/*    */   }
/*    */ 
/*    */ 
/*    */   
/*    */   public String getCreatedBy() {
/* 39 */     return this.createdBy;
/*    */   }
/*    */ 
/*    */ 
/*    */ 
/*    */   
/*    */   public Date getCreatedTime() {
/* 46 */     return this.createdTime;
/*    */   }
/*    */ 
/*    */   
/*    */   public String getGateway() {
/* 51 */     return this.gateway;
/*    */   }
/*    */ }


/* Location:              /juyuan-iotlighting-3.8.6/!/com/ruoyi/iotlighting/domain/TerBuildingPointInfo.class
 * Java compiler version: 8 (52.0)
 * JD-Core Version:       1.1.3
 */