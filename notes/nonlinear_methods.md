# Non-linear methods

## Polynomial Regression
- extends the linear model by adding extra predictors, obtained by raising each of the original predictors to a power.
- Generally speaking, it is unusual to use d greater than 3 or 4 because for large values of d, the polynomial curve can become overly flexible and can take on some very strange shapes.
## Step functions
- need to create cut points
- cut the range of a variable into K distinct regions and avoid impose a global structure.

## Regression splines
- regression spline is a combination of two ideas (d)
- Continuous Piecewise Cubic: the fitted curve must be continuous
- Cubic Spline: both the first and second derivatives of the piecewise polynomials are continuous
<img> <img src="https://cdn.mathpix.com/snip/images/V9vr2cxat-QN4l3OOt9iI3A6BMAYYFJdtq2h07p59to.original.fullsize.png" />
## Smoothing splines

- bad side:
  - high variance at the outer range of the predictors
## Local regression
- using only the nearby training observations
- Assign a weight Ki0 = K(xi, x0) to each point in this neighborhood, so that the point furthest from x0 has weight zero, and the closest has the highest weight. All but these k nearest neighbors get weight zero.

## Generalized additive models
- a general framework for extending a standard linear model by allowing non-linear functions of each of the variables, while maintaining additivity.
<img> tag: <img src="https://cdn.mathpix.com/snip/images/fbMyipcGxXv1W_Wk4PBFKMrHpsYgnc2aZutEVC-NmqQ.original.fullsize.png" />