# Lasso & Ridge
- Lasso and Ridge are shrinkage methods.
- use all predictors/features
- have a shrinkage penalty
- lambda is the key parameter
- motivation
  - aviod overfitting by using complex models

## Lasso (Least Absolute Shrinkage and Selection Operator)
![](https://cdn.mathpix.com/snip/images/t_Dvu6LQ7aKuNYUGcinnD4gQDkKTJLYylGSsVZewVyI.original.fullsize.png)
- we also call Lasso as L1 regularization
- penalizes the sum of their absolute values (L1 penalty)
- similar to feature selection

## Ridge (L2)
![](https://cdn.mathpix.com/snip/images/6So22RakzVd4dEeBl4PYNHWVXfIsRpoNJQj0dwP3isM.original.fullsize.png)
- penalizes sum of squared coefficients (the so-called L2 penalty)

## Lasso vs Ridge
- In Lasso, some coefficients can be 0 
- Ridge regression will perform better when the response is a function of many predictors, all with coefficients of roughly equal size
- The lasso to perform better in a setting where a relatively small number of predictors have substantial coefficients.
- we have L1 and L2, why not use L3 L4 ...etc?
- what is actually L1 and L2 norm?
![](https://cdn.mathpix.com/snip/images/CKDvc-0dH7hddnuHEbqdS-H0rlPdW2E8L4NzMNJoC9g.original.fullsize.png)

## Shape of L1 and L2 (videoes)
- [Lasso](https://youtu.be/jbwSCwoT51M)
- [Ridge](https://youtu.be/5asL5Eq2x0A)

