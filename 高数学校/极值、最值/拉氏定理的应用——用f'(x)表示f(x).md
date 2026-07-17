拉格朗日中值定理的应用


$$\begin{align*}
(1)f(x)∈C[a,b];(2)f(x)∈D(a,b)\\
则至少存在一点\xi∈(a,b),使f'(\xi)=\frac{f(b)-f(a)}{b-a}
\end{align*}$$
其中：
$$f'(\xi)=\frac{f(b)-f(a)}{b-a} ⇔ f(b)-f(a)=f'(\xi)(b-a),在a<b前提下$$
$$\begin{align*}
当b<a时，只要f(x)在[b,a]上满足拉格朗日中值定理的条件，结论仍成立\\
f(a)-f(b)=f'(\xi)(a-b),b<\xi<a\implies两边乘-1就是f(b)-f(a)=f'(\xi)(b-a)
\end{align*}$$
也就是说无论a<b,b<a,只要f(x)满足拉格朗日中值定理的条件，那么：
$$f(b)-f(a)=f'(\xi)(b-a)的\xi介于a,b之间$$
同时我们可以推导出:![[Pasted image 20250126151111.png]]
$$\begin{align*}
0< \frac{|\xi-a|}{|b-a|}<1\implies 0< |\frac{\xi-a}{b-a}|<1\implies 无论a,b的大小关系怎么样，\frac{\xi-a}{b-a}>0\\
那么0< \frac{\xi-a}{b-a}<1 \implies 令 \theta=  \frac{\xi-a}{b-a}，那么\xi= a+\theta(b-a)\\
f(b)-f(a)= f'(a+\theta(b-a))*(b-a)
\end{align*}$$

只要一个ξ介于[a,b]或[b,a]之间，都可以写成这种形式

其他形式：
x1,x2形式：$$\begin{align*}x_{1}≠x_{2},且f(x)在x_{1},x_{2}构成区间内满足拉格朗日中值定理成立条件\\
那么f(x_{2})-f(x_{1})= f'(x_{1}+\theta(x_{2}-x_{1}))*(x_{2}-x_{1})
\end{align*}$$
x0,x0+Delta x形式：$$\begin{align*} \Delta x≠0,且f(x)在x_{0},x_{0}+\Delta x构成区间内满足拉格朗日中值定理成立条件\\
那么f(x_{0}+\Delta x)-f(x_{0})= f'(x_{0}+\theta*\Delta x)*\Delta x
\end{align*}$$
以上: 0<θ<1