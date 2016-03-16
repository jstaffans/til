# Ensure JVM refreshes cached IP addresses of AWS resources 

```java
java.security.Security.setProperty("networkaddress.cache.ttl", "60");
```
