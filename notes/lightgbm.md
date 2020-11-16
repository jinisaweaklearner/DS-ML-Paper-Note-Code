# LightGBM: A Highly Efficient Gradient Boosting Decision Tree
Published Year: 2017 <br/>
Author: Microsoft

**Motivation**

The efficiency and scalability are still unsatisfactory when the feature dimension is high and data size is large.

**Issues** 

- In GBDT, we need to enumerates all possible split points, which is inefficient.
- GBDT is trained in sequence.

**Solutions**
1. Gradient-based One-Side Sampling (GOSS)
2. Exclusive Feature Bundling (EFB)

**GBDT and Its Complexity Analysis**

To find the best split points:
- pre-sorted algorithm
which enumerates all possible split points on the pre-sorted feature values --> inefficient in both `training speed` and `memory consumption`


### 1. Gradient-based One-Side Sampling

- `exclude` a significant proportion of data instances with `small gradients`, and only use the rest to estimate the information gain.

- data instances with `different gradients play different roles ` in the computation of information gain. In particular, accor---ding to the definition of information gain, those instances with larger gradients (i.e., under-trained instances) will contribute more to the information gain. 

- Therefore, when down sampling the data instances, in order to retain the accuracy of information gain estimation, we should better keep those instances with large gradients (e.g., larger than a pre-defined threshold, or among the top percentiles), and only randomly drop those instances with small gradients.

- if an instance is associated `with a small gradient`, the training error for this instance is `small` and it is already `well-trained`.

**Pseudocode of GOSS** 
```
Inputs: 
I: training data 
d: iterations
a: sampling ratio of large gradient data
b: sampling ratio of small gradient data 
loss: loss function 
L: weak learner 

models ← {}
fact ← (1−a)/b 
topN ← a × len(I) 
randN ← b × len(I) 

for i = 1 to d do:
    # 1. get predictions
    preds ← models.predict(I) 

    # 2. get gradients based on loss
    g ← loss(I, preds), w← {1,1,...} 

    # 3. sort gradients for each observation
    sorted ← GetSortedIndices(abs(g)) 

    # 4. get top N based on gradients
    topSet ← sorted[1:topN] 

    # 5. randomly select from the rest
    randSet ← RandomPick(sorted[topN:len(I)], randN) 

    # 6. combine 2 parts from step 4 and 5
    usedSet ← topSet + randSet

    # 7. Assign weight fact to the small gradient data. 
    w[randSet] × = fact 
    
    # train the new model based on the used dataset
    newModel ← L(I[usedSet], − g[usedSet], w[usedSet])
    
    # store the new model
    models.append(newModel)
```

### 2. Exclusive Feature Bundling

- feature space is quite `sparse`
- they rarely take `nonzero values` simultaneously
- the histogram-based algorithm `stores discrete bins` instead of continuous values of the features, we can construct a feature bundle by letting exclusive features reside in different bins.
- Example:
Suppose we have two features in a feature bundle. Originally, feature A takes value from `[0, 10)` and feature B takes value `[0, 20)`. We then add an offset of 10 to the values of feature B so that the refined feature takes values from [10, 30). After that, it is safe to merge features A and B, and use a feature bundle with range `[0, 30]` to replace the original features A and B.
