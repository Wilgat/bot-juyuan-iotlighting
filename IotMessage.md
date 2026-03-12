/*    */ package com.ruoyi.iotlighting.domain;
/*    */ 
/*    */ public class IotMessage
/*    */ {
/*    */   private String sn;
/*    */   private String data;
/*    */   private String type;
/*    */   private String gateway;
/*    */   
/*    */   public void setSn(String sn) {
/* 11 */     this.sn = sn; } public void setData(String data) { this.data = data; } public void setType(String type) { this.type = type; } public void setGateway(String gateway) { this.gateway = gateway; } public boolean equals(Object o) { if (o == this) return true;  if (!(o instanceof IotMessage)) return false;  IotMessage other = (IotMessage)o; if (!other.canEqual(this)) return false;  Object this$sn = getSn(), other$sn = other.getSn(); if ((this$sn == null) ? (other$sn != null) : !this$sn.equals(other$sn)) return false;  Object this$data = getData(), other$data = other.getData(); if ((this$data == null) ? (other$data != null) : !this$data.equals(other$data)) return false;  Object this$type = getType(), other$type = other.getType(); if ((this$type == null) ? (other$type != null) : !this$type.equals(other$type)) return false;  Object this$gateway = getGateway(), other$gateway = other.getGateway(); return !((this$gateway == null) ? (other$gateway != null) : !this$gateway.equals(other$gateway)); } protected boolean canEqual(Object other) { return other instanceof IotMessage; } public int hashCode() { int PRIME = 59; result = 1; Object $sn = getSn(); result = result * 59 + (($sn == null) ? 43 : $sn.hashCode()); Object $data = getData(); result = result * 59 + (($data == null) ? 43 : $data.hashCode()); Object $type = getType(); result = result * 59 + (($type == null) ? 43 : $type.hashCode()); Object $gateway = getGateway(); return result * 59 + (($gateway == null) ? 43 : $gateway.hashCode()); } public String toString() { return "IotMessage(sn=" + getSn() + ", data=" + getData() + ", type=" + getType() + ", gateway=" + getGateway() + ")"; }
/*    */ 
/*    */ 
/*    */ 
/*    */   
/*    */   public String getSn() {
/* 17 */     return this.sn;
/*    */   }
/*    */ 
/*    */   
/*    */   public String getData() {
/* 22 */     return this.data;
/*    */   }
/*    */ 
/*    */   
/*    */   public String getType() {
/* 27 */     return this.type;
/*    */   } public String getGateway() {
/* 29 */     return this.gateway;
/*    */   }
/*    */ }


/* Location:              /juyuan-iotlighting-3.8.6/!/com/ruoyi/iotlighting/domain/IotMessage.class
 * Java compiler version: 8 (52.0)
 * JD-Core Version:       1.1.3
 */