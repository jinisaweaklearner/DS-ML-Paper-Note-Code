# Papers, Notes and Code in Data Science and Machine learning

## Tree-based 

|Model Name | Category | Paper  | Notes   | Code  |
|---|:---:|:---:|:---:|:---:|
| Decision Tree (ID3,C4.5,CART) | -  | -  | [Notes](notes/tree_based/decision_tree.md)   |   |
| Random Forest  |  bagging |   |  [Notes](notes/tree_based/random_forest.md)  |    |
| AdaBoost: Adaptive Boosting  |  boosting |   | [Notes](notes/tree_based/adaboost.md) | [Code](https://github.com/jinisaweaklearner/DS-ML-Paper-Note-Code/blob/master/src/AdaboostClassification.ipynb)  |
| GBDT: Gradient Boosting Decision Tree  |  boosting |   | [Notes](notes/tree_based/gbdt.md)   | [Code](https://github.com/jinisaweaklearner/DS-ML-Paper-Note-Code/blob/master/src/GradientBoostingDecisionTree(GBDT).ipynb)  |
| LightGBM: A Highly Efficient Gradient Boosting Decision Tree |  boosting |[Paper](https://papers.nips.cc/paper/6907-lightgbm-a-highly-efficient-gradient-boosting-decision-tree.pdf) |  [Notes](notes/tree_based/lightgbm.md)  |   |
| XGBoost: A Scalable Tree Boosting System  |  boosting | [Paper](https://arxiv.org/pdf/1603.02754.pdf)  | [Notes](notes/tree_based/xgboost.md)   |   |
| CatBoost: unbiased boosting with categorical features  |  boosting | [Paper](https://arxiv.org/pdf/1706.09516.pdf) | [Notes](notes/tree_based/catboost.md)   |   |
| Deep Forest: Towards an Alternative to Deep Neural Networks  |  - | [Paper](https://arxiv.org/pdf/1702.08835v2.pdf) |  |[Github](https://github.com/kingfengji/gcForest)  |

## Recommender System
|Name |Paper|Notes|Code|Desc|
|---|:---:|:---:|:---:|:---:|
| NeuMF| [Paper](https://arxiv.org/pdf/1708.05031.pdf)  | -  | - | a combination of GMF and MLP  |
| GMF | - | -  | - | generalized matrix factorization with embedding |
| MLP | - | -  | - | multilayer perceptron with embedding|
| Wide & Deep | [Paper](https://arxiv.org/pdf/1606.07792.pdf)   | -  | - | embeding categorical and continuous features |
| Deep Neural Networks for YouTube Recommendations | [Paper](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/45530.pdf) | -  | - | -|


## Auto ML
- H2O AutoML [[Code]](http://docs.h2o.ai/h2o/latest-stable/h2o-docs/automl.html) 

## SVM
- SVM [[Notes]](notes/svm.md)

## Dimention Reduction
- PCA PCR PLS [[Notes]](notes/dimention_reduction.md)
- MDS
- t-SNE
- Auto Encoder

## Non Linear Methods
- Polynomial Regression [[Notes]](notes/nonlinear_methods.md)
- Step functions [[Notes]](notes/nonlinear_methods.md)
- Regression splines [[Notes]](notes/nonlinear_methods.md)
- Local Regression [[Notes]](notes/nonlinear_methods.md)
- Generalized additive models [[Notes]](notes/nonlinear_methods.md)

## NLP Pre-trained Model
- RoBERTa: A Robustly Optimized BERT Pretraining Approach [[Paper]](https://arxiv.org/pdf/1907.11692.pdf) [[Code]](src/RoBERTa_multi_class_yelp5.ipynb) 
- ULMFiT: Universal Language Model Fine-tuning for Text Classification [[Paper]](https://arxiv.org/pdf/1801.06146.pdf)
- GPT2: Language Models are Unsupervised Multitask Learners [[Paper]](https://d4mucfpksywv.cloudfront.net/better-language-models/language_models_are_unsupervised_multitask_learners.pdf) [[Code]](https://github.com/openai/gpt-2)
- BERT: Pre-training of Deep Bidirectional Transformers for
Language Understanding [[Paper]](https://arxiv.org/pdf/1810.04805.pdf)

## Sequential Model
|Name |Paper|Notes|Code|Desc|
|---|:---:|:---:|:---:|:---:|
| LSTM| [Paper](https://arxiv.org/pdf/1708.05031.pdf)  | -  | - | Long Short Term Memory |
| BiLSTM| - | -  | - | Bidirectional Long Short Term Memory |
| GRU| -  | -  | - | Gated Recurrent Unit |
| RNN| - | -  | - | Recurrent Neural Network |
| DeepAR| [Paper](https://arxiv.org/pdf/1704.04110.pdf)  | - | - | - |
| N-BEATS| [Paper](https://arxiv.org/pdf/1905.10437.pdf)  | - | - | - |


## Time Series Papers
|Paper Title |Notes|Desc|
|---|:---:|:---:|
|[FFORMA: Feature-based forecast model average](https://www.monash.edu/business/ebs/research/publications/ebs/wp19-2018.pdf) | - | 2nd place solution in M4 with 42 TS features|
|[A hybrid method of exponential smoothing and recurrent neural networks for time series forecasting](https://www.researchgate.net/publication/334556784_A_hybrid_method_of_exponential_smoothing_and_recurrent_neural_networks_for_time_series_forecasting) | - | 1st place solution in M4 with the combination of RNN and ETS|
|[M5 accuracy competition: Results, findings, and conclusions](https://statmodeling.stat.columbia.edu/wp-content/uploads/2021/10/M5_accuracy_competition.pdf) | - | M5 Summary |
|[Monash Time Series Forecasting Repository](https://forecastingdata.org/) | - | baseline |




## Traditional Time Series Forecasting
- Time Series Ebook [[Link]](https://otexts.com/fpp2/ets-forecasting.html)
- Naïve 
- Seasonal Naïve
- Simple Exponential Smoothing
- ARIMA
- Moving Averages 
- Prophet

## Rating System
- Elo [[wiki]](https://en.wikipedia.org/wiki/Elo_rating_system)
- Glicko [[Paper]](http://www.glicko.net/research/acjpaper.pdf)
- Glicko2 [[Code]](https://bitbucket.org/deepy/glicko2/src/default/)
- Trueskill: A Bayesian Skill Rating System  [[Web]](https://trueskill.org/) [[Paper]](https://www.microsoft.com/en-us/research/wp-content/uploads/2007/01/NIPS2006_0688.pdf)
- BBT https://github.com/DataWraith/bbt
- ELO-MMR https://github.com/EbTech/Elo-MMR


## Anomaly Detection
- Isolation Forest [[Paper]](https://cs.nju.edu.cn/zhouzh/zhouzh.files/publication/icdm08b.pdf?q=isolation-forest) [[Video]](https://www.youtube.com/watch?v=5p8B2Ikcw-k) 
- One-Class SVM
- Local Outlier Factor
- Robust Covariance


## Imbalanced Problem
* SMOTE: Synthetic Minority Over-sampling Technique [[Paper]](https://arxiv.org/pdf/1106.1813.pdf) [[Notes]](notes/Smote.md)

## Model Interpretation
* SHAP: A Unified Approach to Interpreting Model
Predictions [[Paper]](https://arxiv.org/pdf/1705.07874.pdf)
* LIME: “Why Should I Trust You?”
Explaining the Predictions of Any Classifier [[Paper]](https://cs.nju.edu.cn/zhouzh/zhouzh.files/publication/icdm08b.pdf?q=isolation-forest)

## Feature Selection, Engineering and Deduction
- mRMR: Maximum Relevance and Minimum Redundancy [[Paper]](http://home.penglab.com/papersall/docpdf/2005_TPAMI_FeaSel.pdf) [[Github]](https://github.com/fbrundu/pymrmr)
- Autoencoder

## Model Validation
- We need to talk about standard splits [[Paper]](https://pdfs.semanticscholar.org/94be/fec2a6d96e3a60fb8b77f2e161666743c1a5.pdf)
- Adversarial Validation: solve the problem  [[Part1]](http://fastml.com/adversarial-validation-part-one/) [[Part2]](http://fastml.com/adversarial-validation-part-two/) [[Video]](https://www.youtube.com/watch?v=7cUCDRaIZ7I) [[Code]](https://github.com/zjost/blog_code/blob/master/adversarial_validation/adversarial-validation-example.ipynb)

## AB Testing 
-  P Value, effect size and power analysis [[Notes]](notes/p_value.md)

## Resources
- mlu-explain - nice way to vis ML model https://mlu-explain.github.io/
