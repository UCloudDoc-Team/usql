{{indexmenu_n>0}}

# CREATE TABLE AS SELECT

**描述**： 可以快速复制已有数据表，并产出不同格式的数据表

**语法**

    CREATE TABLE new_table_name
    ROW FORMAT SERDE 'SERDE type'
    LOCATION 'UFLIE://......'
       AS  
    SELECT *
    FROM original_table_name

**支持的SERDE**

``` 
 SUPPORT_SERDE_JOSN_OPENX("org.openx.data.jsonserde.JsonSerDe"),
 SUPPORT_SERDE_JOSN_HIVE("org.apache.hive.hcatalog.data.JsonSerDe"),
 SUPPORT_SERDE_ORC_HIVE("org.apache.hadoop.hive.ql.io.orc.OrcSerde"),
 SUPPORT_SERDE_TSV_LAZY("org.apache.hadoop.hive.serde2.lazy.LazySimpleSerDe"),
 SUPPORT_SERDE_CSV_OPEN("org.apache.hadoop.hive.serde2.OpenCSVSerde");
```
