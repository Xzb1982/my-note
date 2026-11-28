PCA 要做的是：**把多个变量压缩成少数几个新变量，并尽量保留样本之间的差异。**这里用“方差”衡量差异，所以推导围绕一个目标展开：**找一个投影方向，让投影后的方差最大。**

我们先推导“把多个变量压缩成一个变量”，再推广。
构造新变量
	假设有 n 个样本、p 个变量，组成数据矩阵 X：每行是一个样本，每列是一个变量。
先将每列减去该列的均值，这叫**中心化**：$$x_{ij}\leftarrow x_{ij}-\bar x_j. $$
以下的 X 都指中心化后的数据，因此每列均值都是 0。

我们想把原来的 \(p\) 个变量加权求和，得到一个新变量：

\[ z_i=a_1x_{i1}+a_2x_{i2}+\cdots+a_px_{ip}, \qquad \boxed{z=Xa}. \]

其中 \(a=(a_1,\ldots,a_p)^\top\) 是需要求的系数。

从几何上看，如果 \(a\) 是单位向量，那么 \(z_i=a^\top x_i\) 就是第 \(i\) 个样本沿着方向 \(a\) 的投影坐标。因此，我们要求：

\[ a^\top a=a_1^2+\cdots+a_p^2=1. \]

这个约束很必要：如果允许把所有系数乘以 \(10\)，新变量的方差就会变成原来的 \(100\) 倍。**固定系数向量的长度，才能公平比较不同方向。**

## 二、为什么求着求着，就变成了特征值问题？

### 1. 把“投影后的方差”写出来

因为 \(X\) 已经中心化，所以 \(z=Xa\) 的均值也是 \(0\)。于是：

\[ \begin{aligned} s_z^2 &=\frac{1}{n-1}\sum_{i=1}^n z_i^2\\ &=\frac{1}{n-1}(Xa)^\top(Xa)\\ &=a^\top\left(\frac{X^\top X}{n-1}\right)a. \end{aligned} \]

记样本协方差矩阵为

\[ S=\frac{X^\top X}{n-1}, \]

便得到：

\[ \boxed{s_z^2=a^\top Sa}. \]

所以，第一主成分要解决的问题就是：

\[ \boxed{\max_a\ a^\top Sa \quad\text{满足}\quad a^\top a=1.} \]

### 2. 用拉格朗日法求解

构造拉格朗日函数：

\[ L(a,\lambda)=a^\top Sa-\lambda(a^\top a-1). \]

由于 \(S\) 是对称矩阵，对 \(a\) 求导并令其为零：

\[ \frac{\partial L}{\partial a} =2Sa-2\lambda a=0 \quad\Longrightarrow\quad \boxed{Sa=\lambda a}. \]

这就是**特征值方程**：\(a\) 是协方差矩阵 \(S\) 的特征向量，\(\lambda\) 是对应的特征值。

再在两边左乘 \(a^\top\)：

\[ a^\top Sa=\lambda a^\top a=\lambda. \]

而左边恰好是投影后的方差，所以：

\[ \boxed{\text{沿单位特征向量投影后的方差} =\text{对应的特征值}.} \]

因此，要让方差最大，就选择**最大特征值对应的单位特征向量**。

### 3. 为什么它确实是全局最大？

将 \(S\) 的特征值从大到小排列：

\[ \lambda_1\geq\lambda_2\geq\cdots\geq\lambda_p\geq0, \]

对应的单位特征向量为 \(v_1,\ldots,v_p\)，它们可以取为彼此正交。

任意单位方向都能写成 \(a=\sum_j c_jv_j\)，且 \(\sum_jc_j^2=1\)。于是：

\[ a^\top Sa =\sum_{j=1}^p\lambda_jc_j^2 \leq\lambda_1\sum_{j=1}^pc_j^2 =\lambda_1. \]

这说明任何方向的方差都不会超过 \(\lambda_1\)，而取 \(a=v_1\) 正好达到它。

所以，**第一主成分**为：

\[ \boxed{z_1=Xv_1,\qquad s_{z_1}^2=\lambda_1.} \]

注意这里的区别：\(v_1\) 是方向或系数，\(z_1\) 才是算出来的新变量。

## 三、第二、第三主成分怎么来？

得到第一主成分后，继续找第二个方向，但要求它与第一个方向正交：

\[ \max_a a^\top Sa, \qquad a^\top a=1,\quad a^\top v_1=0. \]

在上面的展开式 \(a=\sum_jc_jv_j\) 中，这相当于要求 \(c_1=0\)。剩下能取得的最大方差就是 \(\lambda_2\)，方向为 \(v_2\)。

依次类推：

\[ \boxed{ z_1=Xv_1,\quad z_2=Xv_2,\quad\ldots,\quad z_k=Xv_k. } \]

这些新变量之间的样本协方差为：

\[ \widehat{\operatorname{Cov}}(z_j,z_\ell) =v_j^\top Sv_\ell =\lambda_\ell v_j^\top v_\ell =0,\qquad j\neq\ell. \]

所以，各主成分**互不相关**。这里不能直接理解为“相互独立”。

原数据的总方差等于所有特征值之和，因此，保留前 \(k\) 个主成分的累计方差贡献率为：

\[ \boxed{ \frac{\lambda_1+\cdots+\lambda_k} {\lambda_1+\cdots+\lambda_p}. } \]