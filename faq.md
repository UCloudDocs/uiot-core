# 常见问题


1. 请问当前仅对上海区开放吗？

   答：公测期间仅对上海区域开放，其他区域会陆续开放

2. 如何接入IoT-Core平台？

   答：IoT-Core可以帮助物联网设备快速上云。轻松四步即可上云。

	   1）创建产品；

	   2）创建设备；

	   3）移植设备端SDK；

	   4）配置规则引擎流转数据到其他产品；

3. 物联网通信云平台是否收费？

   答：公测期间IoT-Core平台本身的功能免费，规则引擎流转到UCloud的其他产品正常收费。

4. 设备连接时总是不同的重连接，为什么？
 
   答：需要检查下是否同一个设备序列号在多个设备上使用，一个设备会把另一个设备不停的踢下线。
   
5. MQTT的Address、Port、ProductSN、DeviceSN、DeviceSecret都设置正确了，为什么还连不上？

   答：物联网云平台的MQTT broker的心跳时间须在30s-1200s之间，否则会出现连接参数错误。

6. 动态注册之后，我还能通过动态注册获取设备密钥吗？
   
   答：为了安全，动态注册在激活之后不能再通过动态注册获取设备密钥，需要本地做持久化保存。
   
7. MQTT over TLS的CA证书可以只做加密，而不认证吗？

   答：如果使用mbedTLS库，配置接口`mbedtls_ssl_conf_authmode`的认证模式参数`mbedtls_ssl_conf_authmode`从`MBEDTLS_SSL_VERIFY_REQUIRED`改为`MBEDTLS_SSL_VERIFY_NONE`即可跳过认证而仅使用CA证书加密。

8. 如何防止MQTTS的CA证书过期？

   答：基于上述问题7的操作，即可跳过认证而仅使用CA证书加密，即使证书过期也不受影响。
