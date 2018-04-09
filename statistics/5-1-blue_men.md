[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

```python

import scipy

#These are the given values for mean and standar deviation. 
mu = 178
sigma = 7.7

#These are the cm values of the range of acceptable male heights for the group. 
lower = 177.8 #5'10
upper = 185.42 #6'1

#Calculating the normalize cdf for the upper and lower ranges. What percentage of men fall below the upper height? The lower?
percentlower = scipy.stats.norm.cdf(lower, mu, sigma)
percentupper = scipy.stats.norm.cdf(upper, mu, sigma)

#Calculating the percentage in between... those eligable to audition. 
bluemen = percentupper - percentlower

print(bluemen)
```

The formula returns **0.343** , meaning, 34.3% of men are eligable to audtion for the group. 
