/*    */ package com.ruoyi.iotlighting.domain.protocol;
/*    */ 
/*    */ public class ProtocolData {
/*    */   public void setStart(String start) {
/*  5 */     this.start = start; } public void setVersion(int version) { this.version = version; } public void setOption(int option) { this.option = option; } public void setEnd(String end) { this.end = end; } public boolean equals(Object o) { if (o == this) return true;  if (!(o instanceof ProtocolData)) return false;  ProtocolData other = (ProtocolData)o; if (!other.canEqual(this)) return false;  if (getVersion() != other.getVersion()) return false;  if (getOption() != other.getOption()) return false;  Object this$start = getStart(), other$start = other.getStart(); if ((this$start == null) ? (other$start != null) : !this$start.equals(other$start)) return false;  Object this$end = getEnd(), other$end = other.getEnd(); return !((this$end == null) ? (other$end != null) : !this$end.equals(other$end)); } protected boolean canEqual(Object other) { return other instanceof ProtocolData; } public int hashCode() { int PRIME = 59; result = 1; result = result * 59 + getVersion(); result = result * 59 + getOption(); Object $start = getStart(); result = result * 59 + (($start == null) ? 43 : $start.hashCode()); Object $end = getEnd(); return result * 59 + (($end == null) ? 43 : $end.hashCode()); } public String toString() { return "ProtocolData(start=" + getStart() + ", version=" + getVersion() + ", option=" + getOption() + ", end=" + getEnd() + ")"; }
/*    */ 
/*    */ 
/*    */ 
/*    */   
/* 10 */   private String start = "<<"; private int version; public String getStart() { return this.start; }
/*    */   
/*    */   private int option;
/*    */   
/*    */   public int getVersion() {
/* 15 */     return this.version;
/*    */   }
/*    */ 
/*    */   
/*    */   public int getOption() {
/* 20 */     return this.option;
/*    */   }
/*    */ 
/*    */ 
/*    */ 
/*    */   
/* 26 */   private String end = ">>"; public String getEnd() { return this.end; }
/*    */ 
/*    */ }


/* Location:              /juyuan-iotlighting-3.8.6/!/com/ruoyi/iotlighting/domain/protocol/ProtocolData.class
 * Java compiler version: 8 (52.0)
 * JD-Core Version:       1.1.3
 */