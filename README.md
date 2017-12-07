# InterviewSources

 Dec 6th, 2017

 http://www.geeksforgeeks.org/find-the-two-repeating-elements-in-a-given-array/ Find the two repeating elements in a given array

http://www.cnblogs.com/LeftNotEasy/archive/2011/01/19/svd-and-applications.html  关于SVD的描述

https://www.springboard.com/blog/machine-learning-interview-questions/ 面试41问题

Dec 7th, 2017

https://www.quora.com/What-is-a-full-rank-matrix  矩阵秩的意义，秩和行或列的独立性有关，而行或列很难做到独立性，这意味着用求矩阵的逆的方法求解，有很大的局限
，在不是满秩的情况下，线性方程组有多个系数解，一般要引入正则项处理。

LR模型无需事先假定数据分布。logit函数有很好的性质，例如任意阶可导，所以可以用很多优化方法。根据凸函数理论，GD或NM都可求最优解。

LDA（线性判别分析）涉及SVD，用于解拉格郎日优化。

解决类别不平衡问题，“再缩放”（rescaling），欠采样（undersampling,EasyEnsemble),过采样（oversampling,SMOTE），阈值移动（threshold-moving）。

决策树：“分而治之”（divide-and-conquer）。信息熵（information entropy）是度量样本集合纯度最常用的一种指标。基尼指数（Gini index）用于CART。剪枝（pruning）用于对付过拟合。C4.5并没有直接填充缺失值，而是用概率知识把信息增益率的求解作些变化。

见 http://blog.csdn.net/bone_ace/article/details/46322815

神经网络：感知器因只有一层功能神经元，所以学习能力有限，只能解决线性可分问题。为解决非线性可分问题，必须加入隐藏层。多层网络的学习能力虽然强大，但需要更强大的学习算法。误差逆传播（error BackPropagation,BP）是迄今最成功的神经网络学习算法。神经元之间不存在同层连接，也不存在跨层连接。这样的神经网络结构通常称为“多层前馈神经网络”。 “链式法则”。读取训练集一遍称为进行了“一轮”（one round, or one eopch),标准BP和累计BP的区别类似于随机梯度下降和梯度下降之间的区别。BP神经网络常遭遇过拟合,策略是“早停”（early stopping），另一种策略是“正则化”（regularization）。跳出局部最小的策略：1、多组初始化参数值;2、模拟退火，每一步都以一定的概率接受比当前解更差的结果，“次优解”;3、SGD;4、GA。上述技术仍属于启发式的，理论上不保障。多隐层神经网络难以直接用BP训练，因为误差在多隐层内逆传播时，往往会“发散”（diverge）而不能收敛到稳定状态。pre-training预训练，fine-tuning微调。DBN。weight-sharing权共享，CNN。深度学习可以理解为feature-learning“特征学习”或representation-learning“表示学习”。


支持向量机：距离超平面最近的这几个训练样本，被称为“支持向量”（support vector）。
