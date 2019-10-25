

# 聚合函数

聚合函数主要应用于一组数据计算出一个结果。

除了 count(), count\_if(), max\_by(), min\_by() 和 approx\_distinct() 之外,
所有这些聚合函数均会忽略null值并且在没有输入数据或者所有数据 均是null值的情况下返回空结果。比如，sum()
会返回null而不是0, 以及 avg() 不会包含null值计数。 coalesce 函数会把null值转换成0。

**常规聚合函数**

arbitrary(x) → \[与输入参数相同\]：返回 x 的任意非null值。

array\_agg(x) → array\<\[与输入参数相同\]\>：返回以输入参数 x 为元素的数组。

avg(x) → double：返回所有输入值的平均数（算数平均数）。

bool\_and(boolean) → boolean：只有所有参数均为 TRUE 则返回 TRUE ，否则返回 FALSE。

bool\_or(boolean) → boolean：任何一个参数为 TRUE ，则返回 TRUE ， 否则返回 FALSE。

checksum(x) → varbinary：返回不受给定参数值顺序影响的校验值。

count(\*) → bigint：返回输入数据行的统计个数。

count(x) → bigint：返回非null值的输入参数个数。

count\_if(x) → bigint：返回输入参数中 TRUE 的个数。 这个函数和 count(CASE WHEN x THEN 1
END) 等同。

every(boolean) → boolean：这个函数是 bool\_and() 的别名。

geometric\_mean(x) → double：返回所有输入参数的几何平均值。

max\_by(x, y) → \[与x类型相同\]：返回 x 与 y 的全部关联中，y 最大值所关联的第一个 x 值。

max\_by(x, y, n) → array\<\[与x类型相同\]\>：x 与 y 的全部关联中， 以 y 降序排列前 n
个最大值所关联的 x 值中， 返回前 n 个值

min\_by(x, y) → \[与x类型相同\]：返回 x 与 y 的全部关联中，y 最小值所关联的第一个 x 值。

min\_by(x, y, n) → array\<\[与x类型相同\]\>：x 与 y 的全部关联中， 以 y 升序排列前 n 个值所关联的
x 值中， 返回前 n 个值

max(x) → \[与输入类型相同\]：返回输入参数中最大的值。

max(x, n) → array\<\[与x类型相同\]\>：返回所有参数 x 中前 n 大的值.

min(x) → \[与输入类型相同\]：返回所有输入参数中最小的值。

min(x, n) → array\<\[与x类型相同\]\>：返回所有输入参数 x 中，前 n 小的值。

sum(x) → \[和输入类型相同\]：返回所有输入参数的和。

**位聚合函数**

bitwise\_and\_agg(x) → bigint：返回所有输入值二进制与的结果，以二进制补码表示。

bitwise\_or\_agg(x) → bigint：返回所有输入值二进制或的结果，以二进制补码表示。

**映射聚合函数**

histogram(x) → map\<K,bigint\>：返回一个包含输入参数出现次数的映射表。

map\_agg(key, value) → map\<K,V\>：返回一个根据输入 key 和 value 对构造的映射表。

map\_union(x\<K, V\>) →
map\<K,V\>：返回所有输入映射表的联合。如果一个键同时出现在多个输入映射表中，结果中对应键值会取任意输入映射表中的一个。

multimap\_agg(key, value) → map\<K,array\<V\>\>：返回一个由输入参数 key 和 value
对组成的映射表。每个键可以对应多个值。
