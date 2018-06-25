# go-push

用GO做推送

# arch

* gateway: 长连接网关
    * BUCKET: 海量长连接按BUCKET打散, 减小推送遍历的锁粒度
    * MERGE: 按广播/房间粒度的消息前置合并, 减少编码CPU损耗, 减少系统网络调用, 巨幅提升吞吐
* logic: 逻辑服务器