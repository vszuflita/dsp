[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

```python
import numpy as np

import math

import nsfg

#Reading the data

preg = nsfg.ReadFemPreg()

#Cleaning the variables we're planning to use. "totalwgt_lb" will add both the lbs and the oz, and create a new column in our set. 

def CleanFemPreg(df):
    df.birthwgt_lb.replace(na_vals, np.nan, inplace=True)
    df.birthwgt_oz.replace(na_vals, np.nan, inplace=True)
    df['totalwgt_lb']= df.birthwgt_lb + df.birthwgt_oz / 16.0

#Selecting for "live births" only, and assigning them to variable "live". 

live = preg[preg.outcome == 1]

#Assigning whether babies are "first babies" or "not first babies", so we can compare. 

first = live[live.birthord ==1]
others = live[live.birthord !=1]

#Calculating Cohen's D, using the standard formula.

"""The Cohen's D Formula is described as... the difference between the means of the two groups, divided by the pooled standard deviation. The pooled standard deviation is defined as the square root of the size of group 1 added to the variation in group one, added to the size of group 2 added to the variation in group 2, divided by the sum of the sizes of group 1 and 2. """

def CohensD(first, others):
    diff = first.mean() - others.mean()
    
    var1 = first.var()
    var2 = others.var()
    
    n1= len(first)
    n2 = len(others)
    
    pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
    d = diff / math.sqrt(pooled_var)
    
    return(d)

CohensD(first.totalwgt_lb, others.totalwgt_lb)
```

Cohen's D: -0.088672927072602
