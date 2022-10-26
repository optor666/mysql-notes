# 文档
1. MySQL Document: https://dev.mysql.com/doc/
2. MySQL Reference Manual: https://dev.mysql.com/doc/refman/8.0/en/
3. MySQL Tutorial: https://dev.mysql.com/doc/refman/8.0/en/tutorial.html
# 事务
## 文档
1. Transactional and Locking Statements: https://dev.mysql.com/doc/refman/8.0/en/sql-transactional-statements.html
2. Server System Variables autocommit: https://dev.mysql.com/doc/refman/8.0/en/server-system-variables.html#sysvar_autocommit
## 常见操作
### 自动提交
1. 查询事务自动提交配置：
```sql
show variables like 'autocommit';
```
2. 更新事务自动提交配置：
```sql
SET autocommit=ON;
SET autocommit=OFF;
```
3. todo
### 隔离级别
1. 查询事务隔离级别：
```sql
show variables like 'transaction_isolation';
```
2. 更新事务隔离级别：
