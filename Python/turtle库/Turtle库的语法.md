在绘制蟒蛇的代码里面，我们会看到一个import
这就是导入库的操作
import turtle就是导入turtle库
使用库里面的函数，我们就用库名.库里面的函数名(函数参数)来进行对库里面的函数的调用

from...import...
	我们也可以用 from 库名 import 库内函数名  来实现调用
	或者用： from 库名 import * 来调用库内所有函数
	![[Pasted image 20251026215526.png]]
	但是第二种方法的问题在于如果程序内部又自己定义了一些函数，函数名就有可能重复

import...as...
	我们将两种方法结合，用：import 库名 as 新名字  来导入库
	那么我们就可以用 新名字.函数名(函数参数)来调用函数了
	![[Pasted image 20251026220712.png]]

循环语句
	按一定次数循环执行的一组语句
	for 变量 in range(循环的次数)
		for i in range(5):
		print(i)
		![[Pasted image 20251026231523.png]]
		如果我们用 print("Hello",i)就是在Hello后面加了个空格再接上i，加了个逗号，就在字符串后面加空格
	range函数
		range(N)就是输出0到N-1的数字
		range(M,N)就是输出从M到N-1的数字
	for循环的本质是计数循环