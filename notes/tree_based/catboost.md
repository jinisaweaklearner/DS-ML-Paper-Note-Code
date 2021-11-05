# CatBoost: unbiased boosting with categorical features
**Published Year**: 2019 <br/>
**Author**: Yandex

- build symmetric trees
- categorical feature support
  - one hot encoding
  - target statistics (ts) based on category and lable value
- greedy constructed categorical feature combinations (interactions between features) 


![](https://cdn.mathpix.com/snip/images/6QpBdntWqWVNA5YADa56ym4vxR7AhdP6bmFMoKAH7JY.original.fullsize.png)


## Target statistics (TS)
if we use ts directly, there is a leakage problem.

formular of greedy ts

![](https://cdn.mathpix.com/snip/images/wFtDcMBr9HUsmhTZL1oTo4Z_mkCtfcQ4WeKxnhmKbXM.original.fullsize.png)

where a > 0 is a parameter. A common setting for p is the average target value in the dataset.

In CatBoost, ordered ts is used. We randomly rank observations and each time just use historical data to compute ts.
![](https://cdn.mathpix.com/snip/images/4OVKOEM9fxfXUpFTvj3Zc-BdWLjQBEEEvd0Zw7bYjdg.original.fullsize.png)

## resources
videos on the official website https://catboost.ai/docs/concepts/educational-materials-videos.html
