

- [快手因果推断与实验设计](https://mp.weixin.qq.com/s/svVl1eiVUH6rOYG3p2YiGg)
  - 类型
    - Rubin虚拟事实模型（Potential Outcome）的核心是寻找合适的对照组, 比如：经济学上通过RCT实验，互联网常使用AB实验。
    - Pearl因果图模型（Causal Graph Model）：使用有向图描述变量之间的因果关系
  - 例子
    - 双重差分（Difference In Difference）变种；双重差分假设用户开始受影响的时间是一样的，实验处理效应对用户的影响是一样的，而这些假设难以满足。实际操作时对不同类型用户分别做DID估计，再进行加权平均，得到修正后DID实验效果值。
    - `当treatment施加到一个群体或者地区上时，很难找到单一的对照组.`这种时候采用合成控制方法构造虚拟对照组进行比较，原理是构造一个虚拟的对照组，通过treatment前的数据上学习的权重，拟合实验组在实验开始前的数据，模拟实验组用户在没有接受实验情况下的结果，构造合成控制组，实验开始后，评估实验组和合成控制组之间的差异。
  - 推荐策略的评估：因果推断与机器学习
    - 在因果推断上我们非常关心的是如何准确的估计结果以及结果的方差
    - 双重机器学习模型
        - 双重机器学习假设所有混淆变量都可以被观测，其正则化过程能够达到高维变量选择的目的，与Frisch-Waugh-Lovell定理相似，模型通过正交化解决正则化带来的偏差。
    - 因果随机森林模型
    - Meta-Learner for Uplift Modeling
  - 因果图
    - Constraint-based Algorithms
    - Score-based Algorithms

  - 双边实验设计
    - 优势：同时进行了主播侧和观众侧的分流，可以更准确的算出效应
    - 劣势：当结果全面铺开时，往往结果不如预期
  - 时间片轮转实验
    - 实验对象在AB 2组反复切换