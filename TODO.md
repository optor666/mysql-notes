1. binlog, redolog 两阶段提交？
2. MySQL WAL(Write Ahead Log)?
3. 视图？
4. 多版本并发控制 MVCC
5. 四种事务隔离级别的实现方式？
6. 索引结构：哈希、有序数组、二叉树、多叉树、跳表、LSM 树
7. 索引类型：主键索引、非主键索引、覆盖索引
8. 主键索引的叶子节点存的是整行数据。在 InnoDB 中，主键索引也被称为聚簇索引（clustered index）；
9. 非主键索引的叶子节点内容是主键的值。在 InnoDB 中，非主键索引也被称为二级索引（secondary index）；需要多扫描一颗索引树。
10. general_log 
11. 锁：全局锁（主要用于逻辑备份）、表锁、行锁、元数据锁（MDL）
12. MySQL MRR 优化：https://zhuanlan.zhihu.com/p/110154066
13. 两阶段协议、死锁、死锁检测
