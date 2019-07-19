{{indexmenu_n>3}}

# 使用限制(这里待定修改)

| 类别                                   | 描述                                                         | 限制                           | 备注 |
| -------------------------------------- | ------------------------------------------------------------ | ------------------------------ | ---- |
| 产品数量                               | 单账号最多可以创建的产品数。                                 | 100                            |      |
| 设备数量                               | 单产品最多可以添加的设备数。                                 | 10,000                         |      |
| 物模型功能定义                         | 单个产品最多可添加的属性数。                                 | 100                            |      |
| 物模型功能定义                         | 单个产品最多可添加的事件数。                                 | 100                            |      |
| 物模型功能定义                         | 单个产品最多可添加的命令数。                                 | 100                            |      |
| 物模型功能定义                         | 当功能的数据类型：<br>为enum时，枚举项最多不超过25个。<br>为string时，数据长度不超过2048字节。<br> |                                |      |
| 物模型功能定义                         | 命令中可添加的入参和出参分别不超过20个。                     | 20                             |      |
| 物模型功能定义                         | 事件中可添加的出参不超过20个。                               | 20                             |      |
| OTA                                    | 文件大小上限                                                 | 20M                            |      |
| 连接通信                               | 单设备每分钟最大连接次数。                                   | 5                              | 待定 |
| 连接通信                               | 单设备的最大订阅数。<br>超过订阅数的请求将会被直接拒绝。设备端可以通过验证SUBACK消息，确认请求是否成功。 | 100                            | 待定 |
| 连接通信                               | 单设备上报上限QoS0为30条/秒，QoS1为10条/秒。<br>说明 MQTT的Pub上报消息限流，协议上没有任何应答。您可以通过日志服务发现设备被限流的警告。 | QoS0：30条/秒<br>QoS1：10条/秒 | 待定 |
| 连接通信                               | 单设备下行接收限制为50条/秒，同时受限于网络环境。<br>如果网络tcp write buffer拥堵，将直接返回错误。比如，您通过Pub接口发指令给设备，如果设备接收不过来，将收到限流错误。 | 50条/秒                        | 待定 |
| 连接通信                               | 单个连接每秒的吞吐量（带宽）。                               | 1024 KB                        | 待定 |
| 连接通信                               | QoS1消息的最大存储时间。<br>如果最大时间后未从客户端接收到 PUBACK 消息，则会丢弃这些发布请求。 | 7天                            | 待定 |
| 连接通信                               | MQTT报文最大长度                                             | 2MB                            |      |
| 连接通信                               | MQTT连接心跳时间为30至1200秒。心跳时间不在此区间内，服务器将会拒绝连接。<br>建议取值300秒以上。<br>从IoT发送CONNACK响应CONNECT消息时，开始心跳计时。收到PUBLISH、SUBSCRIBE、PING、或 PUBACK消息时，会重置计时器。超过指定1.5倍心跳时间间隔未收到这些消息时（指定心跳时间乘以1.5），将自动断开连接。 | 30-1200秒                      | 待定 |
| Topic                                  | 一个产品最多可以定义50个Topic类。                            | 50                             |      |
| Topic                                  | 设备只能对自己的Topic进行消息发布与订阅。                    | -                              |      |
| Topic                                  | Topic长度不能超过128字节， UTF-8 编码字符。                  | 128字节                        |      |
| Topic                                  | Topic中斜杠的最大数量。                                      | 7                              |      |
| Topic                                  | 每个订阅请求的最大订阅数。                                   | 8                              | 待定 |
| Topic                                  | 广播Topic，同一个Topic最多可以被1000个设备订阅，服务端SDK每秒只可发一条广播。 | 1000                           | 待定 |
| 设备影子                               | 设备影子JSON文档的最大深度。                                 | 5                              | 待定 |
| 规则引擎                               | 账号最多可以设置100条规则。<br>一条规则中转发数据的操作不能超过10个。                                  | 100                            |      |
| API                                    | QPS                                                          |                                | 待定 |