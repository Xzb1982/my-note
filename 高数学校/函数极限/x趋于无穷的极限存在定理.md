那么，又因为极限存在且相等，所以得出[[x趋于无穷的极限存在定理]] 
$$\begin{align*}
设f(x)在(-\infty,a]∪[b,+\infty)上有定义(a≤b且均为常数)，A为一个确定的常数\\
∀（任给）ε>0,∃X>0,当|x|>X时（统一正负无穷中x>X和x<-X的条件）\\
都有|f(x)-A|<ε,则称f(x)当x趋向于\infty时，极限为A，记作\lim_{ x \to \infty } f(x)=A\\
\lim_{ x \to \infty } f(x)=A成立的充要条件是：\lim_{ x \to +\infty } f(x)=A,\lim_{ x \to -\infty } f(x)=A
\end{align*}$$
先证明必要性：
$$\begin{align*}
由\lim_{ x \to \infty }f(x)=A的定义可知， ∀ε>0,∃X>0,当|x|>X时,都有|f(x)-A|<ε\\
那么当-X<x<X时，都有|f(x)-A|<ε，那么\lim_{ x \to +\infty }f(x)以及\lim_{ x \to -\infty }  的极限都存在且都为A
\end{align*}$$
下面证明充分性：
$$\begin{align*}
由\lim_{ x \to +\infty }f(x)=A的定义可知， ∀ε>0,∃X_{1}>0,当x>X_{1}时,都有|f(x)-A|<ε\\
又∵\lim_{ x \to -\infty }f(x)=A,∃X_{2}>0,当x<-X_{2}时,都有|f(x)-A|<ε\\
那么X=max{X_{1}，X_{2}}（全面保证x在X的右，-X的左边），当|x|>X时，都有|f(x)-A|<ε\\
那么\lim_{ x \to \infty } f(x)=A
\end{align*}$$
这个定义有利于我们研究分段函数的极限情况