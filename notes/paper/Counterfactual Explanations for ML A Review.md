**Counterfactual Explanations for ML: A Review**

因果解释可以是基于模型(model-specific)或模型无关(model-agnostic)的：

model-specific: 特征重要性；模型简化

model-agnostic: 可视化; 本地解释（local explanation); 特征重要性; 模型简化

可解释性：模型可解释性和结果可解释性

**Counterfactual Explanations:**

1.如何改变input使得prediction改变

2.改变的约束：

(1)validity: $\underset{x'}{arg min} \space d(x,x')$ subject to $f(x')=y'$

(2)actionability: 限制x'的取值范围$x'\in A$

(3)sparsity: 使改变的特征的数量尽可能少-->加$g(x'-x)$约束

(4)data manifold closeness: 改变后的features应尽可能和训练数据的分布接近

$l(x';X)$, $X$为训练集

(5)causality: 特征间往往不独立，改变一个特征，对其他特征的影响

反事实解释算法的限制：

(6)amortized inference: 解优化问题代价高，amortized inference允许算法为input x 快速计算counterfactual，而不用解优化问题

(7)alternative methods: 线性规划，混合整数规划，SMT

**Assessment of The Approaches on Counterfactual Properties**:

(1)model access: 算法对模型访问的需求程度：模型内部/梯度/预测函数

(2)model agnostic

(3)optimization amortization: 学习从datapoints到counterfactuals的映射，学习一个variational auto-encoder（VAE），对所有数据点都适用

amortized inference: 一个算法对所有数据点适用；multiple counterfactual: 一个数据点提供多个解

(4)counterfactual attributes: 

causal graph, 表示不同特征间的联系

(5)counterfactual optimization problem attributes: 



**open questions**:

(1)unify counterfactual explanations with traditional "explainable AI"

(2)provide counterfactual explanations as discrete and sequential steps of actions 提供连续的改变过程

(3)











