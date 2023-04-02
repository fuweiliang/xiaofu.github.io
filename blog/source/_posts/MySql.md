---
title: MySql学习笔记
date: 2023-03-23 18:58:56
tags:
cover: https://labs.mysql.com/common/themes/sakila/banners/b1280-mysql-mds-aws-azure5.en.jpg
---
1.登录
2.USE db_name(数据库名称);
CREATE TABLE tb_name(
定义字段 字段名 数据类型 是否为空 是否主键，
字段2，
字段3，
....
);
4.查看表的基本结构 ①DESC tb_name;
②SHOW COLUMNS FROM tb_name;
5.查看创建表的详细结构 SHOW CREATE TABLE tb_name;
6.查看数据库中的所有表格 SHOW TABLES;
7.查看所有数据库 SHOW DATABASES;
8.删除表 DROP TABLE tb_name;
9.删除数据库 DROP DATABASES DB_NAME;
10.创建数据库 CREATE DATABASES db_anme;
11.exit
12 修改 ALTER
添加列 ALTER TABLE tb_name ADD COLUMN 字段名 数据类型 是否为空 FIRST(位置第一)
AFTER 字段名 （位于某字段之后)/(加在最后)
13.修改列默认值 ALTER TABLE tb_name
ALTER col_name(字段)SET DEFAULT 值；设置默认值
删除默认值 ALTER TABLE tb_name
ALTER COL_NAME DROP DEFAULT;
给student表添加3个字段

s_hobby 放在s_grade的前面，并设置默认值弹钢琴

s_height

s_class 放第一，并设置默认值 大数据1班
14.字段重命名 ALTER TABLE tb_name
CHANGE old_col_name new_col_name 数据类型(保持不变/新的数据类型)[DEFAULT 值][FIRST/AFTER col_name]];
15.删除字段   ALTER TABLE tb_name
DROP col_name;
16.修改字段数据类型 ALTER tb_name
MODIFY col_name 新的数据类型；
17.重命名表 ①ALTER TABLE tb_name
RENAME new_tb_name;
②RENAME tb_name TO new_tb_name;
数据完整性约束（行完整性）
PRIMARY KEY 主键约束
unique 唯一性约束 保证字段值不重复，唯一

可以直接定义一个完整约束性
CONSTEAINT abc （唯一的）（自己取的名字）
primary key（）
foreign key（）
unique（）
check
not null

共同点：都不允许字段值重复 完整性约束
区别：①一张表只允许有一个primary key 约束，unique可以多个
②主键字段not null,unique 允许null
③自动产生相应索引

	student id 主键约束  null  X 2
		name 			unqiue null 
		sex			男
		grade 		90 	unique

2．参照完整性
参照完整性保证被参照表中的数据与参照表中数据的一致性，又称为引用完整性，参照完整性确保键值在所有表中一致，通过定义主键(PRIMARY KEY)与外键(FOREIGN KEY)之间的对应关系实现参照完整性。
primary key
forign key 外键
需要i满足的要求
①产招标不引用不存在的值
②值得改变会影响（2张表，一张鼠标表 ，另一张也变）
③删除操作互相影响
例如，将教师表teacher作为被参照表、表中的teacherno列作为主键，讲课表lecture作为参照表、表中的teacherno列作为外键，从而建立起被参照表与参照表之间的联系以实现参照完整性，teacher和lecture的对应关系如图3.1所示。

3.用户定义的完整性约束
数据输入的过程检查列数据输入的有效性
check约束
not null约束 非空约束

4.完整性约束 表上强制性执行的一些数据校验规则
primary key
forign key
unique
check
boe null

5 	1一个
完整性约束
constraint abc(唯一的)(自取的名字)
primary key ()
forign key()
unique()
check
not null

完整性约束 定义（创建）
constarint  名称 （可自定义/自动生成）
primary key(字段名)
unqiue(字段名）
check(约束条件）
forign key (列明）

定义完整性约束，到底定义几个约束
CONSTRAINT pk_taxt3 PRIMARY KEY(id));
定义一个叫pk_text3的完整性约束。
此完整性约束仅存在主键完整性约束
删除完整性 DROP
ALTER TABLE tb_name DROP  PRIMARY KEY;
添加完整新约束 ADD
ALTER TABLE tb_name ADD CONSTRAINT
约束名 PRIMARY KEY
unique 唯一性约束
值必须唯一 ，允许null
一张表 可以iy有一个或者多个唯一性约束
分为 列级 表级 约束
列级写法 字段名数据类型（not null)unique
列子：name char(8) unqiue,
表级写法 定义完所有字段后unique(字段名）
例子：，UNIQUE(ID)
定义一个专属UNIQUE的完整性约束的写法
定义完所有字段后 ，CONSTRAINT约束名unique (字段名）
unique
唯一性约束的删除：DROP
ALTER TABLE tb_name DROP INDEX 约束名；
例子：ALTE TABLE text6 DROP INDEX  uk6;删除表text6的唯一约束uk6

唯一性约束的添加：ADD
ALTER TABLE tb_name ADD CONSTRAINT 约束名 	UNIQUE(字段名）
例子:ALTER TABLE text6 ADD COMNSTRAINT uk7 UNIQUE(name)
给表text6添加一个叫uk7的唯一性约束，约束字段name.
外键约束 FOREIGN KEY
作用：保证参照表和被参照表得数据一致
外键：可以是一列或者多列得组合
1：主键是id
2：外键是id(一列)
!:主键PRIMARY KEY（id sno)2:外键id sno(多列)
参照表
定义外键的规则：
1.被参照表已创建（CREATE TABLE）
2.外键必须是被参照表的主键
3.被参照表必须定义好主键和唯一性约束
4.主键不能是null，外键中允许
5.外键字段数必须和主键相同
6.主键和外键的数据类型必须相同
在创表时定义外键约束：
teacher pk:teacherno
teacher1 fk:teacherno
leture1 primary(teacherno,chourseno)复合型主键
foreign(teacherno)外键
(teachno)不等于（teacherno,courseno)
复合型主键：数据绝对不出错，不会产生对应错误
任何一个单独拿出来都是可以当主键。都是独一

为参照指定动作（限制）
1.ON DELLTE CASCDE|RESTRICT
(级联策略)(限制策略)
C:被参照表执行删除操作，参照表也跟着删除
R:限制删除操作
2.ON UPDATA RESTRICT|CASCADE
C:
R:

表级定义来定义外键
定义参照动作 delete update

删除外键约束
ALTER TBALE tb_name DROP FOREIGN KEY 约束名；

增加 ADD
ALTER TABLE tb_name ADD CONSTRAINT 约束名 FOREIGN KEY (外键） REFERENCES tb(被参照表） name(主键); 外键和主键必须保持一致
数目、数据类型均一致
检查约束 check
实现用户定义的完整性 检查值设置的对不对，不符合，不允许输入值。

CONSTRAINT 约束名CHECK（约束条件）

添加
ALTER TABLE scorel ADD CONSTRAINT ck1 CHECK(grade>=0 AND grade<=100);
删除
ALTER TABLE scorel DROP CHECK ck1;
1

第三章小结：
1.数据定义语言 DDl：CREATE ALTER DROP
2.创建数据库 CREATE DATABASE[IF NOT EXISTS]db_name;
3.使用数据库 use db_name;
4.删除数据库 DROP DB_NAME;
5.创建表格 CREATE TABLE tb_name(定义字段 ，字段用逗号隔开）；
①给现成的表，仿照：分析表结构 包含哪些字段，字段什么数据类型 表明还是什么...
什么是表结构？p53
②只给要求，自行创表。按要求的字段和数据类型写
6.复制表结构，不复制数据


9.查看表的详细结构：SHOW CREATE TABLE tb_name;
10.修改表：添加列 ADD ALTER TABLE tb_name ADD
修改默认值：SET DEFAULT/DROP DEFAULT
列重命名：CHANGE
删除列 ：DROP
重命名表格：RENAME TO\RENAMETABLE
删除表：DROP TABLE

11.数据完整性约束
实体完整性PRIMARY KEY\UNIQUE
参照完整性 PRIMARY KEY\FOREIGE KEY(定义动作)
自定义
数据完整性约束CHECK\NOT NULL
表级写法 列级写法！！！ CONSTRAINT约束名

(1)INSERT 语句，用于将数据插入或视图中
(2)UPDATE 语句，用于修改表或视图中的数据，即可修改表或视图中的一行数据，（也可以修改表或视图中）一组或全部数据
(3)DELETE 语句，用于从表或视图中删除数据，可根据条件指定数据

插入数据：
①所有字段都放数据
INSERT INTO tb_name VALUES(数据类型必须和结构图一致，顺序一致)；
②选取部分字段的数据(要赋值的字段)values (数据顺序和前面的括号里一致。类型要写对)

插入多条记录
插入多条记录时，再插入语句中，只能指定多个插入值列表，插入值列表之间插入值用逗号隔开

复制表的数据：
INSERT INTO new tb_name SELECT*FROM old_tb_name;
①两表结构一致  ②复制的是旧表的所有数据

INSERT INTO new_tb(column字段名）
SELECT(字段名)FROM old_tb[WHERE查询条件];
①两表只有部分字段一致（名称和数据类型一致）
②查询条件 根据实际情况填写。


使用UPDATE语句修改数据
修改表中的一行或多行记录的列值使用UPDATE语句。语法格式如下。
UPDATE table_name
SET columnl=value1[, column2=value2,.][WHEREcondition >]
说明如下。
( 1)SET子句
用于指定表中要修改的列名及其值，column
1, column2,..为指定修改的列名，value1, value2,...为相应的指定列修改后的值。

(2 ) WHERE子句:用于限定表中要修改的行，condition指

定要修改的行满足的条件，若语句中不指定WHERE子句，则修改

所有行。

4.4使用DELETE语句删除数据
删除表中的一行或多行记录使用DELETE语句。
语法格式如下。
DELETE FROM table_name[WHERE<condition >]
其中，table_name是要删除数据的表名，WHERE子句是可选项，用于指定表中要删除的行，condition指定删除条件，若省略WHERE子句，则删除所有行。

2.TRANCATE
语句
语法格式如下
TRUNCATE [TABLEJ
table_name
其中，table_name是要删除全部数据的表名。【例4.11】在student表中，删除所有行。mysql> TRUNCATE student;
执行速度比DELETE更快
使用SELECT语句进行查询。
mysql> SELECT * FROM student;查询结果如下。
Empty set (0.01 sec)
·
select字句用于选择列，选择列称为投影查询
select distinct列明或表达式
其中如果没有指定这些选项则默认是all即返回操作所有行过阔可能存在的重复行
如果指定distinct则清楚集合重复行
1.投影指定列
列子：selectteacher弄，同色系，title from teacher;
2.投影全部列·
select*from teacher;
3.修改查询结果的列标题
select ...列名[as列明]
4.计算列值
select子句对列进行查询可以使用加减乘除
算术运算对数字类型的列及进行计算
：select子句语法2
select<表达式>[,<表达式>]
去掉重复行
可以使用关键字DISTINCT 语法格式如下
select distincttitle from teacher;
5.22
where子句条件
条件：<判定条件>[逻辑运算符<判定条件>]
表达式not like表达式
表达式BETWEEN 表达式AND表达式

空值判断
判断一个表达式是否为空时是圆通is null关键字
语法格式如下
<表达式>is [not ]null

4.使用like关键字的字符匹配查询
在使用like关键字时，可以含有通配符，通配符有以下两种：
%:代表0或多个字符
——：代表一个字符
like匹配中使用通配符查询也称【模糊查询】
select子句where某字段like%/-(看情况)

GROUP子句和HAVING子句
聚合函数
聚合函数的统计计算用于计算表中的数据返回单个计算结果2，聚合函数包裹count,sun avg max

COUNT函数用于对计算组中曼珠条件或总函数

all表示对所有值进行计算，



sum/avg[all|disnct<表达式>]

3.HAVING 语法having实在group by 之后的进一步筛选
having子句用于对分组按指定条件进步一部筛选，过滤出满足指定条件的分组

/*
DQL-执行顺序
SELECT
4
字段列表
FROM   
1
表名列表
WHERE 在表中选择行
2
条件列表
GROUP BY  对选取行进行分组
3
分组字段列表
HAVING  筛选满足条件的分组
分组后条件列表
ORDER BY  进行排序
5
排序字段列表
LIMIT
6
分页参数

*/
order by 子句 和limit 子句
1.排序查询
order by 子句对拆寻结果进行排序，语法格式如下。
其中，排序表达式可以是列明，表达式或者一个正整数，asc表示升序排列，系统默认排序asc ，desc表示降序排序。

offset:位置偏移量，指示从那一行开始显示，第一行偏移量是0，第二行的位置偏移量是1，以此类推，如果不置顶位置偏移量和，系统从表中第一行开始显示
（20）row_coun:返回的行数
limit子句有两种v语法例如显示表中第二行到底四行可写为limit 3 offset 1。

5.3.1连接查询
1.交叉查询
交叉查询(cross join) 又称笛卡尔积，有第一个表的每一行与第二与第二个表的每一行链接形成的是表，语法格式如下
seect*from table cross join table 2; 或 select *from table,table2;
2.内连接
内连接使用的比较运算符进行标间某些字段值的比较操作，并将于连接条件相匹配的数据行组成新纪录，以消除交叉连接中没有意义的数据航行
内连接有两种链接方式：
第一种：使用inner join 定义连接条件的显示语法结构
语法格式如下select 目标列表达式1目标列表达式2 目标列表达式n；
from tbalel [innor] join table2 on 链接条件
[where 过滤条件]
第二种：使用where字句定义练肌肉条件的隐式语法结构
语法结构
select 目标表达式1，目标表达式2  .....目标表达式n from table,table2 where 连接条件 [and过滤条件]  
3.第二种
使用where子句定义连接条件的隐式语法结构。
语法格式如下
select 目标表达式1，目标表达式2  .....目标表达式n from table ,table2  where 链接条件[and过滤条件]
4.自然连接
nature join 自然连接关键词
select * from student NATURAL join speciality;
将某个表与自身进行链接，称为子表链接或自身链接，简称自来凝结，使用自链接需要为表多个别名，且对所有查询字段的引用必须使用表别名限定
5.外连接在内连接的结果表，只有满足连接条件的行才能作为结果输出。外连接的结果表不但包含满足连接条件的行还包括相应表中的所有行。
左外连接：结果表除了包括满足链接条件的行外，还包括坐标的所有行，当坐标有记录而在右表中没有匹配记录，在表对应列被摄值为空值null

右外连接：遇上相反·
普通字查询
执行的顺序是只查询的结果，作为附查询的条件
只执行一次
返回一个值的子查询
返回多个字的只查询

1.创建视图
create [or replace] view name as select......from ....where [with check option]限制条件
2.查看视图
select.....from view_name;
3.查看视图结构
desc view_name;
4.插入数据
insert into view_name values();