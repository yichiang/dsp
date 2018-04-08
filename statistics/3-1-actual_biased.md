[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)
This problem presents a robust example of actual vs biased data. As a data scientist, it will be important to examine not only the data that is available, but also the data that may be missing but highly relevant. You will see how the absence of this relevant data will bias a dataset, its distribution, and ultimately, its statistical interpretation.

Questions: 
Exercise 3.1 Something like the class size paradox appears if you survey
children and ask how many children are in their family. Families with many
children are more likely to appear in your sample, and families with no chil-
dren have no chance to be in the sample.
Use the NSFG respondent variable NUMKDHH to construct the actual distribu-
tion for the number of children under 18 in the household.
Now compute the biased distribution we would see if we surveyed the children
and asked them how many children under 18 (including themselves) are in
their household.
Plot the actual and biased distributions, and compute their means. As a
starting place, you can use chap03ex.ipynb

>> 
```
resp = nsfg.ReadFemResp()
print(resp['numkdhh'])
resp['numkdhh'].value_counts()
```
>
```
0    3563
1    1636
2    1500
3     666
4     196
5      82
Name: numkdhh, dtype: int64
```


```
resp['numkdhh'].value_counts()/resp['numkdhh'].size
```
>
```
0    0.466178
1    0.214052
2    0.196258
3    0.087139
4    0.025644
5    0.010729
Name: numkdhh, dtype: float64
```

```
pmf = thinkstats2.Pmf(resp['numkdhh'], label='numkdhh')
pmf
```
> Pmf({0: 0.466178202276593, 1: 0.21405207379301322, 2: 0.19625801386889966, 3: 0.08713855815779145, 4: 0.025644380478869556, 5: 0.01072877142483318})
```
thinkplot.Pmf(pmf)
thinkplot.Config(xlabel='number of children', ylabel='PMF')
```
```
biasedDistribution = BiasPmf(pmf, label='biased distribution')
type(biasedDistribution)
```
> thinkstats2.Pmf

```
biasedDistribution
```
> Pmf({0: 0.0, 1: 0.20899335717935616, 2: 0.38323965252938175, 3: 0.25523760858456823, 4: 0.10015329586101177, 5: 0.052376085845682166})
```
pmf.Mean()
```
> 1.024205155043831

```
biasedDistribution.Mean()
```
> 2.403679100664282


```
thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf, biasedDistribution])
thinkplot.Config(xlabel='number of children', ylabel='PMF')

```


#Notes
I am still confused about BiasedPmf. 