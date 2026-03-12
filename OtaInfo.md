/*    */ package com.ruoyi.iotlighting.domain;
/*    */ 
/*    */ import com.fasterxml.jackson.annotation.JsonFormat;
/*    */ import com.fasterxml.jackson.databind.ser.std.ToStringSerializer;
/*    */ import com.ruoyi.common.annotation.Excel;
/*    */ import com.ruoyi.common.core.domain.BaseEntity;
/*    */ import java.util.Arrays;
/*    */ import java.util.Date;
/*    */ 
/*    */ public class OtaInfo extends BaseEntity {
/*    */   private static final long serialVersionUID = 1L;
/*    */   @JsonSerialize(using = ToStringSerializer.class)
/*    */   private Long id;
/*    */   @Excel(name = "文件名称")
/*    */   private String name;
/*    */   @Excel(name = "文件内容")
/*    */   private Byte[] data;
/*    */   private String createdBy;
/*    */   
/* 20 */   public void setId(Long id) { this.id = id; } private Date createdTime; private String updatedBy; @JsonFormat(pattern = "yyyy-MM-dd") @Excel(name = "更新时间", width = 30.0D, dateFormat = "yyyy-MM-dd") private Date updatedTime; private String delFlag; @Excel(name = "所属部门") private Long deptId; public void setName(String name) { this.name = name; } public void setData(Byte[] data) { this.data = data; } public void setCreatedBy(String createdBy) { this.createdBy = createdBy; } public void setCreatedTime(Date createdTime) { this.createdTime = createdTime; } public void setUpdatedBy(String updatedBy) { this.updatedBy = updatedBy; } @JsonFormat(pattern = "yyyy-MM-dd") public void setUpdatedTime(Date updatedTime) { this.updatedTime = updatedTime; } public void setDelFlag(String delFlag) { this.delFlag = delFlag; } public void setDeptId(Long deptId) { this.deptId = deptId; } public boolean equals(Object o) { if (o == this) return true;  if (!(o instanceof OtaInfo)) return false;  OtaInfo other = (OtaInfo)o; if (!other.canEqual(this)) return false;  Object this$id = getId(), other$id = other.getId(); if ((this$id == null) ? (other$id != null) : !this$id.equals(other$id)) return false;  Object this$deptId = getDeptId(), other$deptId = other.getDeptId(); if ((this$deptId == null) ? (other$deptId != null) : !this$deptId.equals(other$deptId)) return false;  Object this$name = getName(), other$name = other.getName(); if ((this$name == null) ? (other$name != null) : !this$name.equals(other$name)) return false;  if (!Arrays.deepEquals((Object[])getData(), (Object[])other.getData())) return false;  Object this$createdBy = getCreatedBy(), other$createdBy = other.getCreatedBy(); if ((this$createdBy == null) ? (other$createdBy != null) : !this$createdBy.equals(other$createdBy)) return false;  Object this$createdTime = getCreatedTime(), other$createdTime = other.getCreatedTime(); if ((this$createdTime == null) ? (other$createdTime != null) : !this$createdTime.equals(other$createdTime)) return false;  Object this$updatedBy = getUpdatedBy(), other$updatedBy = other.getUpdatedBy(); if ((this$updatedBy == null) ? (other$updatedBy != null) : !this$updatedBy.equals(other$updatedBy)) return false;  Object this$updatedTime = getUpdatedTime(), other$updatedTime = other.getUpdatedTime(); if ((this$updatedTime == null) ? (other$updatedTime != null) : !this$updatedTime.equals(other$updatedTime)) return false;  Object this$delFlag = getDelFlag(), other$delFlag = other.getDelFlag(); return !((this$delFlag == null) ? (other$delFlag != null) : !this$delFlag.equals(other$delFlag)); } protected boolean canEqual(Object other) { return other instanceof OtaInfo; } public int hashCode() { int PRIME = 59; result = 1; Object $id = getId(); result = result * 59 + (($id == null) ? 43 : $id.hashCode()); Object $deptId = getDeptId(); result = result * 59 + (($deptId == null) ? 43 : $deptId.hashCode()); Object $name = getName(); result = result * 59 + (($name == null) ? 43 : $name.hashCode()); result = result * 59 + Arrays.deepHashCode((Object[])getData()); Object $createdBy = getCreatedBy(); result = result * 59 + (($createdBy == null) ? 43 : $createdBy.hashCode()); Object $createdTime = getCreatedTime(); result = result * 59 + (($createdTime == null) ? 43 : $createdTime.hashCode()); Object $updatedBy = getUpdatedBy(); result = result * 59 + (($updatedBy == null) ? 43 : $updatedBy.hashCode()); Object $updatedTime = getUpdatedTime(); result = result * 59 + (($updatedTime == null) ? 43 : $updatedTime.hashCode()); Object $delFlag = getDelFlag(); return result * 59 + (($delFlag == null) ? 43 : $delFlag.hashCode()); } public String toString() { return "OtaInfo(id=" + getId() + ", name=" + getName() + ", data=" + Arrays.deepToString((Object[])getData()) + ", createdBy=" + getCreatedBy() + ", createdTime=" + getCreatedTime() + ", updatedBy=" + getUpdatedBy() + ", updatedTime=" + getUpdatedTime() + ", delFlag=" + getDelFlag() + ", deptId=" + getDeptId() + ")"; }
/*    */ 
/*    */ 
/*    */ 
/*    */ 
/*    */ 
/*    */   
/*    */   public Long getId() {
/* 28 */     return this.id;
/*    */   }
/*    */ 
/*    */ 
/*    */   
/*    */   public String getName() {
/* 34 */     return this.name;
/*    */   }
/*    */ 
/*    */ 
/*    */   
/*    */   public Byte[] getData() {
/* 40 */     return this.data;
/*    */   }
/*    */ 
/*    */   
/*    */   public String getCreatedBy() {
/* 45 */     return this.createdBy;
/*    */   }
/*    */ 
/*    */   
/*    */   public Date getCreatedTime() {
/* 50 */     return this.createdTime;
/*    */   }
/*    */ 
/*    */   
/*    */   public String getUpdatedBy() {
/* 55 */     return this.updatedBy;
/*    */   }
/*    */ 
/*    */ 
/*    */ 
/*    */   
/*    */   public Date getUpdatedTime() {
/* 62 */     return this.updatedTime;
/*    */   }
/*    */ 
/*    */   
/*    */   public String getDelFlag() {
/* 67 */     return this.delFlag;
/*    */   }
/*    */ 
/*    */ 
/*    */   
/*    */   public Long getDeptId() {
/* 73 */     return this.deptId;
/*    */   }
/*    */ }


/* Location:              /juyuan-iotlighting-3.8.6/!/com/ruoyi/iotlighting/domain/OtaInfo.class
 * Java compiler version: 8 (52.0)
 * JD-Core Version:       1.1.3
 */