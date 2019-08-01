{{indexmenu_n>0}}

# CREATE TABLE AS SELECT

**描述**： 可以快速复制已有数据表，并产出不同格式的数据表

**语法**：

    CREATE TABLE new_table_name
    ROW FORMAT SERDE 'SERDE type'
    LOCATION 'ufile://......'
       AS  
    SELECT *
    FROM original_table_name

**支持的SERDE**：

``` 
 JOSN_OPENX SERDE："org.openx.data.jsonserde.JsonSerDe"
 JOSN_HIVE SERDE："org.apache.hive.hcatalog.data.JsonSerDe"
 ORC_HIVE SERDE："org.apache.hadoop.hive.ql.io.orc.OrcSerde"
 TSV_LAZY SERDE："org.apache.hadoop.hive.serde2.lazy.LazySimpleSerDe"
 CSV_OPEN SERDE："org.apache.hadoop.hive.serde2.OpenCSVSerde"
```
