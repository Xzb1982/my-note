
# 第一题
List L consists of the integers from 1 to 99 and two integers c and d such that c + d = 100 and cd<0.

Which of the following statements must be true？
Indicate all such statements

A. The average (arithmetic mean) of the numbers in L is equal to the median of the numbers in L.
B. The range of the numbers in L is greater than 100.
C. The range of the numbers in L is less than 200.


翻译：
列表 \(L\) 包含从 1 到 99 的所有整数，以及另外两个整数 \(c\) 和 \(d\)，其中满足：
\[ c+d=100,\qquad cd<0 \]

以下哪些陈述一定成立？（选择所有符合条件的选项）
A. 列表 \(L\) 中所有数的算术平均数等于其中位数。
B. 列表 \(L\) 中所有数的极差大于 100。
C. 列表 \(L\) 中所有数的极差小于 200。
注： 极差（Range）指一组数据中的最大值与最小值之差。

题目原文是：

> List L consists of the integers from 1 to 99 and two integers c and d such that c + d = 100 and cd < 0.

这里需要注意 consists of ... and ... 这个结构，意思是“由……和……组成”。
因此，题目的意思是：
列表 \(L\) 由以下整数构成：
① 从 1 到 99 的所有整数；
② 另外两个整数 \(c\) 和 \(d\)，满足 \(c+d=100\) 且 \(cd<0\)。
所以列表实际上是：
\[ L=\{1,2,3,\ldots,99,c,d\} \]
总共有 \(99+2=101\) 个整数。

要解这道题，先要满足cd两个的条件
	第一步：理解 cd<0
	两个整数相乘得到负数，说明它们一定一正一负。
	不妨假设：$$c<0,\qquad d>0 
	$$
	第二步：结合 c+d=100
	由题目可知： d=100-c 
	由于 c<0，所以： d=100-c>100 
	因此，我们得到了两个结论：$$\boxed{c<0,\qquad d>100} $$
	也就是说，列表 L 中新增的两个整数，一个比 1 小，另一个比 99 大。

之后：假设原来有 n 个数，平均数为 \mu，那么总和是 n\mu。
如果再加入 m 个数，而且这 m 个数的平均数同样为 \mu，那么：
$$ \bar{x}_{\text{新}} =\frac{n\mu+m\mu}{n+m} =\frac{(n+m)\mu}{n+m} =\boxed{\mu}$$ 
所以，只要两组数据的平均数相同，合并之后的平均数也相同，不管两组数据分别有多少个数。

A. 算术平均数等于中位数。
原本的 1 到 99 的中位数是 50。加入一个负数和一个大于 100 的数后，中位数仍然是 50。
同时，由于 c+d=100，新增两个数的平均值也是 50，因此整个列表的平均数仍然是 50。
所以 A 正确。

B. 极差大于 100。
由于最大值大于 100，最小值小于 0，因此：$$\text{Range}=\max(L)-\min(L)>100 $$
所以 B 正确。(也可以用 c<0,d>100直接推理)

C. 极差小于 200。
这个不一定。例如：$$c=-100,\qquad d=200 $$
虽然满足：$$c+d=100,\qquad cd<0 $$
但极差为：200-(-100)=300 
因此 C 不一定成立。



1, 2, 2, 3, 3, 3, 4, 4, 4, 4, …, 24 The list above consists of 300 entries that are integers in increasing order, and each integer  n occurs n times for 1 <=n <=24. What is the least integer k in the list for which at least 15 percent of all the entries are less than k?

给定以下数列：
\[ 1,2,2,3,3,3,4,4,4,4,\ldots,24 \]
上述数列共有 300 个整数，并且按照从小到大的顺序排列。
对于每个满足 \(1\leq n\leq24\) 的整数 \(n\)，它在数列中恰好出现 \(n\) 次。
问题：
在这个数列中，满足“至少 15% 的数列元素严格小于 \(k\)”这一条件的最小整数 \(k\) 是多少？
注意：题目中的 less than \(k\) 指的是严格小于 \(k\)，不包括等于 \(k\) 的元素。

300个数字，其中1重复1次，2重复2次，3重复3次，以此类推
300* 0.15 = 45

1+2+3+4+5+6+7+8+9 =45

应该是10？
