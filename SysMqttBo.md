/*    */ package com.ruoyi.iotlighting.mqtt.bo;
/*    */ 
/*    */ import com.ruoyi.common.core.domain.BaseEntity;
/*    */ 
/*    */ public class SysMqttBo
/*    */   extends BaseEntity {
/*    */   private String topic;
/*    */   private String data;
/*    */   private Integer qos;
/*    */   
/*    */   public void setTopic(String topic) {
/* 12 */     this.topic = topic; } public void setData(String data) { this.data = data; } public void setQos(Integer qos) { this.qos = qos; } public void setRetained(boolean retained) { this.retained = retained; } public String toString() { return "SysMqttBo(topic=" + getTopic() + ", data=" + getData() + ", qos=" + getQos() + ", retained=" + isRetained() + ")"; }
/* 13 */   public boolean equals(Object o) { if (o == this) return true;  if (!(o instanceof SysMqttBo)) return false;  SysMqttBo other = (SysMqttBo)o; if (!other.canEqual(this)) return false;  if (!super.equals(o)) return false;  if (isRetained() != other.isRetained()) return false;  Object this$qos = getQos(), other$qos = other.getQos(); if ((this$qos == null) ? (other$qos != null) : !this$qos.equals(other$qos)) return false;  Object this$topic = getTopic(), other$topic = other.getTopic(); if ((this$topic == null) ? (other$topic != null) : !this$topic.equals(other$topic)) return false;  Object this$data = getData(), other$data = other.getData(); return !((this$data == null) ? (other$data != null) : !this$data.equals(other$data)); } protected boolean canEqual(Object other) { return other instanceof SysMqttBo; } public int hashCode() { int PRIME = 59; result = super.hashCode(); result = result * 59 + (isRetained() ? 79 : 97); Object $qos = getQos(); result = result * 59 + (($qos == null) ? 43 : $qos.hashCode()); Object $topic = getTopic(); result = result * 59 + (($topic == null) ? 43 : $topic.hashCode()); Object $data = getData(); return result * 59 + (($data == null) ? 43 : $data.hashCode()); }
/*    */   
/*    */   public String getTopic() {
/* 16 */     return this.topic;
/*    */   } public String getData() {
/* 18 */     return this.data;
/*    */   } public Integer getQos() {
/* 20 */     return this.qos;
/*    */   } private boolean retained = false; public boolean isRetained() {
/* 22 */     return this.retained;
/*    */   }
/*    */ }


/* Location:              /juyuan-iotlighting-3.8.6/!/com/ruoyi/iotlighting/mqtt/bo/SysMqttBo.class
 * Java compiler version: 8 (52.0)
 * JD-Core Version:       1.1.3
 */