# Summary

* [Introduction](README.md)
* [1 系统设计](1-xi-tong-she-ji.md)
  * [1.1 部署图](11-bu-shu-tu.md)
  * [1.2 点对点发送消息的流程](12-dian-dui-dian-fa-song-xiao-xi-de-liu-cheng.md)
  * [1.3 消息的存储结构](13-xiao-xi-de-cun-chu-jie-gou.md)
* [2 存储服务器](2-cun-chu-fu-wu-qi.md)
  * [2.1 rpc 接口](21-rpc-jie-kou.md)
    * [2.1.1 点对点获取同步的消息](21-rpc-jie-kou/211-dian-dui-dian-huo-qu-tong-bu-de-xiao-xi.md)
    * [2.1.2 获取群组的同步消息](21-rpc-jie-kou/212-huo-qu-qun-zu-de-tong-bu-xiao-xi.md)
    * [2.1.3 保存点对点的消息](21-rpc-jie-kou/213-bao-cun-dian-dui-dian-de-xiao-xi.md)
    * [2.1.4 保存发送到群组的消息](21-rpc-jie-kou/214-bao-cun-fa-song-dao-qun-zu-de-xiao-xi.md)
* [3 路由服务器](3-lu-you-fu-wu-qi.md)
* [4 接入服务器](4-jie-ru-fu-wu-qi.md)
  * [4.1 消息存入redis](4-jie-ru-fu-wu-qi/41-xiao-xi-cun-ru-redis.md)
  * [4.2 从redis中查找消息](4-jie-ru-fu-wu-qi/42-cong-redis-zhong-cha-zhao-xiao-xi.md)
* [5  通知服务器](5-tong-zhi-fu-wu-qi.md)
  * [5.1 通讯协议](5-tong-zhi-fu-wu-qi/51-tong-xun-xie-yi.md)
    * [5.1.1 心跳协议](5-tong-zhi-fu-wu-qi/51-tong-xun-xie-yi/511-xin-tiao-xie-yi.md)
    * [5.1.2 点对点的同步通知](5-tong-zhi-fu-wu-qi/51-tong-xun-xie-yi/512-dian-dui-dian-de-tong-bu-tong-zhi.md)
    * [5.1.3 点对点的同步通知带数据](5-tong-zhi-fu-wu-qi/51-tong-xun-xie-yi/513-dian-dui-dian-de-tong-bu-tong-zhi-dai-shu-ju.md)
    * [5.1.4 群组同步通知](5-tong-zhi-fu-wu-qi/514-qun-zu-tong-bu-tong-zhi.md)
* [6 imsdk](6-imsdk.md)
* [7 im管理服务器qim](7-imguan-lifu-wu-qi-qim.md)



