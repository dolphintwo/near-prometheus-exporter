# Grafana设置阀值告警

我们可以在grafana上设置针对哪些监控的项目设置告警阀值，下面以几个常见的为示例：

1. CPU负载超过80%
![](./img/cpu_alert.jpeg?raw=true)


2. 内存占用超过801%
![](./img/memory_alert.jpg?raw=true)


3. 出块率低于91%
![](./img/block_alert.jpg?raw=true)


4. 节点连接数少于10
![](./img/peers_alert.jpg?raw=true)


5. 是否是验证者状态
![](./img/is_validator_alert.jpg?raw=true)


6. 节点是否需要升级
![](./img/upgrade_alert.jpg?raw=true)


# 测试CPU过载能否发送告警邮件
下面我们配置下告警的邮箱然后实际测试能否如预期工作：

按照如下方式配置完邮件地址
![](./img/set_email.png?raw=true)

实际压力测试下cpu，看看是否会收到邮件。下面是收到的邮件示例图。

告警邮件，CPU负载过高。
![](./img/alert_email.jpeg?raw=true)

CPU恢复正常邮件。
![](./img/ok_email.jpeg?raw=true)

对应于实际的CPU负载曲线如下：
![](./img/cpu_alert.jpeg?raw=true)