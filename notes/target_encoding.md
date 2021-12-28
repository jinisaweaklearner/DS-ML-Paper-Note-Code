motivation: encode categorical variables
existing solution: 
- One hot encoding
    - sparse
- Label encoding
    - convert each value in a column to an integerert | misunderstand


### Definition of target encoding
The idea is to calculate the mean value of the target column “y” (the column to predict), for each distinct element in the categorical column “x” and then replace each element in “x” with the associated mean. This is why it is also known as the “mean target encoding”.


### Reference
- https://medium.com/rapids-ai/target-encoding-with-rapids-cuml-do-more-with-your-categorical-data-8c762c79e784
- https://maxhalford.github.io/blog/target-encoding/
- other encoding methods https://wrosinski.github.io/fe_categorical_encoding/#:~:text=Count%20encoding%20is%20based%20on,can%20be%20replaced%20with%201%20.