{{indexmenu_n>2}}

======= 数据表 =======

## 创建数据表

准备工作：用户将CSV、ORC、JSON类型的文件上传到Ufile中，上传说明详见
[UFile-操作指南-上传文件](/storage_cdn/ufile/guide/put)

**方式一：使用向导创建数据表**

1\. 进入USQL界面后，选择需要创建数据表的目标数据库 

2\. 在数据表的右边选择‘+创建数据表’
![](/images/创建数据表.png) 

3\. 在创建页中，输入表名称（限制：英文、数字）、选择数据格式、选择字段分隔符、输入字段列表及类型
![](/images/创建数据表2.png) 

4\. 点击 ‘创建’

**方式二：使用DDL语句创建数据表**

在查询框中输入DDL语句，创建数据表： 


```  
CREATE [EXTERNAL] TABLE [IF NOT EXISTS]
[db_name.]table_name [(col_name data_type [COMMENT col_comment] [, ...] )] 
PARTATION BY [col_name data_type] 
[ROW FORMAT row_format] 
[STORED AS file_format] 
[LOCATION 'ufile:']
[TBLPROPERTIES ( ['has_encrypted_data'='true | false',]
['classification'='aws_glue_classification',] property_name=property_value [, ...] ) ] 
```

## 查看数据表

USQL目前支持两种预览数据表的方式： 使用向导查看或通过SQL语句查看。

**方式一：使用向导查看数据表**

1\. 点击数据表右边的按钮，选择‘预览数据表’。 
![](/images/预览数据表.png) 

2\. 点击‘立即运行’。

**方式二：使用DDL查看数据表**

1\. 在查询框中输入

    SELECT * FROM table_name(表名称)

## 删除数据表

**方式一：使用向导删除数据表**

1\. 进入USQL界面后，选择数据表右边的‘…’再选择‘删除表’ 
![](/images/删除表.png)

2\. 点击 ‘删除’

**方式二：使用DDL语句删除数据表**

1\. 在查询框中输入

``` 
  DROP TABLE  table_name(表名称)
```

2\. 点击‘立刻运行’

## 查询数据表

使用SQL语句及函数查询数据表，详见 [SQL语句](/analysis/usql/common/sql/statement)

## 保存查询

USQL支持对SQL查询语句进行保存。

1\. 点击‘保存’
![](/images/common/查询.png) 

2\. 输入‘查询名称’和‘描述’并保存查询语句。
![](/images/common/查询2.png) 

3\. 已保存的查询语句在‘已保存SQL’中查看。
![](/images/common/查询3.png)

## 查询记录

USQL记录所有的查询操作。

用户可以在‘历史SQL’中查看所有查询记录，记录包括查询时间、查询语句、状态、运行时间、扫描数据量、下载结果。
![](/images/common/查询4.png)
