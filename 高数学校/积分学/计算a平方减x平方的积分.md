例题（同时也是一个重要性质）[[计算a平方减x平方的积分]]：$$\begin{align*}
\int^a_{0} \sqrt{ a^2- x^2 }dx,(a>0) \\
令 x= a\sin t, 则 x^2 = a^2 \sin^2 t, dx = a\cos t dt\\
\int^a_{0} \sqrt{ a^2 - a^2 \sin^2 t } dt = a^2 \int^{\frac{\pi}{2}}_{0} \cos t * \cos tdt \\
用降幂公式：a^2\int^{\frac{\pi}{2}}_{0}  \frac{\cos 2t +1}{2} dt = \frac{a^2}{2} \left[  \frac{1}{2} (\sin 2t)|^{\frac{\pi}{2}}_{0}+t|^{\frac{\pi}{2}}_{0}  \right] =   \frac{a^2}{4} \pi 
\end{align*}$$
