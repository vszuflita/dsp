[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)


```python
import nsfg
import numpy as np
import thinkplot
import thinkstats2
import matplotlib.pyplot as plt

#Reading the file
fam = nsfg.ReadFemResp()

#Formula for finding pmf (unbiased)
kid_act_dis = thinkstats2.Pmf(fam.numkdhh, label= 'Actual distribution of Number of Kids per HH')

#Defining how to calculate the biased pmf. 
def BiasedPmf(pmf, label):
    new_pmf = pmf.Copy(label=label)
    
    for x, p in pmf.Items():
        new_pmf.Mult(x, x) #Multiplying each pmf by the number of kids who "experience" that kid per HH situation. 
        
    new_pmf.Normalize()
    return new_pmf
    
#Formula for finding biased pmf. 
kid_biased_dis = BiasedPmf(kid_act_dis, label='Biased distribution of Number of Kids per HH')

#Plotting the results. 
thinkplot.PrePlot(2)
thinkplot.Pmfs([kid_act_dis, kid_biased_dis])
thinkplot.Show(xlabel='Kids per HH', ylabel='PMF')

#Finding the mean for each distribution
print(kid_act_dis.Mean())
print(kid_biased_dis.Mean())
```

The mean for the actual distribution is: **1.024205155043831**

The mean for the biased distribution is: **2.403679100664282**

Here is the visual representation of the differences between the distributions:

