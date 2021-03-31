## 面试

1. 自我介绍

2. 项目简要介绍

3. 多进程，多线程，协程了解多少，具体应用场景

2. 多线程之间用锁是干什么

3. 乐观锁，悲观锁

4. 有了乐观锁，为什么还要悲观锁

5.  了解常见http的攻击吗？比如sql注入，XSS

6. 路由器，交换机，网桥在哪一层？

7. 路由器，交换机有什么作用

8. 路由协议OSPF具体是干什么

## 笔试题

1. sql题

   给定blog表

   id，content，author，create_time

   按照create_time做分页查找，先建索引再查找。

```
alter table blog add index timeAsc(create_time asc);
select *
from blog
order by create_time desc
limit 5 offset 5;
```

​	小坑：limit 5 offset 5要写在最后面，会依赖

​	面试官：如果有一亿条数据，offset到7千万，会出现什么问题

​	我：会扫索引扫到七千万

​	面试官：应该会扫全表

2. #### [两两交换链表中的节点](https://leetcode-cn.com/problems/swap-nodes-in-pairs/)