# Gredient Boosting Decision Tree

How predictions are updated by residuals
```
initialize y_pred = avg(y)

for i from 1 to N (iters)
    get decision rules of a single decison tree
    residual = y_pred - y
    get avg(residual) of each node
    update y_pred = y_pred(n-1) + lr * avg(residual) of the related nodes
for end
```

## Key idea
- In each iteration, building different trees by different features can help to fix the residual.
- Always get the avg for each node.
- Flexible parametes are in Sklearn, e.g. if use all data or subsamples to build each single tree. Lose function can be customized and the default is least squares regression (ls).


## Resources
- how GBDT works (StatQuest) https://www.youtube.com/watch?v=3CC4N4z3GJc
- extract decision rules https://stackoverflow.com/questions/20224526/how-to-extract-the-decision-rules-from-scikit-learn-decision-tree
- explian how GBDT works https://towardsdatascience.com/machine-learning-part-18-boosting-algorithms-gradient-boosting-in-python-ef5ae6965be4
