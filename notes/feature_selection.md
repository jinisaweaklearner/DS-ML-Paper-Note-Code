## Feature Selection

## Permutation feature importance
- impurity-based importances are biased towards high cardinality features
- impurity-based importances are computed on training set statistics and therefore do not reflect the ability of feature to be useful to make predictions that generalize to the test set (when the model has enough capacity)
- impurity-based importances are generated based on the training part, but permutation feature importance could be calculated by both training and testing datsets
### examples
- random features test https://scikit-learn.org/stable/auto_examples/inspection/plot_permutation_importance.html#sphx-glr-auto-examples-inspection-plot-permutation-importance-py
- ermutation Importance with Multicollinear or Correlated Features https://scikit-learn.org/stable/auto_examples/inspection/plot_permutation_importance_multicollinear.html#sphx-glr-auto-examples-inspection-plot-permutation-importance-multicollinear-py
- https://scikit-learn.org/stable/auto_examples/ensemble/plot_gradient_boosting_regression.html#sphx-glr-auto-examples-ensemble-plot-gradient-boosting-regression-py
- https://scikit-learn.org/stable/auto_examples/ensemble/plot_forest_importances.html#sphx-glr-auto-examples-ensemble-plot-forest-importances-py

### SKlearn
- Permutation feature importance overview https://scikit-learn.org/stable/modules/permutation_importance.html
- https://scikit-learn.org/stable/modules/generated/sklearn.inspection.permutation_importance.html#sklearn.inspection.permutation_importance
- source code https://github.com/scikit-learn/scikit-learn/blob/1fc86b6aacd89da44a3b4e8abf7c3e2ba4336ffe/sklearn/inspection/_permutation_importance.py
- source code parallel test for each feature/column https://github.com/scikit-learn/scikit-learn/blob/1fc86b6aacd89da44a3b4e8abf7c3e2ba4336ffe/sklearn/inspection/_permutation_importance.py#L260
- source code repalce the existing values with the shuffled values https://github.com/scikit-learn/scikit-learn/blob/1fc86b6aacd89da44a3b4e8abf7c3e2ba4336ffe/sklearn/inspection/_permutation_importance.py#L61