# 第一题

Distinct odd prime numbers 的意思是：两个互不相同的奇质数。
a and b are distinct odd prime numbers.

Quantity A: The number of factors of 2𝑎𝑏^2
Quantity B: The number of factors of 𝑎^2* b^3

我觉得是A，因为2n a ab b b^2 1都是其因数
B只有 $$a ,b ,a^2, b^2, b^3, a^2b, ab^3, a^2  b^2 , 𝑎^2b^3,ab^2,ab,1
$$

答案是C

首先，A有 1 2 a b ab 2a 2b 2b^2 2ab^2 ab^2   b^2 2ab

这种题最好列表


# 第二题

在坐标系中有点（a,b）,其中 a 和 b 均为正整数，问有多少个点满足关系式𝑎 + 𝑏 ≤ 200
101 * 100 = 10100个点
思路：我们先只看在y轴上的101个点，包含(0,0),之后向正x轴* 100倍数

# 第三题

x and y are integers.
Quantity A: 2^(𝑥+𝑦)^2
Quantity B:
2 ^(𝑥^2+𝑦^2)
 (𝑥+𝑦)^2 = 𝑥^2+𝑦^2 + 2xy  \implies 2xy ? 0 \implies xy ? 0
d

a is a positive integer.
x is the remainder when 15a is divided by 6.
\frac{15a}{6} \implies \frac{5a}{2} 的余数为 x 如果 a为1，则余下0,；如果a是2，那么余0,；即除2n为0；除2n+1余1
a是>0的整数
Quantity A:x
Quantity B:2
选B  （不对）

该题需要用到带余除法定理
对于整数 N 和正整数 d，总能唯一地写成：$$\boxed{N=dq+r,\qquad 0\leq r<d.} $$
这里，N 是被除数，d 是除数，q 是整数商，r 是余数。
进而，我们可以推导出：$$r = N- dq , 0\leq r<d$$
即：==**余数就是取出完整组后剩下的数量**==
该式还告诉我们：==**当被除数 N、除数 d和整数商 q 都已知时，能通过 r=N-dq 唯一确定余数。**==
不过，q 不能随便选，它必须使算出的 r 满足 0\leq r<d。例如选 q=2，会得到 17-5\times2=7，超过了除数 5，说明还可以再分出一组。
进一步我们可以得知：$$ \frac{N}{q} = d+ \frac{r}{q},0\leq r<d 且 q≠0$$
在 q>0 的情况下，可以把它理解成：**把全部 N 个东西平均分给原来的 q 组，每组原先有 d 个，再分到剩余部分的 \frac rq。**

**不过，这个等式不能保证“N 除以 q，整数商就是 d，余数就是 r”**，因为余数还必须小于新的除数 q。
例如：19=5\times3+4. 

两边除以 3： $$\frac{19}{3}=5+\frac43. $$
但 \frac43 里面还含有一个完整的 1，所以要继续整理： $$\frac{19}{3}=6+\frac13. $$
因此，19 除以 3的整数商是 6，余数是 1。原来的 4 大于新的除数 3，不能直接充当这次除法的余数。
所以：$$\boxed{\text{小数部分}=\frac{\text{余数}}{\text{除数}}} 
$$
以及反过来：$$\boxed{\text{余数}=\text{除数}\times\text{小数部分}.} $$
## 为什么分数可以约分，余数却不能直接照搬？
你写的$$\frac{15a}{6}=\frac{5a}{2} $$
完全成立。但“分数的值相等”，不能直接推出“两个除法的余数相等”。

因为
	对于整数 N 和正整数 d，存在唯一的整数 q,r，使得： $$\boxed{N=dq+r,\qquad 0\leq r<d} $$
	现在假设我们把被除数 N 和除数 d 同时乘以一个正整数 k。
	两边同时乘 k：kN=k(dq+r) 
	根据乘法分配律：$$\boxed{kN=(kd)q+kr} $$
	注意，这里已经得到一个新除法的形式：
	- 新的被除数是 kN；
	- 新的除数是 kd；
	- 整数商仍然是 q；
	- 剩余部分变成了 kr。
	但我们还不能马上断言 kr 就是新的余数，因为必须验证： $$0\leq kr < kd $$
	原来的余数满足：$$0\leq r < d $$
	由于 k>0，不等式两边同时乘 k，方向不变：$$\boxed{0\leq kr<kd} $$
	这恰好满足带余除法定理对余数的要求。

# 第四题

a is a positive integer.
x is the remainder when 15a is divided by 6.
\frac{15a}{6} \implies \frac{5a}{2} 的余数为 x 如果 a为1，则余下0,；如果a是2，那么余0,；即除2n为0；除2n+1余1
a是>0的整数
Quantity A:x
Quantity B:2

回到这一道题： 15a/6 N为15a，d为6， 15a = 6q+x  a>0,  0<= x < 6
选D

# 第五题

使得5^𝑎是1500的最大因子的𝑎的值，和使得3^𝑏是33,333,333的最大因子𝑏的值，下列说法正确的有：

A. 𝑎𝑏 = 3
B. 𝑎 = 3𝑏
C. 2𝑎 > 3

第一句话的意思是：1500 最多能被多少个 5 连续整除？，这个多少个 = a
a=3
33,333,333最多能被多少个3整除 b=1

ABC都对


A. The tens digit of the product (4^100)(5^99)
B. The tens digit of the product (4^100)(5^101)

==**tenth digit是十分位，ten's digit是十位**==

这道题直接用到的是**十进制位值原理**：一个整数乘以 100，原来的各个数位都向左移动两位，空出的个位、十位填上 0。例如：$$37\times100=3700.$$ 
如果进一步追问“一个整数末尾究竟有几个零”，就可以用质因数分解来解释。其理论基础是**算术基本定理**：
==**每个大于 1 的正整数，都能分解成质数的乘积；不考虑排列顺序，这种分解是唯一的。**==

因为10=2* 5, 

所以，**每凑出一个因子 2 和一个因子 5，就能凑出一个因子 10**。能凑出多少个 10，就能在末尾形成多少个零。

这就得到常用规律： $$\boxed{ \text{末尾连续零的个数} = \min\!\left\{ \text{质因数 }2\text{ 的个数}, \text{质因数 }5\text{ 的个数} \right\}. } $$

所以这道题选择C，两者相等

![[Pasted image 20261109202501.png]]

# 第六题

r is the remainder obtained dividing7^995 + 7^50 − 4 by 7

Quantity A: r
Quantity B: 4

7^995 + 7^50 − 4 =N,  d=7, 
r在[0,7)之间，所以选D  不对

首先，7^995 + 7^50 − 4 我们需要变成 7q+r的形式，而且r要在[ 0,d ) 之间
这样我们才能求出更为准确的r
7(7^994 + 7^49) -4 dq部分凑出来了，但是r还没凑出来，于是我们需要把-4变成 0到7里面的数字
因为前面有7，于是我们可以借助7来凑:  N=7（7^{994}+7^{49}）-4. 
同时，根据带余除法：N=7q+r. 
两个表达式表示同一个 N，因此：7K-4=7q+r. 
移项得到：$$\boxed{r+4=7(K-q).} $$
由于 K,q 都是整数，右边是 7 的整数倍，所以：$$ \boxed{r+4\text{ 必须是 }7\text{ 的倍数}.} 
$$
现在再用你已经得到的范围：0\leq r<7 \quad\Longrightarrow\quad 4\leq r+4<11. 
在 [4,11) 里，7 的倍数只有 7。因此：
$$r+4=7 \quad\Longrightarrow\quad \boxed{r=3}. $$

## 为什么 [0,7) 没有保留题目的全部信息？

题目给你的条件是：$$ \begin{cases} N=7^{995}+7^{50}-4,\\ N=7q+r,\quad q\text{ 是整数},\\ 0\leq r<7. \end{cases} $$
一个数要成为**本题的余数**，必须同时满足这些条件。
你只使用最后一条，就得到：$$r\in\{0,1,2,3,4,5,6\}. $$

这个推导完全正确。但这七个数只是**通过了“余数范围”检查的候选值**，还没有检查它们能不能满足前面的等式。
例如，r=0 符合范围，但它是否真能成为本题的余数，还要检查： $$7^{995}+7^{50}-4=7q $$
是否存在整数 q 使它成立。不能只因为 0 在范围里，就认定本题允许 r=0。
因此，你原先从“范围中既有小于 4的数，也有大于 4 的数”走到选 D，中间缺少了一步：
**这些不同的数，是否真的都能满足题目的其余条件？**

# 第七题

n is an even integer.偶整数
Quantity A：The number of prime factors of n
Quantity B：The number of prime factors of n/2
n的质因数的数量 ？ \frac{n}{2} 的质因数的数量

n可以是负数，但是一定有2 这个质因子 （一定要记住，==**质数没有1**==）
然后 \frac{n}{2} 会改变偶数的偶性吗？—— 会

## 为什么偶数除以 2，不一定得到奇数？
根据偶数的定义：$$n=2k,\qquad k\in\mathbb Z $$
所以：\frac n2=k 
我们只知道 k 是整数，并不知道它是奇数还是偶数。
例如：

| n   | n/2 | 除以 2 后 |
| --- | --- | ------ |
| 6   | 3   | 奇数     |
| 10  | 5   | 奇数     |
| 12  | 6   | 偶数     |
| 16  | 8   | 偶数     |

那么，究竟什么时候会变成奇数？
这取决于 n含有几个因子 2。
如果 n=2\times3=6，除掉唯一的一个 2 后，剩下 3，已经没有因子 2。
如果 n=2\times2\times3=12，除掉一个 2 后，剩下 2\times3=6，仍然含有因子 2。

对于任何非零偶整数，都可以写成： n=2^k m 
其中 k\geq1，m 是奇整数。
除以 2：$$\frac n2=2^{k-1}m 
$$
这里有两种情况：
① 当 k=1 时，n/2=m，质因数 2 消失，因此 A 比 B 多一个不同质因数。
② 当 k≤2 时，n/2 仍含有质因数 2，因此 A 和 B 的不同质因数集合完全相同。

![[Pasted image 20261109223546.png]]

![[Pasted image 20261109223908.png]]

# 第八题

If c and d are odd positive integers, which of the following could be odd?

Indicate all such expressions

![[Pasted image 20261109234510.png]]

奇数乘上奇数还是奇数
AB都是奇数
偶数乘上偶数还是偶数，C不对
奇数+奇数=偶数，偶数乘上偶数还是偶数，D不对
奇数/奇数 有可能除不尽，因此不一定是偶数，也不一定是奇数 E不对
选AB

不对，E也可以入选，因为题干问的是==**could be**==
CD是不可能为奇数的
E可以为奇数

# 第九题

if x is an integer, which of the following must be an even integer?

A. 𝑥^2 − 𝑥 − 1 找特例 x=1 就不是偶数

B. 𝑥^2 − 4𝑥 + 6 找特例 x=1 就不是偶数

C. 𝑥^2 − 5𝑥 + 5 找特例 x=1 就不是偶数

==**D. 𝑥^2 + 3𝑥 + 8==**  选D

E. 𝑥^2 + 2𝑥 + 10 找特例 x=1 就不是偶数

# 第十题

If w, x, y, and z are consecutive positive integers （连续正整数）, where w<x<y, which of the following statements must be true?

Indicate all such statements.


A. wxy is a multiple of 3. A一定对，因为任意一个连续3个正整数一定是3的倍数

B. wxz is a multiple of 3.B不一定，因为 如果是 xyz是连续的 x< y< z就不满足了

C. wxy + wyz is a multiple of 3. wxy一定有3的倍数，但是wyz不一定，把wy提出来，x+z,

