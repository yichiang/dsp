[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)
This is a classic example of hypothesis testing using the normal distribution. The effect size used here is the Z-statistic.

Exercise 5.1 In the BRFSS (see Section 5.4), the distribution of heights is
roughly normal with parameters  = 178 cm and  = 7.7 cm for men, and
 = 163 cm and  = 7:3 cm for women.
In order to join Blue Man Group, you have to be male between 5'10" and
6'1" (see http://bluemancasting.com). What percentage of the U.S. male
population is in this range? Hint: use scipy.stats.norm.cdf.

>> 
It asked for the percentage of the U.S. male population is in the range. Thus, we use  parameters  = 178 cm and  = 7.7 cm to get normal distribution. 
```
import scipy.stats
# The distribution of heights is roughly normal with parameters µ = 178 cm and σ = 7.7 cm for men
normalDistribution = scipy.stats.norm(178, 7.7)
# Percentage of the U.S. male population is between 5’10” and 6’1”
inchToCm=2.54
normalDistribution.cdf((6*12+1)* inchToCm) - normalDistribution.cdf((5*12+10)* inchToCm)
```
