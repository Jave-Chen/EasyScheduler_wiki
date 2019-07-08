# FAQ



## V1.0.4

**Q: worker 和 master 自动结束，会有什么原因？**

A:

```shell
Unable to read additional data from server sessionid 0x16a2
ecfc248014e, likely server has closed socket, closing socket connection and attempting reconnect
org.apache.zookeeper.ClientCnxn:[1162] - Session 0x16a2ecfc2480151 for server null, unexpected error
, closing socket connection and attempting reconnect
```

如 worker 和 master 连接 zk 失败，master 和 worker 就会自动退出，报错如上。



---

**Q: 安装以后，如何修改 zk 配置？**

A: 修改对应节点 `conf/zookeeper.properties` 文件中对应的值，重启 master/worker 即可。



---

**Q:ubuntu 下安装报错，如何解决？**

A: ubuntu 用 `sudo bash install.sh`



------

**Q: 关闭  alert 服务后，为什么 sql 任务日志还是有告警错误？**

A: sql 任务，流程告警，容错都会走邮件。