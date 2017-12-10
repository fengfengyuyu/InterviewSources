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

支持向量机：距离超平面最近的这几个训练样本，被称为“支持向量”（support vector）。 对偶问题，KKT条件，SMO。核函数相当于把两个样本映射到特征空间之后的内积，由于特征空间维数可能很高，甚至可能是无穷维，因此直接计算内积是非常困难的，这就有了核函数的价值。“再生核希尔伯特空间，RKHS）。soft-margin软间隔，非凸、非连续，数学性质不好，不易求解，“替代损失”（surrogate loss）函数一般具有较好的数学性质。SVM可以得到近似LR模型，两者性能相当，LR可以给出概率值。Lp范数（norm）是常用的正则化项，L2范数倾向于非零分量个数尽量稠密，L0范数和L1范数倾向于非零分量个数尽量少。表示定理（representer theorem）。核函数直接决定了支持向量机与核方法的最终性能。核函数选择一直未决，多核学习可看成集成学习。
 
贝叶斯分类器：最小化分类错误率的贝叶斯最优分类器，首先要获得后验概率。机器学习所要实现的是基于有限的训练样本集尽可能准确地估计出后验概率。主要有两种策略：给定x，通过直接建模P（c|x)来预测c，这样得到的模型叫“判别式模型”;也可先对联合概率分布P（x,c)建模，然后再由此获得P(c|x)，这样得到的是“生成式模型”。DT、BP、SVM都是判别式模型。类先验概率，根据大数定律，训练集包含充足的独立同分布样本时，P(c)可通过各类样本出现的频率来进行估计。

Dec 10th,2017

想写一个R脚本的sgd，差点把自己坑了。

http://www.stat.cmu.edu/~cshalizi/402/programming/writing-functions.pdf 如何写r 的function

https://machinelearningmastery.com/implement-linear-regression-stochastic-gradient-descent-scratch-python/ 大哥，你这个博客太多糟点了，坑人啊

http://www.cnblogs.com/louyihang-loves-baiyan/p/5136447.html 这个有点靠谱，但不能这么写

http://ruder.io/optimizing-gradient-descent/ 各种gradient descent的介绍


