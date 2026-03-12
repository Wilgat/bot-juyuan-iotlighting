/*    */ package com.ruoyi.iotlighting.domain;
/*    */ 
/*    */ public class TerAlertCount extends BaseEntity {
/*    */   private String sensorType;
/*    */   
/*  6 */   public void setSensorType(String sensorType) { this.sensorType = sensorType; } private int count; private String[] alertSensorType; public void setCount(int count) { this.count = count; } public void setAlertSensorType(String[] alertSensorType) { this.alertSensorType = alertSensorType; } public boolean equals(Object o) { if (o == this) return true;  if (!(o instanceof TerAlertCount)) return false;  TerAlertCount other = (TerAlertCount)o; if (!other.canEqual(this)) return false;  if (getCount() != other.getCount()) return false;  Object this$sensorType = getSensorType(), other$sensorType = other.getSensorType(); return ((this$sensorType == null) ? (other$sensorType != null) : !this$sensorType.equals(other$sensorType)) ? false : (!!Arrays.deepEquals((Object[])getAlertSensorType(), (Object[])other.getAlertSensorType())); } protected boolean canEqual(Object other) { return other instanceof TerAlertCount; } public int hashCode() { int PRIME = 59; result = 1; result = result * 59 + getCount(); Object $sensorType = getSensorType(); result = result * 59 + (($sensorType == null) ? 43 : $sensorType.hashCode()); return result * 59 + Arrays.deepHashCode((Object[])getAlertSensorType()); } public String toString() { return "TerAlertCount(sensorType=" + getSensorType() + ", count=" + getCount() + ", alertSensorType=" + Arrays.deepToString((Object[])getAlertSensorType()) + ")"; }
/*    */ 
/*    */ 
/*    */ 
/*    */   
/*    */   public String getSensorType() {
/* 12 */     return this.sensorType;
/*    */   }
/*    */ 
/*    */   
/*    */   public int getCount() {
/* 17 */     return this.count;
/*    */   } public String[] getAlertSensorType() {
/* 19 */     return this.alertSensorType;
/*    */   }
/*    */ }


/* Location:              /juyuan-iotlighting-3.8.6/!/com/ruoyi/iotlighting/domain/TerAlertCount.class
 * Java compiler version: 8 (52.0)
 * JD-Core Version:       1.1.3
 */