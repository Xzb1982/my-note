numpy 主要是干什么的  
	numpy 的核心对象是多维数组 `ndarray`。你把它理解成“高性能的数值矩阵”就行，它==**擅长做向量化运算、线性代数、随机数、统计汇总等。很多机器学习库最终都把数据变成 numpy 数组来算。**==
	内容
		numpy 里常用又实用的东西大概分几类：  
		1）创建与形状处理
		- `np.array` 把列表转成数组
		- `np.zeros / np.ones / np.full` 造全 0、全 1、全常数数组
		- `np.arange / np.linspace` 造等差序列或等分点
		- `reshape / ravel / transpose(T)` 改形状、拉平、转置
		- `np.concatenate / np.stack / np.hstack / np.vstack` 拼接数组
		2）索引与筛选
		- 布尔索引：`x[x>0]` 这种写法非常常用
		- `np.where` 做条件选择或找位置
		- `np.clip` 把数值裁剪到区间里，例如限制异常值
		3）统计与聚合
		- `np.sum / mean / std / min / max` 以及 `axis=` 按行按列汇总
		- `np.argmax / argmin` 找最大最小的位置
		- `np.cumsum / cumprod` 累计和、累计积
		4）线性代数
		- `np.dot` 和 `@` 做点积或矩阵乘法
		`np.linalg.inv / eig / svd / norm` 做逆矩阵、特征分解、奇异值分解、范数线性模型、PCA 这类方法背后都离不开这套东西。
	