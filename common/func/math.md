{{indexmenu_n>0}}

# 数据函数和运算符

**数学操作**

| 操作 | 描述    |
| -- | ----- |
| \+ | 加     |
| \- | 减     |
| \* | 乘     |
| /  | 除（取整） |
| %  | 取余    |


**数学函数**

abs(x) → \[same as input\]：返回x的绝对值。

cbrt(x) → double：返回 x 的立方根。

ceil(x) → \[same as input\]：ceiling() 的同名方法。

ceiling(x) → \[same as input\]：返回x的向上取整的值。

degrees(x) → double：将角度x以弧度转换为度。

e() → double：返回欧拉常量。

exp(x) → double：返回x的欧拉常量次幂。

floor(x) → \[same as input\]：返回x向下取整的最近整数。

from\_base(string, radix) → bigint：返回radix进制的字符串string代表的数值。

ln(x) → double：返回x的自然对数。

log2(x) → double：返回x以2为底的对数。

log10(x) → double：返回x以10为底的对数。

log(x, b) → double：返回x以b为底的对数。

mod(n, m) → \[same as input\]：返回n除m的模数(余数)。

pi() → double：返回常量Pi。

pow(x, p) → double：power()的同名方法。

power(x, p) → double：返回x的p次幂。

radians(x) → double：将角度x以度为单位转换为弧度。

rand() → double：random() 的同名方法。

random() → double：返回 0.0 \<= x \< 1.0 范围内的伪随机数。

random(n) → \[same as input\]：返回 0 \<= x \< n 范围内的伪随机数。

round(x) → \[same as input\]：返回x四舍五入后的最近的整数值。

round(x, d) → \[same as input\]：返回x四舍五入到d位小数位的值.

sign(x) → \[same as input\]：x的正负号函数x为0, 返回0; x\>0, 返回1; x\<0, 返回-1。

sqrt(x) → double：返回 x 的平方根。

to\_base(x, radix) → varchar：返回 x 的 radix 进制表示的字符串。

truncate(x) → double：舍弃 x 的小数位,返回整数值。

width\_bucket(x, bound1, bound2, n) → bigint：bound1 到 bound2 范围等长划分成n个桶,
返回x在其中的桶号。

width\_bucket(x, bins) → bigint：返回 x 在数组 bins 描述的分桶中的桶号. 参数 bins
必须是一个double类型的数组, 并且嘉定是按照升序排序的。


**三角函数**

所有三角函数都是以弧度表示

acos(x) → double：返回 x 的反余弦。

asin(x) → double：返回 x 的反正弦。

atan(x) → double：返回 x 的反正切。

atan2(y, x) → double：返回 y / x 的反正切。

cos(x) → double：返回 x 的余弦值。

cosh(x) → double：返回 x 的双曲余弦值。

sin(x) → double：返回 x 的正弦值。

tan(x) → double：返回 x 的正切值。

tanh(x) → double：返回 x 的双曲正切。


**浮点函数**

infinity() → double：返回表示正无穷大的常量。

is\_finite(x) → boolean：判定x是否为有限数。

is\_infinite(x) → boolean：判定x是否为无限数。

is\_nan(x) → boolean：判定x是否为非法数值。

nan() → double：返回代表非数值的常量值。
