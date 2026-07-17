讲矩阵的LU分解之前，我们需要涉及到两个基本公式：

对于AB而言，这两个矩阵乘上什么可以得到单位阵呢？
根据[[逆矩阵（用矩阵语言表述）]]，我们可以知道肯定是乘上逆矩阵

但是是怎么乘呢？
$$\begin{align*}
ABB^{-1}A^{-1}=I,根据矩阵乘法结合律\\
A(BB^{-1})A^{-1}=I \implies AA^{-1}=I\\
\end{align*}
$$
但是，为什么我们在乘以逆矩阵时，要反过来乘呢？

其实就像穿鞋搭袜一样，先脱鞋再脱袜，先穿袜再穿鞋。

这是第一个基本公式

接下来，我们也要涉及一些转置（transpose）的内容：

$$\begin{align*}
AA^{-1}=I,现在等式两边转置 \implies (AA^{-1})^{T}= I^T\\
单位矩阵的转置矩阵就是单位矩阵，因为单位矩阵是对称的。\\
那么（转置之后行变列，列变行，矩阵乘法的顺序只有相反才能符合左行右列）\\
\therefore (A^{-1})^TA^T= I, 那么，只有当 (A^{-1})^T= (A^T)^{-1}时\\
我们可以得到(A^{-1})^TA^T= (A^T)^{-1}A^{T}=I
\end{align*}
$$

矩阵的LU分解实际上和消元有关，消元的目的是为了使矩阵更清晰明了

例子：
$$\begin{align*}
L\begin{bmatrix}
2,1 \\
8,7
\end{bmatrix}= \begin{bmatrix}
2,1 \\
0,3
\end{bmatrix}\\
这里的L用矩阵乘法的知识可以知道：L= \begin{bmatrix}
1,0 \\
-4,1
\end{bmatrix}\\
因为第一行不变，可以为[1,0],第二行要进行行的数乘和相加减\\
因此可以放[-4,1],其中1不变，－4进行数乘加减运算,消去\begin{bmatrix}
2,1 \\
8,7
\end{bmatrix}的8\\ \\
那么，如果这样放呢？ \begin{bmatrix}
2,1 \\
8,7
\end{bmatrix}= L\begin{bmatrix}
2,1 \\
0,3
\end{bmatrix}\\
那么此处的L＝ \begin{bmatrix}
1,0 \\
4,1
\end{bmatrix}\\
可以这样理解： L^{-1}L \begin{bmatrix}
2,1 \\
8,7
\end{bmatrix}= L^{-1}\begin{bmatrix}
2,1 \\
0,3
\end{bmatrix}\implies \begin{bmatrix}
2,1 \\
8,7
\end{bmatrix}= L^{-1}\begin{bmatrix}
2,1 \\
0,3
\end{bmatrix}
\end{align*}
$$
当然也可以通过矩阵乘法来理解：
$$\begin{align*}
\begin{bmatrix}
2,1 \\
8,7
\end{bmatrix}= \begin{bmatrix}
1,0 \\
4,1
\end{bmatrix}\begin{bmatrix}
2,1 \\
0,3
\end{bmatrix}第一行不变，第二行再加回8
\end{align*}
$$

因此我们可以发现L是下三角矩阵，U是上三角矩阵：
$$\begin{align*}
\begin{bmatrix}
2,1 \\
8,7
\end{bmatrix}= \begin{bmatrix}
1,0 \\
4,1
\end{bmatrix}\begin{bmatrix}
2,1 \\
0,3
\end{bmatrix}
\end{align*}
$$
那么A＝LU（下三角矩阵左乘上三角矩阵）
下面继续分解，可以讲LU变成LDU，D是对角矩阵
[[矩阵的高斯消元法]]：$$\begin{align*}
初等交换矩阵: \begin{bmatrix}
1,0 \\
0,1
\end{bmatrix} \to(r_{1} \leftrightarrow r_{2}) \begin{bmatrix}
0,1 \\
1,0
\end{bmatrix}\\
初等数乘矩阵: \begin{bmatrix}
1,0 \\
0,1
\end{bmatrix} \to (kr_{2}) \begin{bmatrix}
1,0 \\
0,k
\end{bmatrix}\\
初等相加减矩阵： \begin{bmatrix}
1,0 \\
0,1
\end{bmatrix}\to (r_{1}+r_{2}) \begin{bmatrix}
1,1 \\
0,1
\end{bmatrix}
\end{align*}
$$


A=LDU是：

$$\begin{align*}
\begin{bmatrix}
2,1 \\
8,7
\end{bmatrix}= \begin{bmatrix}
1,0 \\
4,1
\end{bmatrix}\begin{bmatrix}
2,1 \\
0,3
\end{bmatrix} \implies \begin{bmatrix}
2,1 \\
8,7
\end{bmatrix}= \begin{bmatrix}
1,0 \\
4,1
\end{bmatrix}\begin{bmatrix}
2,0 \\
0,3
\end{bmatrix}\begin{bmatrix}
1, \frac{1}{2} \\
0,1
\end{bmatrix}
\end{align*}
$$

