![[Pasted image 20260810125916.png]]
注意”步进“按钮，可以一步步来运行
"继续"可以让你选定一个步骤然后，你点了之后可以一直往下运行下去
![[Pasted image 20260810131139.png]]
这里的红色是添加了断点，那么如果点了"继续"，那么就会运行到断点那一行

又例如计算矩形的面积和周长可以用以下代码![[Pasted image 20260810131610.png]]

![[Pasted image 20260810131810.png]]
我们在工作区选项卡，可以双击变量名称，然后查看这个变量里面有什么

![[Pasted image 20260810132349.png]]

matlab和python很像，但是要注意区别，例如print（python的输出函数）变成disp()
而且前面需要:
clc
clear
close all

![[Pasted image 20260810132651.png]]
![[Pasted image 20260810132605.png]]
上图是matlab条件选择逻辑的程序写法

MATlab for循环的编写

![[Pasted image 20260810135152.png]]
for循环完整的参数的写法是
![[Pasted image 20260810135546.png]]
也就是：起点：步长：终点

MATLAB构造函数
![[Pasted image 20260810140656.png]]![[Pasted image 20260810145116.png]]

![[Pasted image 20260810145407.png]]
你可以发现这里有个步进，也就是进入这个子函数，那么进入这个子函数，运算完了之后继续下一步，就直接出结果了

MATLAB绘图
![[Pasted image 20260810150237.png]]

![[Pasted image 20260810150507.png]]
![[Pasted image 20260810150710.png]]
在这里，就相当于创建了一个year序列，从0到10，然后步长为2

![[Pasted image 20260810150857.png]]
population = zeros(1行，11列)
这个是构建全0矩阵的语句

![[Pasted image 20260810151502.png]]

![[Pasted image 20260810151708.png]]

![[Pasted image 20260810151804.png]]

可以看一下上面的，怎么一步步画图的

相应的，python代码的画图，如图所示：![[Pasted image 20260810152011.png]]