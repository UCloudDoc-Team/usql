{{indexmenu_n>5}}

# SELECT

**描述：**基本的查询语句，返回查询结果

**语法：**

    SELECT [ALL | DISTINCT] attr_expr_list FROM table_reference 
    [WHERE where_condition] 
    [GROUP BY col_name_list] 
    [ORDER BY col_name_list]
    [ASC | DESC] 
    [SORT BY col_name_list]] 
    [LIMIT number]

**关键字：**

ALL：为默认选项；返回结果包含重复行，其后必须为\*。

DISTINCT：返回结果不含重复行。

WHERE：查询的过滤条件，支持算术运算符、关系运算符和逻辑运算符。

GROUP BY：分组判断条件，支持单字段及多字段分组。

ORDER BY：返回按排序条件查询的结果。

Col\_name\_list：字段列表。

ASC/DESC：ASC为升序，DESC为降序，默认为ASC。

SORT BY：在桶内进行排序。

LIMIT：对查询结果进行限制，number参数仅支持INT类型。
