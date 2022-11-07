# 文档
1. MySQL Document: https://dev.mysql.com/doc/
2. MySQL Reference Manual: https://dev.mysql.com/doc/refman/8.0/en/
3. MySQL Tutorial: https://dev.mysql.com/doc/refman/8.0/en/tutorial.html

# 文档导航
- [Chapter 5 MySQL Server Administration](https://dev.mysql.com/doc/refman/8.0/en/server-administration.html)
  - [5.1 The MySQL Server](https://dev.mysql.com/doc/refman/8.0/en/mysqld-server.html)
    - [5.1.8 Server System Variables](https://dev.mysql.com/doc/refman/8.0/en/server-system-variables.html)
  - [5.2 The MySQL Data Directory](https://dev.mysql.com/doc/refman/8.0/en/data-directory.html)
- [Chapter 6 Security](https://dev.mysql.com/doc/refman/8.0/en/security.html)
- [Chapter 15 The InnoDB Storage Engine](https://dev.mysql.com/doc/refman/8.0/en/innodb-storage-engine.html)
  - [15.14 InnoDB Startup Options and System Variables](https://dev.mysql.com/doc/refman/8.0/en/innodb-parameters.html)
# 事务
## 文档
1. Transactional and Locking Statements: https://dev.mysql.com/doc/refman/8.0/en/sql-transactional-statements.html
2. Server System Variables autocommit: https://dev.mysql.com/doc/refman/8.0/en/server-system-variables.html#sysvar_autocommit ，取值：ON、OFF
3. Server System Variables transaction_isolation: https://dev.mysql.com/doc/refman/8.0/en/server-system-variables.html#sysvar_transaction_isolation ，取值：READ-UNCOMMITTED、READ-COMMITTED、REPEATABLE-READ、SERIALIZABLE
## 常见操作
### 自动提交
1. 查询事务自动提交配置：
```sql
show variables like 'autocommit';
```
2. 更新事务自动提交配置：
```sql
# Session Scope
SET autocommit=ON;
SET autocommit=OFF;
# Global Scope
```
### 隔离级别
1. 查询事务隔离级别：
```sql
show variables like 'transaction_isolation';
```
2. 更新事务隔离级别：
```sql
# Session Scope
SET @@SESSION.transaction_isolation = 'READ-COMMITTED';
SET SESSION transaction_isolation = 'READ-COMMITTED';
SET transaction_isolation = 'READ-COMMITTED';
SET @@transaction_isolation = 'READ-COMMITTED'; # set the next-transaction isolation level
# Global Scope
SET GLOBAL transaction_isolation = 'READ-COMMITTED';
```
# 工具
1. InnoDB 数据结构可视化：https://github.com/jeremycole/innodb_diagrams
