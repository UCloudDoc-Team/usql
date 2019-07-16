{{indexmenu_n>0}}

# 分区PARTITION

**声明分区**

创建数据库时需要声明分区

    CREATE EXTERNAL TABLE table_name (col_name data_type, col_name data_type,... )
      PARTITIONED BY (date_name data_type,date_name data_type,...)
      STORED AS TEXTFILE
      LOCATION 'UFile://...';

示例

    CREATE EXTERNAL TABLE example(
      id string, 
      ip string, 
      delay int, 
      status string
    )
    PARTITIONED BY(year int, month int, day int)
    STORED AS TEXTFILE
    LOCATION 'UFile://...';

**添加分区**

    ALTER TABLE table_name ADD PARTITION partition_spec [LOCATION 'location']

添加多个分区

    ALTER TABLE table_name ADD 
    PARTITION partition_spec
    PARTITION partition_spec
    PARTITION partition_spec
    location 'ufile://...'

示例

    ALTER TABLE example ADD
    PARTITION (year = 2019, month = 04, day = 17)
    PARTITION (year = 2019, month = 04, day = 16)
    PARTITION (year = 2019, month = 04, day = 15)

**查看分区** 
语法

    SHOW PARTITIONS table_name

**查询分区**

    SELECT *FROM table_name WHERE partition_spec

示例

    SELECT *FROM example WHERE year = 2019 and month = 04

**删除分区**

    ALTER TABLE table_name DROP PARTITION partition_spec

一次性删除多个分区时，需要使用逗号隔开
