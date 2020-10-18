# Support Vector Machines
SVM was developed in the computer science community in the 1990s.

## Maximal Margin Classifier
- Hyperplane: In a p-dimensional space, a hyperplane is a flat affine subspace of dimension p−1

- key step: compute the (perpendicular) distance from each training observation to a given separating hyperplane

- drawbacks:
  - cannot find linear decesion boundary
  - some noisy data can change the hyperplane (sensitivity problem)

## Support vector classifier / Soft Margin Classifier
- use soft margin (allow some observations to be on the incorrect side of the margin, or even the incorrect side of the hyperplane)

- the tuning parameter: C
  - when C > 0: no more than C observations can be on the wrong side of the hyperplane.
  - Large C: wide margin, many support vectors, highly fit to the data, high bias, low variance
  - Small C: narrow margin, few support vectors, fit the data less hard, low bias, high variance

- The support vector classifier’s decision rule is based only on the support vectors

- definition of support vectors: Observations that lie directly on the margin, or on the wrong side of the margin for their class, are known as support vectors.

- problem: still fail on non-linear decision boundary

## Support Vector Machine
- we consider enlarging the feature space using functions of the predictors (kernels)
- different kernels
  - linear
  - polynomial (computes the inner-product)
  - RBF (radial basis function)


