# navicat
# 约束
- 主键(primary key)
- 主键自增auto_increment
- 外键(foreign key)--链接表格的主键 ` foreign () references <表><列名>`
- 唯一约束(UNIQUE)
- 检查约束(CHECK(...>...|...<...))
- 默认值(DEFAULT)
- 非空约束(NOT NULL)
# 数据库
## 创建仓库

```MySQL
CREATE DATABASE <`数据库名`>&&防止和关键词重复;
```

## 删除数据库

```MySQL
drop database <`数据库名`>;
```

## 选择数据库

```MySQL
use <数据库名>;
```

# 数据表

## 创建数据表

```MySQL
CREATE TABLE <`表名`> (列名 列数据类型);
CREATE TABLE `USER`(
	`USER_ID` INT AUTO_INCREMENT [PRIMARY KEY],
	`USER_NAME` VARCHAR(20) NOT NULL,
	[PRIMARY KEY (`USER_ID`)]
	unique [index(``)]
)[ENGINE=INNODB DEFAULT CHARSET=UTF8;]
```

## 删除数据表

```MySQL
drop table <`数据表名`>
```

#### 转移数据表

```MySQL
rename <db1>.<表名> to <db2>.<表名>
```

## 查看表结构

```MySQL
DESCRIBE(desc简略) <表名>
```

## 修改数据表的属性

```MySQL
ALTER TABLE <表名> 
[选项]
	-ADD COLUMN <[foreign key] (列名)> <类型> [first|after <列名>]
	-CHANGE COLUMN <旧列名> <新列名> <类型>
	-ALTER COLUMN <列名> {set default <值>|drop default}
	-MODIFY <列名> <新类型>
	-DROP COLUMN <列名>
	-RENAME TO <表名>
```

## 添加数据

```MySQL
INSERT INTO <`表名`> [（`列名`）] VLUES [（值1,值2...）] 
INSERT INTO <`表名`> SET <列名>=<值> <列名>=<值>
```

## 查询数据
```MySQL
SELECT [功能] <列名|*> FROM <表名> [约束]
[约束]
	-ORDER BY <列名> ASC|DESC
	-GROUP BY <列名> 
	-LIMIT <行数>
[功能]
	-DISTINCT 去重
	-
union|union all 将两个表格的查询结果合并输出
正则
regexp
```

###### 内联查询

```MySQL
join
SELECT <a.列名> <b.列名> FROM <表名 a> INNER JOIN <表名 b> [ON a.  =b. ]&&交集
SELECT <a.列名> <b.列名> FROM <表名 a> LEFT JOIN <表名 b> [ON a.  =b. ]&& a
SELECT <a.列名> <b.列名> FROM <表名 a> RIGHT JOIN <表名 b> [ON a.  =b. ]&& b
```

## 修改数据

```MySQL
UPDATE <表名> SET [<列名>=<值>]，+ [WHERE <列名>=<值> ]
DELETE FROM <表名> [WHERE]
TRUNCATE <表名>
AS 别名
//
on deleter casecade
```

# 索引

```MySQL
CREATE INDEX <indexName> ON <表名><列名>
show  index from <>
drop index <>
```

#### where&&having(having 查询后再过滤，where全局过滤)
#### OR && NOT && AND && IN/EXISTS && BETWEEN  AND && IS[NOT]NULL

# LIKE 

```MySQL
%:任意(多个)字符
_:字符
[a-zA-Z]:包含
[^a]:不包含a
```


# 功能函数

```MySQL
数字函数
	count()&&数据总数
	avg()&&平均值
	sum()&&总和
	max()&&最大
	min()&&最小
```

# 事务

```MySQL
SET AUTOCOMMIT =0;
(START TRANSACTION)
语句1；
...;
commit;提交
rollback;回滚
```

# 视图

```MySQL
%%创建
create view <viewname>
as
select ....

&&修改
create or replace view <viewname>
as
查询语句
//
alter view <>
as
查询语句

&&删除
drop view <viewname>
```

# 存储过程/函数
```MySQL
delimiter $结束标记
&&
in输入值|out返回值|inout
&&
create procedure <name>(IN <> INT)
begin
函数体
end $
call <名>(参数)$
drop procedure <name>
show create procedure <名字>
&&

create function <name([a int]) > returns <int>
begin
declare <c> int;
	函数体
	return <c>;
end $

&&调用
select <函数名>$
DROP FUNCTION <name1>,<name2>
show create function <>
```

# 变量

```MySQL
show global|session variables [like '']
select @@global.|@@session.
set @@global[.] =''|
set @@|session<变量>=<>
&&
set @用户变量名[:]=值|select @用户变量名：=值
&&局部再begin end中
declare 变量名 类型
set [@]局部变量名[:]=值

```

# 判断
```MySQL
if(表达式1，表达式2，表达式3)
&&
case(e)
when 'a' then 值;
else 值;
end case;
&&
while 判断 do 
     语句
end while;
```