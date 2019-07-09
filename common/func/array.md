{{indexmenu_n>0}}

# 数组函数和运算符

**下标运算符\[\]**

\[\]运算符用于访问数组中的一个元素，并从一个元素开始建立索引:

    SELECT my_array[1] AS first_element

**连接运算符||**

||运算符用于将数组与相同类型的数组或元素连接起来:

    SELECT ARRAY [1] || ARRAY [2]; -- [1, 2]
    SELECT ARRAY [1] || 2; -- [1, 2]
    SELECT 2 || ARRAY [1]; -- [2, 1]

**数组函数**

array\_distinct（x ）-\> x：去重：删除数组x中重复元素。

Array\_intersect(x,y) -\>(x,y)：返回X，y中的交集数据，并去重。

Array\_union(x,y) -\>(x,y)：返回X，y中的并集数据，并去重。

array\_except(x, y) → (x,y)：从x数组中去除y数组中的元素，并返回新数组。

array\_join(x, delimiter, null\_replacement) →
varchar：使用分隔符和可选字符串连接给定数组的元素，以替换空值。

array\_max(x) → x： 返回数组中最大值x。

array\_min(x) → x：返回数组中最小值x。

array\_position(x, element) → bigint：x中第一次出现element的位置，如果没有则返回0。

array\_remove(x, element) → array：删除x中所有与element 相同的元素。

array\_sort(x) → array：排序并返回有序数组，x需要非空，空元素将放置在返回数组的末尾。

arrays\_overlap(x, y) →
boolean：测试x、y是否含有非空的相同元素，如果没有共同非空元素但是x或y为空，则返回null。

cardinality(x) → bigint：返回数组x的基数大小。

concat(array1, array2, ..., arrayN) →
array：连锁array1-arrayN，与SQL的标准操作||有相同效果。

contains(x, element) → Boolean：如果数组x含有element则返回true。

element\_at(array\<E\>, index) → E：返回数组中在index位置的元素（index\>=0）。

filter(array, function) → array：使用function在array内构建数组。

flatten(x) → array：把array（array（T））链接成arrat（T）。

reverse(x) → array：反转数组排列顺序。

sequence(start, stop) →
array\<bigint\>：从start到stop生成整数序列，如果start\<stop，按照1递增，反之按照1递减。

sequence(start, stop, step) →
array\<bigint\>：从start到stop按照step规律递增生成整数序列。

sequence(start, stop, step) →
array\<timestamp\>：从start到stop按照step规律递增生成时间戳序列，step范围：年月日时分秒。

shuffle(x) → array：随机排序数组。

slice(x, start, length) → array：在数组x中选出以start开始，长度为length的子数组。

transform(array, function) → array：数组array中的所有元素按照function运算，并返回新数组。

zip(array1, array2\[, ...\]) → array\<row\>：合并多个数组至一个数组。

zip\_with(array1, array2, function) →
array：使用函数function合并数组1、数组2，数组1、2需要有相同长度。
