为啥需要数据预处理
	现实世界中的数据往往存在**噪声（Noisy）、不完整（Incomplete）和不一致（Inconsistent）** 
	噪声数据
		① 错误值（Erroneous Values）：例如，工资为 -10K，显然不符合正常情况。
		② 非预期值（Unexpected Values）：例如，当数据集中其他人的工资都处于 30K～50K 区间时，某个人的工资却达到 100K。
	数据不完整
		① 缺少所关注的属性（Missing Attributes of Interest）：例如，数据集中完全没有职业信息这一字段。
		② 缺失值（Missing Values）：例如，虽然数据集中存在职业（Occupation）这一字段，但某些记录的职业信息为空，即 `occupation = ""`。
	数据不一致
		数据之间存在差异或不统一
		例如，不同大学的学生评分标准可能不同，因此各大学之间的学生评分可能存在不一致的问题。
	这样的数据会对结果造成不良的影响
那么怎么做数据预处理呢？
	 数据清洗（Data Cleaning）
		① 填补缺失值（Fill in Missing Values）；
		② 平滑噪声数据（Smooth Noisy Data），减少数据中的噪声或随机波动；
		③ 识别或删除异常值（Identify or Remove Outliers）；
		④ 解决数据不一致的问题（Resolve Inconsistencies）。