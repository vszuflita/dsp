[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

```python
import numpy as np
import thinkplot
import thinkstats2
import matplotlib.pyplot as plt

#Picking random numbers between 1-1000
randos = np.random.random(1000)

#Assigning random numbers PMFs
rando_pmfs = thinkstats2.Pmf(randos, label='PMF')
thinkplot.Pmf(rando_pmfs)
thinkplot.Show(xlabel = 'Random number between 0-1000', ylabel="PMF")
```

It's almost impossible to see the distribution:

![PMF](https://github.com/vszuflita/dsp/blob/master/img/output_5_0.png)


```python
#Assigning random numbers CDFs
rando_cdfs = thinkstats2.Cdf(randos, label='CDF')
thinkplot.Cdf(rando_cdfs)
thinkplot.Show(xlabel = 'Random number between 0-1000', ylabel="CDF")
```

The distribution is almost perfectly uniform:

![CDF](https://github.com/vszuflita/dsp/blob/master/img/output_6_0.png)

