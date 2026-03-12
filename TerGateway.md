/*    */ package com.ruoyi.iotlighting.domain;
/*    */ 
/*    */ import java.util.Date;
/*    */ 
/*    */ public class TerGateway extends BaseEntity {
/*    */   private static final long serialVersionUID = 1L;
/*    */   @JsonSerialize(using = ToStringSerializer.class)
/*    */   private Long id;
/*    */   @Excel(name = "SN码")
/*    */   private String sn;
/*    */   private String name;
/*    */   @Excel(name = "创建人")
/*    */   private String createdBy;
/*    */   @JsonFormat(pattern = "yyyy-MM-dd HH:mm:ss")
/*    */   @Excel(name = "创建时间", width = 30.0D, dateFormat = "yyyy-MM-dd HH:mm:ss")
/*    */   private Date createdTime;
/*    */   
/* 18 */   public void setId(Long id) { this.id = id; } @Excel(name = "更新人") private String updatedBy; @JsonFormat(pattern = "yyyy-MM-dd HH:mm:ss") @Excel(name = "更新时间", width = 30.0D, dateFormat = "yyyy-MM-dd HH:mm:ss") private Date updatedTime; private String delFlag; @Excel(name = "所属部门") private Long deptId; private String buildingName; @JsonSerialize(using = ToStringSerializer.class) private Long buildingId; private String wifiType; public void setSn(String sn) { this.sn = sn; } public void setName(String name) { this.name = name; } public void setCreatedBy(String createdBy) { this.createdBy = createdBy; } @JsonFormat(pattern = "yyyy-MM-dd HH:mm:ss") public void setCreatedTime(Date createdTime) { this.createdTime = createdTime; } public void setUpdatedBy(String updatedBy) { this.updatedBy = updatedBy; } @JsonFormat(pattern = "yyyy-MM-dd HH:mm:ss") public void setUpdatedTime(Date updatedTime) { this.updatedTime = updatedTime; } public void setDelFlag(String delFlag) { this.delFlag = delFlag; } public void setDeptId(Long deptId) { this.deptId = deptId; } public void setBuildingName(String buildingName) { this.buildingName = buildingName; } public void setBuildingId(Long buildingId) { this.buildingId = buildingId; } public void setWifiType(String wifiType) { this.wifiType = wifiType; } public boolean equals(Object o) { if (o == this) return true;  if (!(o instanceof TerGateway)) return false;  TerGateway other = (TerGateway)o; if (!other.canEqual(this)) return false;  Object this$id = getId(), other$id = other.getId(); if ((this$id == null) ? (other$id != null) : !this$id.equals(other$id)) return false;  Object this$deptId = getDeptId(), other$deptId = other.getDeptId(); if ((this$deptId == null) ? (other$deptId != null) : !this$deptId.equals(other$deptId)) return false;  Object this$buildingId = getBuildingId(), other$buildingId = other.getBuildingId(); if ((this$buildingId == null) ? (other$buildingId != null) : !this$buildingId.equals(other$buildingId)) return false;  Object this$sn = getSn(), other$sn = other.getSn(); if ((this$sn == null) ? (other$sn != null) : !this$sn.equals(other$sn)) return false;  Object this$name = getName(), other$name = other.getName(); if ((this$name == null) ? (other$name != null) : !this$name.equals(other$name)) return false;  Object this$createdBy = getCreatedBy(), other$createdBy = other.getCreatedBy(); if ((this$createdBy == null) ? (other$createdBy != null) : !this$createdBy.equals(other$createdBy)) return false;  Object this$createdTime = getCreatedTime(), other$createdTime = other.getCreatedTime(); if ((this$createdTime == null) ? (other$createdTime != null) : !this$createdTime.equals(other$createdTime)) return false;  Object this$updatedBy = getUpdatedBy(), other$updatedBy = other.getUpdatedBy(); if ((this$updatedBy == null) ? (other$updatedBy != null) : !this$updatedBy.equals(other$updatedBy)) return false;  Object this$updatedTime = getUpdatedTime(), other$updatedTime = other.getUpdatedTime(); if ((this$updatedTime == null) ? (other$updatedTime != null) : !this$updatedTime.equals(other$updatedTime)) return false;  Object this$delFlag = getDelFlag(), other$delFlag = other.getDelFlag(); if ((this$delFlag == null) ? (other$delFlag != null) : !this$delFlag.equals(other$delFlag)) return false;  Object this$buildingName = getBuildingName(), other$buildingName = other.getBuildingName(); if ((this$buildingName == null) ? (other$buildingName != null) : !this$buildingName.equals(other$buildingName)) return false;  Object this$wifiType = getWifiType(), other$wifiType = other.getWifiType(); return !((this$wifiType == null) ? (other$wifiType != null) : !this$wifiType.equals(other$wifiType)); } protected boolean canEqual(Object other) { return other instanceof TerGateway; } public int hashCode() { int PRIME = 59; result = 1; Object $id = getId(); result = result * 59 + (($id == null) ? 43 : $id.hashCode()); Object $deptId = getDeptId(); result = result * 59 + (($deptId == null) ? 43 : $deptId.hashCode()); Object $buildingId = getBuildingId(); result = result * 59 + (($buildingId == null) ? 43 : $buildingId.hashCode()); Object $sn = getSn(); result = result * 59 + (($sn == null) ? 43 : $sn.hashCode()); Object $name = getName(); result = result * 59 + (($name == null) ? 43 : $name.hashCode()); Object $createdBy = getCreatedBy(); result = result * 59 + (($createdBy == null) ? 43 : $createdBy.hashCode()); Object $createdTime = getCreatedTime(); result = result * 59 + (($createdTime == null) ? 43 : $createdTime.hashCode()); Object $updatedBy = getUpdatedBy(); result = result * 59 + (($updatedBy == null) ? 43 : $updatedBy.hashCode()); Object $updatedTime = getUpdatedTime(); result = result * 59 + (($updatedTime == null) ? 43 : $updatedTime.hashCode()); Object $delFlag = getDelFlag(); result = result * 59 + (($delFlag == null) ? 43 : $delFlag.hashCode()); Object $buildingName = getBuildingName(); result = result * 59 + (($buildingName == null) ? 43 : $buildingName.hashCode()); Object $wifiType = getWifiType(); return result * 59 + (($wifiType == null) ? 43 : $wifiType.hashCode()); } public String toString() { return "TerGateway(id=" + getId() + ", sn=" + getSn() + ", name=" + getName() + ", createdBy=" + getCreatedBy() + ", createdTime=" + getCreatedTime() + ", updatedBy=" + getUpdatedBy() + ", updatedTime=" + getUpdatedTime() + ", delFlag=" + getDelFlag() + ", deptId=" + getDeptId() + ", buildingName=" + getBuildingName() + ", buildingId=" + getBuildingId() + ", wifiType=" + getWifiType() + ")"; }
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
/*    */   public String getSn() {
/* 32 */     return this.sn;
/*    */   }
/*    */ 
/*    */   
/*    */   public String getName() {
/* 37 */     return this.name;
/*    */   }
/*    */ 
/*    */ 
/*    */ 
/*    */   
/*    */   public String getCreatedBy() {
/* 44 */     return this.createdBy;
/*    */   }
/*    */ 
/*    */ 
/*    */ 
/*    */   
/*    */   public Date getCreatedTime() {
/* 51 */     return this.createdTime;
/*    */   }
/*    */ 
/*    */ 
/*    */   
/*    */   public String getUpdatedBy() {
/* 57 */     return this.updatedBy;
/*    */   }
/*    */ 
/*    */ 
/*    */ 
/*    */   
/*    */   public Date getUpdatedTime() {
/* 64 */     return this.updatedTime;
/*    */   }
/*    */ 
/*    */   
/*    */   public String getDelFlag() {
/* 69 */     return this.delFlag;
/*    */   }
/*    */ 
/*    */ 
/*    */   
/*    */   public Long getDeptId() {
/* 75 */     return this.deptId;
/*    */   } public String getBuildingName() {
/* 77 */     return this.buildingName;
/*    */   }
/*    */   public Long getBuildingId() {
/* 80 */     return this.buildingId;
/*    */   } public String getWifiType() {
/* 82 */     return this.wifiType;
/*    */   }
/*    */ }


/* Location:              /juyuan-iotlighting-3.8.6/!/com/ruoyi/iotlighting/domain/TerGateway.class
 * Java compiler version: 8 (52.0)
 * JD-Core Version:       1.1.3
 */