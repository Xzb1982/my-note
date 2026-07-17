主要做什么
	pandas 的核心对象是 `Series` 和 `DataFrame`。==**你可以把 DataFrame 理解成“带行列标签的 Excel 表”，但它比 Excel 强在：读写方便、清洗方便、分组统计方便、时间序列处理方便，并且能和 numpy、sklearn 无缝对接。**==
内容
	pandas 里最有用的一批功能通常是：  
	1）读写数据
	- `pd.read_csv / read_excel` 读文件
	- `df.to_csv / to_excel` 导出结果  
	    项目里，数据整理的一半时间都在这块。
	2）选取与过滤
	- `df.loc` 按标签选，`df.iloc` 按位置选
	- `df.query` 用字符串写筛选条件也很爽
	- `df.sort_values` 排序
	3）缺失值与类型处理
	- `df.isna / df.dropna / df.fillna` 查缺失、删缺失、填缺失
	- `df.astype` 强制类型转换
	- `pd.to_datetime` 把日期字符串变成时间类型  
	    这一步如果做不好，后面模型经常会报错。
	4）合并与变形
	- `pd.merge` 像 SQL 一样按键连接两张表
	- `df.join / concat` 拼表
	- `df.pivot_table` 做透视表
	- `df.melt` 宽表转长表  
	    做因子表、面板数据、特征表时特别常用。
	5）分组统计与滚动窗口
	- `df.groupby(...).agg(...)` 分组聚合，例如均值、计数、分位数
	- `df.rolling(window).mean()` 滚动均值
	- `df.resample('D')` 时间重采样  
	    金融时间序列和特征工程里这类操作出现频率很高。
	6）快速体检
	- `df.head / tail / info / describe` 看数据概况
	- `df.value_counts` 统计类别频数
	- `df.duplicated / drop_duplicates` 去重