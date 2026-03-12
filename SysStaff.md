/*    */ package com.ruoyi.iotlighting.domain;
/*    */ public class SysStaff extends BaseEntity { private static final long serialVersionUID = 1L; private Long staffId; @Excel(name = "用户表id")
/*    */   private Long userId;
/*    */   @Excel(name = "员工编号")
/*    */   private String staffNumber;
/*    */   @Excel(name = "员工职位：lifeguard救生员，patrol 巡检人员")
/*    */   private String staffPosition;
/*    */   
/*  9 */   public void setStaffId(Long staffId) { this.staffId = staffId; } @Excel(name = "工牌号码") private String licenseNumber; @Excel(name = "用户密码") private String password; private String userName; private String nickName; private List<Long> roleKeyList; public void setUserId(Long userId) { this.userId = userId; } public void setStaffNumber(String staffNumber) { this.staffNumber = staffNumber; } public void setStaffPosition(String staffPosition) { this.staffPosition = staffPosition; } public void setLicenseNumber(String licenseNumber) { this.licenseNumber = licenseNumber; } public void setPassword(String password) { this.password = password; } public void setUserName(String userName) { this.userName = userName; } public void setNickName(String nickName) { this.nickName = nickName; } public void setRoleKeyList(List<Long> roleKeyList) { this.roleKeyList = roleKeyList; } public boolean equals(Object o) { if (o == this) return true;  if (!(o instanceof SysStaff)) return false;  SysStaff other = (SysStaff)o; if (!other.canEqual(this)) return false;  Object this$staffId = getStaffId(), other$staffId = other.getStaffId(); if ((this$staffId == null) ? (other$staffId != null) : !this$staffId.equals(other$staffId)) return false;  Object this$userId = getUserId(), other$userId = other.getUserId(); if ((this$userId == null) ? (other$userId != null) : !this$userId.equals(other$userId)) return false;  Object this$staffNumber = getStaffNumber(), other$staffNumber = other.getStaffNumber(); if ((this$staffNumber == null) ? (other$staffNumber != null) : !this$staffNumber.equals(other$staffNumber)) return false;  Object this$staffPosition = getStaffPosition(), other$staffPosition = other.getStaffPosition(); if ((this$staffPosition == null) ? (other$staffPosition != null) : !this$staffPosition.equals(other$staffPosition)) return false;  Object this$licenseNumber = getLicenseNumber(), other$licenseNumber = other.getLicenseNumber(); if ((this$licenseNumber == null) ? (other$licenseNumber != null) : !this$licenseNumber.equals(other$licenseNumber)) return false;  Object this$password = getPassword(), other$password = other.getPassword(); if ((this$password == null) ? (other$password != null) : !this$password.equals(other$password)) return false;  Object this$userName = getUserName(), other$userName = other.getUserName(); if ((this$userName == null) ? (other$userName != null) : !this$userName.equals(other$userName)) return false;  Object this$nickName = getNickName(), other$nickName = other.getNickName(); if ((this$nickName == null) ? (other$nickName != null) : !this$nickName.equals(other$nickName)) return false;  Object<Long> this$roleKeyList = (Object<Long>)getRoleKeyList(), other$roleKeyList = (Object<Long>)other.getRoleKeyList(); return !((this$roleKeyList == null) ? (other$roleKeyList != null) : !this$roleKeyList.equals(other$roleKeyList)); } protected boolean canEqual(Object other) { return other instanceof SysStaff; } public int hashCode() { int PRIME = 59; result = 1; Object $staffId = getStaffId(); result = result * 59 + (($staffId == null) ? 43 : $staffId.hashCode()); Object $userId = getUserId(); result = result * 59 + (($userId == null) ? 43 : $userId.hashCode()); Object $staffNumber = getStaffNumber(); result = result * 59 + (($staffNumber == null) ? 43 : $staffNumber.hashCode()); Object $staffPosition = getStaffPosition(); result = result * 59 + (($staffPosition == null) ? 43 : $staffPosition.hashCode()); Object $licenseNumber = getLicenseNumber(); result = result * 59 + (($licenseNumber == null) ? 43 : $licenseNumber.hashCode()); Object $password = getPassword(); result = result * 59 + (($password == null) ? 43 : $password.hashCode()); Object $userName = getUserName(); result = result * 59 + (($userName == null) ? 43 : $userName.hashCode()); Object $nickName = getNickName(); result = result * 59 + (($nickName == null) ? 43 : $nickName.hashCode()); Object<Long> $roleKeyList = (Object<Long>)getRoleKeyList(); return result * 59 + (($roleKeyList == null) ? 43 : $roleKeyList.hashCode()); } public String toString() { return "SysStaff(staffId=" + getStaffId() + ", userId=" + getUserId() + ", staffNumber=" + getStaffNumber() + ", staffPosition=" + getStaffPosition() + ", licenseNumber=" + getLicenseNumber() + ", password=" + getPassword() + ", userName=" + getUserName() + ", nickName=" + getNickName() + ", roleKeyList=" + getRoleKeyList() + ")"; }
/*    */ 
/*    */ 
/*    */ 
/*    */ 
/*    */   
/*    */   public Long getStaffId() {
/* 16 */     return this.staffId;
/*    */   }
/*    */ 
/*    */ 
/*    */   
/*    */   public Long getUserId() {
/* 22 */     return this.userId;
/*    */   }
/*    */ 
/*    */ 
/*    */   
/*    */   public String getStaffNumber() {
/* 28 */     return this.staffNumber;
/*    */   }
/*    */ 
/*    */ 
/*    */   
/*    */   public String getStaffPosition() {
/* 34 */     return this.staffPosition;
/*    */   }
/*    */ 
/*    */ 
/*    */   
/*    */   public String getLicenseNumber() {
/* 40 */     return this.licenseNumber;
/*    */   }
/*    */ 
/*    */ 
/*    */   
/*    */   public String getPassword() {
/* 46 */     return this.password;
/*    */   } public String getUserName() {
/* 48 */     return this.userName;
/*    */   } public String getNickName() {
/* 50 */     return this.nickName;
/*    */   } public List<Long> getRoleKeyList() {
/* 52 */     return this.roleKeyList;
/*    */   } }


/* Location:              /juyuan-iotlighting-3.8.6/!/com/ruoyi/iotlighting/domain/SysStaff.class
 * Java compiler version: 8 (52.0)
 * JD-Core Version:       1.1.3
 */