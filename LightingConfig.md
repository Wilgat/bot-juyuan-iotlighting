/*    */ package com.ruoyi.iotlighting.domain.protocol;
/*    */ 
/*    */ import com.ruoyi.common.utils.DataUtils;
/*    */ import com.ruoyi.iotlighting.domain.TerInfo;
/*    */ 
/*    */ public class LightingConfig extends ProtocolData {
/*    */   private int lightingCount;
/*    */   private List<TerInfo> terInfoList;
/*    */   
/* 10 */   public void setLightingCount(int lightingCount) { this.lightingCount = lightingCount; } public void setTerInfoList(List<TerInfo> terInfoList) { this.terInfoList = terInfoList; } public boolean equals(Object o) { if (o == this) return true;  if (!(o instanceof LightingConfig)) return false;  LightingConfig other = (LightingConfig)o; if (!other.canEqual(this)) return false;  if (getLightingCount() != other.getLightingCount()) return false;  Object<TerInfo> this$terInfoList = (Object<TerInfo>)getTerInfoList(), other$terInfoList = (Object<TerInfo>)other.getTerInfoList(); return !((this$terInfoList == null) ? (other$terInfoList != null) : !this$terInfoList.equals(other$terInfoList)); } protected boolean canEqual(Object other) { return other instanceof LightingConfig; } public int hashCode() { int PRIME = 59; result = 1; result = result * 59 + getLightingCount(); Object<TerInfo> $terInfoList = (Object<TerInfo>)getTerInfoList(); return result * 59 + (($terInfoList == null) ? 43 : $terInfoList.hashCode()); } public String toString() { return "LightingConfig(lightingCount=" + getLightingCount() + ", terInfoList=" + getTerInfoList() + ")"; }
/*    */ 
/*    */ 
/*    */   
/*    */   public int getLightingCount() {
/* 15 */     return this.lightingCount;
/*    */   }
/*    */ 
/*    */   
/*    */   public List<TerInfo> getTerInfoList() {
/* 20 */     return this.terInfoList;
/*    */   }
/*    */   public String getHexData() {
/* 23 */     StringBuffer sb = new StringBuffer();
/* 24 */     sb.append(DataUtils.string2HexString(getStart()));
/* 25 */     sb.append(DataUtils.intTohex(getVersion()));
/* 26 */     sb.append(DataUtils.intTohex(getOption()));
/* 27 */     if (getLightingCount() <= 255) {
/* 28 */       sb.append(DataUtils.intTohex(0));
/*    */     }
/* 30 */     sb.append(DataUtils.intTohex(getLightingCount()));
/*    */     
/* 32 */     for (TerInfo terInfo : this.terInfoList) {
/* 33 */       sb.append(DataUtils.string2HexString(terInfo.getSn()));
/* 34 */       sb.append(DataUtils.intTohex(1));
/* 35 */       sb.append(DataUtils.intTohex(1));
/* 36 */       sb.append(DataUtils.intTohex(terInfo.getPointX().intValue()));
/* 37 */       sb.append(DataUtils.intTohex(terInfo.getPointY().intValue()));
/*    */     } 
/* 39 */     sb.append(DataUtils.string2HexString(getEnd()));
/* 40 */     return sb.toString();
/*    */   }
/*    */ }


/* Location:              /juyuan-iotlighting-3.8.6/!/com/ruoyi/iotlighting/domain/protocol/LightingConfig.class
 * Java compiler version: 8 (52.0)
 * JD-Core Version:       1.1.3
 */