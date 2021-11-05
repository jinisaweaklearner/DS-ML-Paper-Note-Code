# XGBoost: A Scalable Tree Boosting System
Published Year: 2016 <br/>
Author: Chen Tianqi


## TREE BOOSTING IN A NUTSHELL

### Regularized Learning Objective

![](https://cdn.mathpix.com/snip/images/yoaHR9Jdwwyo4t2l1o0UJHPOcFGsKWDpm8QScwjBv4A.original.fullsize.png)
```
T: the number of leaves
w: leaf weights
Ω penalizes the complexity of the model
```

- a continuous score on each of the leaf, we use wi to represent score on i-th leaf.
- the regularized objective will tend to select a model employing simple and predictive functions.

**Shrinkage**
- Shrinkage scales newly added weights by a factor η after each step of tree boosting.
- Similar to a learning rate in tochastic optimization, shrinkage reduces the influence of each individual tree and leaves space for future trees to improve the model.


**Column Subsampling**
- column sub-samples also speeds up computations of the parallel algorithm.
- subsampling columns not only reduces running time, and but also gives a bit higher performance for this problem. This could due to the fact that the subsampling helps prevent overfitting, which is observed by many of the users.

**Gradient Tree Boosting**

take first and second order gradient (change and the change of change) into consideration

Second-order approximation can be used to quickly optimize the objective in the general setting (`Taylor Expansion`).

![](https://cdn.mathpix.com/snip/images/F3ujJpo-JnxfSJcRE73YCTGWIdFyPChI2KCZnrG1bw8.original.fullsize.png)

- g is the loss of first order
- f is the loss of second order

more resources about taylor expansion
- https://en.wikipedia.org/wiki/Taylor_series
- https://en.wikipedia.org/wiki/Taylor's_theorem

![](img/xgboost-formula.png)
![](https://cdn.mathpix.com/snip/images/XA9lsjWoD2AiKJGNQ5HXhfLFGSPhbtW296W1zNhChe0.original.fullsize.png)

This formula is usually used in practice for evaluating the split candidates.

**Find split points**

The local proposal refines the candidates after splits, and can potentially be more appropriate for deeper trees. We find that the local proposal indeed requires fewer candidates. The global proposal can be as accurate as the local one given enough candidates.

**Approximate Algorithm**

To summarize, the algorithm first proposes candidate splitting points according to percentiles of feature distribution (a specific criteria will be given in Sec. 3.3). The algorithm then maps the continuous features into buckets split by these candidate points, aggregates the statistics and finds the best solution among proposals based on the aggregated statistics.

**Handle missing values**
![Missing values](img/xgboost-missingvalue.png)


## resources
- xgboost https://xgboost.readthedocs.io/en/latest/tutorials/model.html
- vis https://www.mariofilho.com/can-gradient-boosting-learn-simple-arithmetic/