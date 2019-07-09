{{indexmenu_n>0}}

# 条件表达式

\*\* CASE \*\*

标准SQL中的CASE表达式有两种结构：

1\. 简单结构会从左至右依次查找value直到找到和expression的相等的值。

    CASE expression
        WHEN value THEN result
        [ WHEN ... ]
        [ ELSE result ]
    END

找到后会返回对应的result结果，如果没有找到相等的value，则会返回ELSE语句的result值。例如：

    SELECT a,
           CASE a
               WHEN 1 THEN 'one'
               WHEN 2 THEN 'two'
               ELSE 'many'
           END

2\. 高级结构会从左到右依次计算condition直到找到第一个为TRUE的condition，并返回其result值。

    CASE
        WHEN condition THEN result
        [ WHEN ... ]
        [ ELSE result ]
    END

如果没有找到 True 的 condition，则返回ELSE语句中的result值。例如：

    SELECT a, b,
           CASE
               WHEN a = 1 THEN 'aaa'
               WHEN b = 2 THEN 'bbb'
               ELSE 'ccc'
           END

**IF**

IF函数是和下述的CASE表达式效果相同:

    CASE
        WHEN condition THEN true_value
        [ ELSE false_value ]
    END

if(condition, true\_value): 如果condition为TRUE计算返回true\_value，否则返回NULL。

if(condition, true\_value, false\_value): 如果condition为TRUE计算返回
true\_value，否则计算返回 false\_value。
