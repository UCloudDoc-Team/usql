

# 字符串函数和运算符

**字符串运算符**

用’||‘执行连接

**字符串函数**

chr(n) → varchar：把n值转化成Unicode的char。

concat(string1, …, stringN) → varchar：字符串连接操作，返回 string1 , string2 , … ,
stringN 字符串连接。 此功能与标准SQL的连接运算符 ( || )功能相同。

length(string) → bigint：返回字符串 string 长度。

lower(string) → varchar：转换字符串 string 为小写。

lpad(string, size, padstring) → varchar：将字符串 string 左边拼接 padstring
直到长度达到 size 并返回填充后的字符串。如果 size 比 string 长度小，则截断。 size 不能为负数，
padstring 必须非空。

ltrim(string) → varchar：删除字符串所有前导空格。

replace(string, search) → varchar：删除字符串 string 中的所有子串 search 。

replace(string, search, replace) → varchar：将字符串 string 中所有子串 search 替换为
replace。

reverse(string) → varchar：将字符串 string 逆序后返回。

rpad(string, size, padstring) → varchar：将字符串 string 右边拼接 padstring
直到长度达到 size ,返回填充后的字符串。如果 size 比 string 长度小，则截断。 size 不能为负数，
padstring 必须非空。

rtrim(string) → varchar：删除字符串 string 右边所有空格。

split(string, delimiter) → array\<varchar\>：将字符串 string 按分隔符 delimiter
进行分隔，并返回数组。

split(string, delimiter, limit) → array\<varchar\>：将字符串 string 按分隔符
delimiter 分隔，并返回按 limit 大小限制的数组。数组中的最后一个元素包含字符串中的所有剩余内容。 limit 必须是正数。

split\_part(string, delimiter, index) → varchar：将字符串 string 按分隔符
delimiter 分隔，并返回分隔后数组下标为 index 的子串。 index 以 1 开头，如果大于字段数则返回null。

split\_to\_map(string, entryDelimiter, keyValueDelimiter) →
map\<varchar, varchar\>：通过 entryDelimiter 和 keyValueDelimiter
拆分字符串并返回map。 entryDelimiter 将字符串分解为key-value对，
keyValueDelimiter 将每对分隔成key、value。

strpos(string, substring) → bigint：返回字符串中子字符串的第一次出现的起始位置。位置以 1 开始
，如果未找到则返回 0 。

substr(string, start) → varchar：返回 start 位置开始到字符串结束。位置从 1 开始。如果 start
为负数，则起始位置代表从字符串的末尾开始倒数。

substr(string, start, length) → varchar：返回 start 位置开始长度为 length 的子串，位置从
1 开始。如果 start 为负数，则起始位置代表从字符串的末尾开始倒数。

trim(string) → varchar：删除字符串 string 前后的空格。

upper(string) → varchar：转换字符串为大写。

**Unicode函数**

normalize(string) → varchar：用NFC规范化形式转换字符串。

to\_utf8(string) → varbinary：将字符串编码为UTF-8格式。

from\_utf8(binary) → varchar：将二进制 binary
解码为UTF-8编码的字符串,无效的UTF-8字符被替换为Unicode字符
U+FFFD 。

from\_utf8(binary, replace) → varchar：将二进制 binary
解码为UTF-8编码的字符串。无效的UTF-8字符替换为 replace
。替换字符串必须是单个字符或空格（无效字符会被删除）。
