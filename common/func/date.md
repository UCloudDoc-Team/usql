

# 日期时间函数和运算符

**日期时间运算符**

| 操作符 | 例子                                                | 结果                      |
| --- | ------------------------------------------------- | ----------------------- |
| \+  | date '2012-08-08' + interval '2' day              | 2012-08-10              |
| \+  | time '01:00' + interval '3' hour                  | 04:00:00.000            |
| \+  | timestamp '2012-08-08 01:00' + interval '29' hour | 2012-08-09 06:00:00.000 |
| \+  | timestamp '2012-10-31 01:00' + interval '1' month | 2012-11-30 01:00:00.000 |
| \+  | interval '2' day + interval '3' hour              | 2 03:00:00.000          |
| \+  | interval '3' year + interval '5' month            | 3-5                     |
| \-  | date '2012-08-08' - interval '2' day              | 2012-08-06              |
| \-  | time '01:00' - interval '3' hour                  | 22:00:00.000            |
| \-  | timestamp '2012-08-08 01:00' - interval '29' hour | 2012-08-06 20:00:00.000 |
| \-  | timestamp '2012-10-31 01:00' - interval '1' month | 2012-09-30 01:00:00.000 |
| \-  | interval '2' day - interval '3' hour              | 1 21:00:00.000          |
| \-  | interval '3' year - interval '5' month            | 2-7                     |

**时区转换**

‘AT TIME ZONE’运算符定义时间标签

    SELECT timestamp '2012-10-31 01:00 UTC';
    2012-10-31 01:00:00.000 UTC
    
    SELECT timestamp '2012-10-31 01:00 UTC' AT TIME ZONE 'America/Los_Angeles';
    2012-10-30 18:00:00.000 America/Los_Angeles

**日期和时间函数**

current\_date -\> date：返回查询开始时的当前日期。

current\_time -\> time with time zone：返回查询开始时的当前时间。

current\_timestamp -\> timestamp with time zone：返回查询开始时的当前时间戳。

current\_timezone() → varchar：以IANA（例如，America /
Los\_Angeles）定义的格式返回当前时区，或以UTC的固定偏移量（例如+08：35）返回当前时区。

from\_iso8601\_timestamp(string) → timestamp with time zone：将ISO
8601格式化的字符串解析为具有时区的时间戳。

from\_iso8601\_date(string) → date：将ISO 8601格式的字符串解析为日期。

rom\_unixtime(unixtime) → timestamp： 返回unixtime时间戳。

from\_unixtime(unixtime, string) → timestamp with time
zone：返回指定时区的unixtime时间戳。

from\_unixtime(unixtime, hours, minutes) → timestamp with time
zone：返回为hours和minutes对应时区的unixtime时间戳。

localtime -\> time：返回查询开始时的当前时间。

localtimestamp -\> timestamp：返回查询开始时的当前时间戳。

now() → timestamp with time zone：这是current\_timestam的另一种表达。

to\_iso8601(x) → varchar：将x格式化为ISO 8601字符串。 x可以是date,
timestamp,或带时区的timestamp。

to\_unixtime(timestamp) → double：转换为unix时间戳。

    注意：
    以下SQL标准的函数不使用括号：
    current_date
    current_time
    current_timestamp
    localtime
    localtimestamp
