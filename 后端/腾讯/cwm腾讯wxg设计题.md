## 腾讯二面

* 生成不重复的ID，考虑多台机器的情况

  SnowFlake（64bit）

* 如果考虑32bit呢

  考虑每台机器被分配一段ID，如果用完申请新段

* UDP传输HTTP的优势

  QUIC 

* 然后各种引导

  在移动端弱网环境下，基站的切换会导致TCP连接中断，UDP无连接，不会再有TCP的连接重建立过程，直接可以广播到终端

## 腾讯三面

* 微博大V和粉丝架构

* 微信朋友圈架构

* 考虑微信用户每个人都做了新冠检测，然后在某个同一时间点在微信发布结果，同时查询自己的结果，同时显示自己的朋友感染新冠的名单，怎么做架构

  我先答了个做预处理，把朋友关系这些都预处理出来，到时候只做显示，然后他问我有什么数据结构，我说不知道，然后他说可以布隆过滤器，后来他还问有没有其他的，引导了下之后我打了个bitmap