/*    */ package com.ruoyi.iotlighting.mqtt.config.properties;
/*    */ @Component
/*    */ public class MqttProperties { @Value("${mqtt.username}")
/*    */   private String username;
/*    */   @Value("${mqtt.password}")
/*    */   private String password;
/*    */   @Value("${mqtt.host-url}")
/*    */   private String hostUrl;
/*    */   @Value("${mqtt.in-client-id}")
/*    */   private String inClientId;
/*    */   @Value("${mqtt.out-client-id}")
/*    */   private String outClientId;
/*    */   
/* 14 */   public void setUsername(String username) { this.username = username; } @Value("${mqtt.client-id}") private String clientId; @Value("${mqtt.default-topic}") private String defaultTopic; @Value("${mqtt.timeout}") private int timeout; @Value("${mqtt.keepalive}") private int keepalive; @Value("${mqtt.clearSession}") private boolean clearSession; public void setPassword(String password) { this.password = password; } public void setHostUrl(String hostUrl) { this.hostUrl = hostUrl; } public void setInClientId(String inClientId) { this.inClientId = inClientId; } public void setOutClientId(String outClientId) { this.outClientId = outClientId; } public void setClientId(String clientId) { this.clientId = clientId; } public void setDefaultTopic(String defaultTopic) { this.defaultTopic = defaultTopic; } public void setTimeout(int timeout) { this.timeout = timeout; } public void setKeepalive(int keepalive) { this.keepalive = keepalive; } public void setClearSession(boolean clearSession) { this.clearSession = clearSession; } public boolean equals(Object o) { if (o == this) return true;  if (!(o instanceof MqttProperties)) return false;  MqttProperties other = (MqttProperties)o; if (!other.canEqual(this)) return false;  if (getTimeout() != other.getTimeout()) return false;  if (getKeepalive() != other.getKeepalive()) return false;  if (isClearSession() != other.isClearSession()) return false;  Object this$username = getUsername(), other$username = other.getUsername(); if ((this$username == null) ? (other$username != null) : !this$username.equals(other$username)) return false;  Object this$password = getPassword(), other$password = other.getPassword(); if ((this$password == null) ? (other$password != null) : !this$password.equals(other$password)) return false;  Object this$hostUrl = getHostUrl(), other$hostUrl = other.getHostUrl(); if ((this$hostUrl == null) ? (other$hostUrl != null) : !this$hostUrl.equals(other$hostUrl)) return false;  Object this$inClientId = getInClientId(), other$inClientId = other.getInClientId(); if ((this$inClientId == null) ? (other$inClientId != null) : !this$inClientId.equals(other$inClientId)) return false;  Object this$outClientId = getOutClientId(), other$outClientId = other.getOutClientId(); if ((this$outClientId == null) ? (other$outClientId != null) : !this$outClientId.equals(other$outClientId)) return false;  Object this$clientId = getClientId(), other$clientId = other.getClientId(); if ((this$clientId == null) ? (other$clientId != null) : !this$clientId.equals(other$clientId)) return false;  Object this$defaultTopic = getDefaultTopic(), other$defaultTopic = other.getDefaultTopic(); return !((this$defaultTopic == null) ? (other$defaultTopic != null) : !this$defaultTopic.equals(other$defaultTopic)); } protected boolean canEqual(Object other) { return other instanceof MqttProperties; } public int hashCode() { int PRIME = 59; result = 1; result = result * 59 + getTimeout(); result = result * 59 + getKeepalive(); result = result * 59 + (isClearSession() ? 79 : 97); Object $username = getUsername(); result = result * 59 + (($username == null) ? 43 : $username.hashCode()); Object $password = getPassword(); result = result * 59 + (($password == null) ? 43 : $password.hashCode()); Object $hostUrl = getHostUrl(); result = result * 59 + (($hostUrl == null) ? 43 : $hostUrl.hashCode()); Object $inClientId = getInClientId(); result = result * 59 + (($inClientId == null) ? 43 : $inClientId.hashCode()); Object $outClientId = getOutClientId(); result = result * 59 + (($outClientId == null) ? 43 : $outClientId.hashCode()); Object $clientId = getClientId(); result = result * 59 + (($clientId == null) ? 43 : $clientId.hashCode()); Object $defaultTopic = getDefaultTopic(); return result * 59 + (($defaultTopic == null) ? 43 : $defaultTopic.hashCode()); } public String toString() { return "MqttProperties(username=" + getUsername() + ", password=" + getPassword() + ", hostUrl=" + getHostUrl() + ", inClientId=" + getInClientId() + ", outClientId=" + getOutClientId() + ", clientId=" + getClientId() + ", defaultTopic=" + getDefaultTopic() + ", timeout=" + getTimeout() + ", keepalive=" + getKeepalive() + ", clearSession=" + isClearSession() + ")"; }
/*    */ 
/*    */ 
/*    */ 
/*    */ 
/*    */   
/*    */   public String getUsername() {
/* 21 */     return this.username;
/*    */   }
/*    */ 
/*    */ 
/*    */   
/*    */   public String getPassword() {
/* 27 */     return this.password;
/*    */   }
/*    */ 
/*    */ 
/*    */   
/*    */   public String getHostUrl() {
/* 33 */     return this.hostUrl;
/*    */   }
/*    */ 
/*    */ 
/*    */   
/*    */   public String getInClientId() {
/* 39 */     return this.inClientId;
/*    */   }
/*    */ 
/*    */ 
/*    */   
/*    */   public String getOutClientId() {
/* 45 */     return this.outClientId;
/*    */   }
/*    */ 
/*    */ 
/*    */   
/*    */   public String getClientId() {
/* 51 */     return this.clientId;
/*    */   }
/*    */ 
/*    */ 
/*    */   
/*    */   public String getDefaultTopic() {
/* 57 */     return this.defaultTopic;
/*    */   }
/*    */ 
/*    */ 
/*    */   
/*    */   public int getTimeout() {
/* 63 */     return this.timeout;
/*    */   }
/*    */ 
/*    */ 
/*    */   
/*    */   public int getKeepalive() {
/* 69 */     return this.keepalive;
/*    */   }
/*    */   
/*    */   public boolean isClearSession() {
/* 73 */     return this.clearSession;
/*    */   } }


/* Location:              /juyuan-iotlighting-3.8.6/!/com/ruoyi/iotlighting/mqtt/config/properties/MqttProperties.class
 * Java compiler version: 8 (52.0)
 * JD-Core Version:       1.1.3
 */