## 事务
### 事务的acid
### 事务的4种隔离级别/并发控制
数据库事务的隔离级别有4种，由低到高分别为Read uncommitted 、Read committed 、Repeatable read 、Serializable 。而且，在事务的并发操作中可能会出现脏读，不可重复读，幻读。

脏读：读未提交事务的数据

不可重复读：一个事务范围内两个相同的查询却返回了不同数据

https://www.cnblogs.com/3013218061shang/p/5573476.html