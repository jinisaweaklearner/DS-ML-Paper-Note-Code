# Dimention Reduction
## Principal Components Analysis
- motivations 
  - producing derived variables for use in supervised learning problems
  - PCA also serves as a tool for data visualization
- target
  - find a low-dimensional representation of the data that captures as much of
the information as possible
- definition of first principal component
  - (normalised) linear combination of the variables (X1 X2...Xp) with the largest variance.
- two ways to interpret PCA:
  - maximize the variance of features after dimention reduction
  - minimise the sum of the squared perpendicular distances
- principal conponent scores (z)
  - z = phi * (value of features - avg value)
- proportion of variance explained (PVE) by each proportion of variance explained principal component
  - var(phi * (x - mean of x)) / var(x)


## Principal Component Regression
- definition
  - transform the predictors and then fit a least squares model (linear regression) using the transformed variables.
- assumption
  - use less features and overcome overfitting
- PCR is not a feature selection method


## Partial Least Squares
- What is similar to PCR
  - First identifies a new set of features Z1 Z2...ZM that are linear
combinations of the original features.
  - Then, fits a linear model via least squares using these M new features.
- What is different to PCR
  - Use the response variable Y to supervise the learning of Z1 Z2... ZM so
that the direction found by PLS can explain `both the response and the
predictors`.
