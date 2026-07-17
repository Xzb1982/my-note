`sklearn` 的全名是 scikit-learn，==**它是一个“传统机器学习工具箱”。它的优势不是某个模型特别强，而是流程特别规范：数据预处理、划分训练测试、交叉验证、调参、评估指标、管道化流水线，这些都能用统一接口串起来。**==你看到的 `StandardScaler`、`MLPClassifier`、`accuracy_score` 都是这个体系里的组件。

内容
	sklearn 里最常用、最值得熟悉的模块我建议你按“机器学习流水线”来记：  
	1）数据预处理 preprocessing
	- `StandardScaler` 标准化，做的是  
	    对每个特征：`x' = (x - μ) / σ`  
	    神经网络、SVM、KNN 这类对尺度敏感的模型通常需要它。
	- `MinMaxScaler` 归一化到区间
	- `OneHotEncoder` 类别变量独热编码
	- `PolynomialFeatures` 生成多项式特征
	2）缺失值处理 impute
	- `SimpleImputer` 用均值、中位数、众数等填补
	3）数据集切分与验证 model_selection
	- `train_test_split` 划分训练集与测试集
	- `cross_val_score` 交叉验证评分
	- `GridSearchCV / RandomizedSearchCV` 网格搜索与随机搜索调参
	4）把步骤串起来 pipeline 与 compose
	- `Pipeline` 把“标准化→模型”封装成一个对象，避免数据泄漏
	- `ColumnTransformer` 对不同列做不同预处理，例如数值列做标准化、类别列做独热
	5）常见模型分类与回归
	- 线性模型 `LinearRegression / LogisticRegression / Ridge / Lasso`
	- 树与集成 `DecisionTreeClassifier / RandomForestClassifier / GradientBoostingClassifier / HistGradientBoostingClassifier`
	- 支持向量机 `SVC`
	- 近邻 `KNeighborsClassifier`
	- 神经网络 `MLPClassifier`  
	    你现在用的 `MLPClassifier` 就是多层感知机分类器。
	6）指标评估 metrics  
	你导入的三个都很典型：
	- `accuracy_score(y_true, y_pred)`：准确率，等于预测正确的比例
	- `confusion_matrix(y_true, y_pred)`：混淆矩阵，输出一个计数表，告诉你每个真实类别被分到哪些预测类别
	- `classification_report(y_true, y_pred)`：汇总每一类的 precision、recall、F1 和 support  
	    另外也很常用的还有：`precision_score / recall_score / f1_score / roc_auc_score / mean_squared_error / r2_score` 等。
	    