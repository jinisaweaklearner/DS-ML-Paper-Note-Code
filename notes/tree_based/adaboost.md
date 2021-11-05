# Adaboost

In short, Adaboost is to change the weights of observations based on errors. The observations with large errors will be assigned to higher weights.

## adaboost regressor
```
initial weights = 1/n (n: total number of observations)

for i from 1 to N (iters)
    1. get X_,y_ by bootstrapping (total number of observations is not changed)
    2. train model_ by X_,y_ and get y_pred
    3. err = abs(y - y_pred)
    4. normalize err (exclude right predictions)
    5. get the total weighted error for each observation
    6. more calculation; e.g. sum(weights * absolute error)
    7. update the weights for this iteration based on errors
    9. normalize the weights (sum up is 1)
for end

y_pred_final = median(y_pred)

e.g. if y_pred are 3,4,4 in 3 treed, then the final prediction is the medium(4)
```


## resources
- concepts of adaboost https://www.cs.toronto.edu/~mbrubake/teaching/C11/Handouts/AdaBoost.pdf
- adaboost for classfication with code https://geoffruddock.com/adaboost-from-scratch-in-python/
- ml notes in toronto https://www.cs.toronto.edu/~mbrubake/teaching/C11/notesReadings.html