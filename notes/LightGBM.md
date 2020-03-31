# LightGBM: A Highly Efficient Gradient Boosting Decision Tree
Published Year: 2017 <br/>
Author: Microsoft

**Motivation**

The efficiency and scalability are still unsatisfactory when the feature dimension is high and data size is large.

**Issues** 

For each feature, need to scan all the data instances to estimate the `information gain` of all possible split points, which is very `time consuming`.

**Solutions**
1. Gradient-based One-Side Sampling (GOSS)
2. Exclusive Feature Bundling (EFB)

**GBDT and Its Complexity Analysis**
To find the best split points:
- pre-sorted algorithm
which enumerates all possible split points on the pre-sorted feature values --> inefficient in both `training speed` and `memory consumption`
- histogram-based algorithm

**Related work**

reduce the number of features -> filter weak features -> principle component analysis or projection pursuit | assume features contain significant redundancy -> not always be true in practice (features

**Gradient-based One-Side Sampling**

- exclude a significant proportion of data instances with small gradients, and only use the rest to estimate the information gain.

- data instances with `different gradients play different roles ` in the computation of information gain. In particular, accor---ding to the definition of information gain, those instances with larger gradients (i.e., under-trained instances) will contribute more to the information gain. 

- Therefore, when down sampling the data instances, in order to retain the accuracy of information gain estimation, we should better keep those instances with large gradients (e.g., larger than a pre-defined threshold, or among the top percentiles), and only randomly drop those instances with small gradients.

- if an instance is associated with a small gradient, the training error for this instance is small and it is already well-trained.

**Pseudocode of GOSS** <br/>
Inputs: <br/>
I: training data <br/>
d: iterations <br/>
a: sampling ratio of large gradient data <br/>
b: sampling ratio of small gradient data <br/>
loss: loss function <br/>
L: weak learner <br/>

models ← {} <br/>
fact ← (1−a)/b <br/>
topN ← a × len(I) <br/>
randN ← b × len(I) <br/>

for i = 1 to d do: <br/>
&emsp;&emsp; preds ← models.predict(I) <br/>
&emsp;&emsp; g ← loss(I, preds), w← {1,1,...} <br/>
&emsp;&emsp; sorted ← GetSortedIndices(abs(g)) <br/>
&emsp;&emsp; topSet ← sorted[1:topN]  <br/>
&emsp;&emsp; randSet ← RandomPick(sorted[topN:len(I)], randN) <br/>
&emsp;&emsp; usedSet ← topSet + randSet <br/>
&emsp;&emsp; w[randSet] × = fact |  Assign weight fact to the small gradient data. <br/>
&emsp;&emsp; newModel ← L(I[usedSet], − g[usedSet], w[usedSet]) <br/>
&emsp;&emsp; models.append(newModel) <br/>

**Exclusive Feature Bundling**

- feature space is quite `sparse`
- they rarely take `nonzero values` simultaneously
- the histogram-based algorithm `stores discrete bins` instead of continuous values of the features, we can construct a feature bundle by letting exclusive features reside in different bins.
- Example:
Suppose we have two features in a feature bundle. Originally, feature A takes value from `[0, 10)` and feature B takes value `[0, 20)`. We then add an offset of 10 to the values of feature B so that the refined feature takes values from [10, 30). After that, it is safe to merge features A and B, and use a feature bundle with range `[0, 30]` to replace the original features A and B.
