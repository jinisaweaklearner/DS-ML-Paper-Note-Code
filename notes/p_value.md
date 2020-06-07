# P Value

- P value is unstable when there are only very few samples (dance of P value).
- coiffience / standard error (how many standard errors far away) = Z score



##### which alpha (threshold) will be chosen in a/b testing? why?

Based on where you want to use it.  In maunfact or medicent testing, the thresthold could be very small. In general, **0.05 is fine to reject null hypothesis **(no diff between two groups).



##### Definiton of P Value

Suppose p is 0.03, if we still believe the null hypothesis is true, the probability to see it is 0.03.

##### Defiition of effect size (d)

- The estimated difference in the means / pooled estimated standard deviations 

- s1 and s2 are the standard deviations of each group

   <img src="https://cdn.mathpix.com/snip/images/B0KcFQg544LhdK_nBzjMhK8WowuEy_yFTrzO-sTlmwE.original.fullsize.png" />



##### Defintion of Power Analysis (avoid False Positive)

- determin the sample size for the next time we do experiments.

- Use Power anlysis to get enough number of observations to make decisions.

- The value of power is from 0 to 1. Commonly, power is 0.8.

- Use threshold of significance (alpha), power and effect size to get sample size.

- To get the overlap between two distributions, we need to calculate effect size.

- If there is a big overlap, we may need a large amount of samples.

  

Example

If alpha is 0.05, power is 0.8 and effective size is 1.5. By using statistical power calculator, the sample size is 9.

In other words, if I get 9 observations in each group, I will have 80% chance that I will correctly reject the null hypothesis.



##### Absense of envidence is not envidence of absense



##### Videos

- Be careful about P hacking https://www.youtube.com/watch?v=HDCOUXE3HMM
- Power anlysis https://www.youtube.com/watch?v=VX_M3tIyiYk