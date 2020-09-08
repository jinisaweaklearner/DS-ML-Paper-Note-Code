# Normalization

## Min-Max
Highlights:
- Min-Max transforms the numerical variable into a new range. i.e. 0 to 1
- The distribution won't be changed after normalization.

Scaling to a range is a good choice when both of the following conditions are met:
- You know the approximate upper and lower bounds on your data with few or no outliers.
- Your data is approximately uniformly distributed across that range.
- Be careful about 0 and negative values 

## Log Scale
why log scale? Log scale can help to identy the parttern of values in different ranges.

Eaxmaple

The two time series plots below show monthly visitor arrivals to New Zealand, available from Statistics New Zealand. You can see that the seasonality in arrivals stays roughly proportional to the scale of the arrivals; and you can see the significant changes in growth rate (eg during the second world war) which are just invisible on the original scale.
![](https://i.stack.imgur.com/IYF9Q.png)

Other examples: https://dfrieds.com/data-visualizations/when-use-log-scale.html


## Standardization (z-score normalization)
use z-score to ensure your feature distributions have mean = 0 and std = 1

It’s useful when there are a few outliers, but not so extreme that you need clipping.

![](https://developers.google.com/machine-learning/data-prep/images/norm-z-score.svg)



https://www.codecademy.com/articles/normalization#:~:text=Min%2Dmax%20normalization%20is%20one,decimal%20between%200%20and%201.
![](https://s3.amazonaws.com/codecademy-content/courses/normalization/z-score.png)
