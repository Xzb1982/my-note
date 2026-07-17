[[format函数]]
format函数可以用，分割例如"{}{}".format(A,B)
那么这样，AB分别会放在前后两个{}里面

format {:<填充字符，如果要写参数就{序号}><对齐方式><长度><是整数还是小数>}

==**注意有for循环的时候要看一下里面的变量有没有漏赋值的**==

变量可以交换赋值例如
	a, b = b, a + b
	这个可以慢慢理解成：
		- 原来的 `b` 变成新的 `a`
		- 原来的 `a+b` 变成新的 `b`
	比如原来是:
		- `a=0`
		- `b=1`
	更新后就是：
		- `a=1`
		- `b=1`
	再更新一次：
		- `a=1`
		- `b=2`
	再更新一次:
		- `a=2`
		- `b=3`

列表切片
	列表切片的基本样子是：
	[开始:结束:步长]
	`[::-1]` 里：
		- 开始不写，表示从头开始
		- 结束不写，表示到最后
		- 步长是 `-1`，表示倒着走

for循环可以 for in range也可以 for A in B B可以是列表
==**如果是后者,那么可以用A遍历并提取列表里面所有的元素**==

eval(input()) 组合，将输入的字符串转换为数字

for i in range(10)
	for+range组成计数循环


print(..., end=",")
	前面一个参数输入的是输出出来的内容，可以是变量也可以是字符串
	end=""是因为
		默认 `print()` 打印后会换行  
		这里改成每次打印后接一个逗号

len()
	求字符串的长度，就是字符个数的函数
	`len()`不管你是文字还是中文逗号，只要是一个字符，它就算 1 个。

.split()
	==**字符串/字符串变量名.split()**==
	`split()` 的作用就是“按...切开”。
		里面可以填","，那么就是按照“，”切开
		==**也可以直接填""，那么就是按照空格切开,注意不要打空格上去不然会多空几格**==
	例如："0 1 3 5".split()
	会得到：['0', '1', '3', '5']
	==**返回分割后的字符串列表**==

open() 
	用于打开一个文件，创建一个 file 对象，通过相关参数读写文件
	语法
		open(name[, mode[, buffering]])
	参数说明：
	- name : 一个包含了你要访问的文件名称的字符串值。
	- mode : mode 决定了打开文件的模式：只读，写入，追加等。所有可取值见如下的完全列表。这个参数是非强制的，默认文件访问模式为只读(r)。
	- buffering : 如果 buffering 的值被设为 0，就不会有寄存。如果 buffering 的值取 1，访问文件时会寄存行。如果将 buffering 的值设为大于 1 的整数，表明了这就是的寄存区的缓冲大小。如果取负值，寄存区的缓冲大小则为系统默认。

file对象的相关方法
	file 对象方法
	- **file.read([size])**：size 未指定则返回整个文件，如果文件大小 >2 倍内存则有问题，f.read()读到文件尾时返回""(空字串)。
	- **file.readline()**：返回一行。
	- **file.readlines([size])** ：返回包含size行的列表, size 未指定则返回全部行。
	- **for line in f: print line** ：通过迭代器访问。
	- **f.write("hello\n")**：如果要写入字符串以外的数据,先将他转换为字符串。
	- **f.tell()**：返回一个整数,表示当前文件指针的位置(就是到文件头的字节数)。
	- **f.seek(偏移量,[起始位置])**：用来移动文件指针。
		- 偏移量: 单位为字节，可正可负
		- 起始位置: 0 - 文件头, 默认值; 1 - 当前位置; 2 - 文件尾
	- **f.close()** 关闭文件


replace() 
	把字符串中的 old（旧字符串） 替换成 new(新字符串)，如果指定第三个参数max，则替换不超过 max 次。
	str.replace(old, new[, max])
	参数
		- old -- 将被替换的子字符串。
		- new -- ==**新字符串，用于替换old子字符串。**==
		- max -- 可选字符串, 替换不超过 max 次
	str = "this is string example....wow!!! this is really string";
	print str.replace("is", "was");
	print str.replace("is", "was", 3);
	以上实例输出结果如下：
		thwas was string example....wow!!! thwas was really string
		thwas was string example....wow!!! thwas is really string

join() 
	用于将序列中的元素以指定的字符连接生成一个新的字符串。
	字符串/字符串变量.join(sequence)
	参数
		- sequence -- 要连接的元素序列。
	symbol = "-"; seq = ("a", "b", "c"); 
	# 字符串序列 print symbol.join( seq );
	以上实例输出结果如下：a-b-c

pow(,)
	pow函数用于幂运算
	前一个参数表示底数，后一个参数表示幂次

`chr(n)`：
	它的作用：==**把一个 Unicode 编码变成对应字符**==。
	例如:chr(9802)
	会得到一个对应字符。
配对的有ord(n):
	ord() 函数是 chr() 函数（对于8位的ASCII字符串）或 unichr() 函数（对于Unicode对象）的配对函数
	它以一个字符（长度为1的字符串）作为参数，返回对应的 ASCII 数值，或者 Unicode 数值
	如果所给的 Unicode 字符超出了你的 Python 定义范围，则会引发一个 TypeError 的异常。
	ord(c)
		参数
			c -- 字符
		返回值
			返回值是对应的十进制整数。
		以下展示了使用 ord() 方法的实例：
			ord('a')
			97
			ord('b')
			98
			ord('c')
			99

 type(要判断的数据变量)
	 判断数据类型的函数

While循环与 Try except函数的联用
	while True:  
	    try:  
	        a = eval(input('请输入一个正整数:'))  
	        if a > 0 and ==**type(a)**== == int:  
	            print(a)  
	            ==**break**==  
	        else:  
	            print("请输入正整数")  
	    except:  
	        print("请输入正整数")

下标思想
	==**cnt += st[i + 1]**==
	这句最关键。
	为什么是 `i + 1`？
	因为：
	- `st[0]` 是姓名
	- `st[1]` 是英语
	- `st[2]` 是数学
	- `st[3]` 是 Python语言
	==**成绩是从下标 1 开始的，不是从下标 0 开始。**==
	所以：
	- 当 `i = 0` 时，取 `st[1]`
	- 当 `i = 1` 时，取 `st[2]`
	- 当 `i = 2` 时，取 `st[3]`
	也就是把三门成绩依次加起来。
	例如张三：90+87+95=272
	最后 `cnt` 就是 272。

unicore
	if ==**'\u4e00' <= c <= '\u9fff':**==
	Python 里的字符本质上都有编码值。  
	常用汉字大多落在 `\u4e00` 到 `\u9fff` 这个范围里。
	所以这句的意思是：“如果当前字符 `c` 的编码落在中文区间里，那就说明它是中文字符。”

列表相关函数
	append()：
		列表名.append(obj)
			- obj -- 添加到列表末尾的对象。
		返回值
			**append()** 方法==**向列表的尾部添加一个新的元素**==。
			而且要注意==**列表内元素下标的改变**==
		例如
			aList = [123, 'xyz', 'zara', 'abc'];
			aList.append( 2009 );
			print "Updated List : ", aList;
			以上实例输出结果如下：
			Updated List :  [123, 'xyz', 'zara', 'abc', 2009]
	insert()：
		列表名.insert(index, obj)
		参数
			- index -- 对象 obj 需要插入的索引位置。
			- obj -- 要插入列表中的对象。
		实例
			 aList = [123, 'xyz', 'zara', 'abc'] ;
			 aList.insert( 3, 2009) ;
			 print "Final List : ", aList;
			以上实例输出结果如下：
			Final List : [123, 'xyz', 'zara', 2009, 'abc'];
	注意append和insert的区分
		

 isnumeric() 
	这个函数检测字符串是否只由数字组成。这种方法只针对unicode对象。
	语法：字符串/字符串变量.isnumeric()
	没有参数
	如果字符串中只包含数字字符，则返回 True，否则返回 False
	例子
		str = u"this2009";  
		print str.isnumeric();
		str = u"23443434";
		print str.isnumeric();
		以上实例输出结果如下：
		False
		True

相应的有：
isalpha()
	该函数检测字符串是否只由字母组成。
	语法：字符串/字符串变量.isalpha()
	无参数
	如果字符串至少有一个字符并且所有字符都是字母则返回 True，否则返回 False。
	例子
		str = "runoob";  
		print str.isalpha();  
		str = "runoob菜鸟教程";  
		print str.isalpha();  
		str = "this is string example....wow!!!";  
		print str.isalpha();  
		以上实例输出结果如下：
		True
		False
		False
以及：
isdigit():
	判断：当前这个字符串是不是==**“全部由数字字符组成”。**==

time第三方库
	把一个时间戳（按秒计算的浮点数）转化为time.asctime()的形式
		asctime() 函数接受时间元组并返回一个可读的形式为"Tue Dec 11 18:07:14 2008"（2008年12月11日 周二18时07分14秒）的24个字符的字符串。
	如果参数未给或者为None的时候，将会默认time.time()为参数。
	time.ctime([ sec ])
	参数
		sec -- 要转换为字符串时间的秒数。
	实例
		import time
		print "time.ctime() : %s" % time.ctime()
		以上实例输出结果为：
		time.ctime() : Tue Feb 17 10:00:18 2013

random第三方库
	random.seed(123) 
		可以自由设定随机数种子
		==**固定一个随机数种子，进而保证得到的随机结果都固定**==
	`random.randint(1, 999)`  
		生成一个 1 到 999 之间的整数
		其中.randint(A,B),随机生成A到B之间的整数
	random.choice(列表/列表变量)
		从列表 里随机选一个元素


jieba第三方库
	jieba.lcut(变量/字符串)
		`lcut` 的意思你可以先简单记成：把一句中文切成一个“词语列表”
		例如：jieba.lcut("俄罗斯举办世界杯")
		得到的大概就是：['俄罗斯', '举办', '世界杯']