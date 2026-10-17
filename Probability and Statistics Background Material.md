R usage (R语言)

To a data set , we can write a observation set:
{x1,x2,x3,....,xn}

we can summerize it by histogram
or some sample value
mean
or 标准差 standard deviation (sample's)

相同平均值，但是数据的离散程度是不一样的

例如![[Pasted image 20261017162640.png]]

Covariance

$$ \frac{1}{N-1} \sum^N_{i=1} (x_{i}- \bar{x}) (y_{i} - \bar{y}) $$
评判两个变量之间的变化方向

we need to make differences on sample and population(样本和总体)

such as ![[Pasted image 20261017163759.png]]

抽样分布 sample distribution
when we choose multiple times on the mean of the X

we can get a lot of X's mean

these means can make into a disturibution

无偏估计量   ——  one of the propreties on estimators

低方差：if 都无偏 unbianess , 那么 a lower variance estimator is better

MSE mean square error
![[Pasted image 20261017164745.png]]

![[Pasted image 20261017164904.png]]

there is a trade off on 高方差但是低无偏性；以及高无偏，低方差

这里的无偏性翻译错了应该是离差

假设检验 hypothesis test

we make two hypo  such as mean =0 or mean ≠0

![[Pasted image 20261017165648.png]]

分子是 离差，分母是对抽样分布标准差的估计

这里可以做t检验，t检验和自由度有关


normal distribution

uniform distribution

learning from data 
	pridiction & causal
	![[Pasted image 20261017171027.png]]
	the above structure is prediction 
	However, when we turn to causal , the following structure is :
	![[Pasted image 20261017171158.png]]
	一个是预测关系，一个是因果关系

different types data

截面数据 cross-sectional data

时间序列数据 time-series data

面板数据 panel data

![[Pasted image 20261017171901.png]]

dealing with the time series data
	log return or simple return
	![[Pasted image 20261017172341.png]]
	![[Pasted image 20261017172647.png]]


we make a portfolio 
![[Pasted image 20261017173024.png]]

![[Pasted image 20261017173033.png]]



概率公理

![[Pasted image 20261017174539.png]]

条件概率与贝叶斯定理

 Define the conditional probability
2. Create a partition of O2
3. Combine the partition and the conditional probabilitydefinitions to get the Partition Theorem
4. Take the conditional probability definition and use thepartition theorem in the denominator to get Bayes' theorem

为什么贝叶斯定理和分类模型


![[Pasted image 20261017175838.png]]
![[Pasted image 20261017175859.png]]

![[Pasted image 20261017180000.png]]
概率密度函数和概率

离散型随机变量的分布

伯努利分布

二项分布（n次独立重复试验的伯努利分布）

几何分布（特殊的二项分布）和超几何分布

泊松分布


连续性随机变量的分布

每个分布的应用是什么？

均匀分布是