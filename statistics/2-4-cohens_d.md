[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

Exercise 4   Using the variable `totalwgt_lb`, 

investigate whether first babies are lighter or heavier than others. Compute Cohen’s d to quantify the difference between the groups. 


Notes - 

effect size: `A summary statistic intended to quantify the size of an effect like a difference between groups.`

firsts.totalwgt_lb.mean()
`7.201094430437772`
others.totalwgt_lb.mean()
`7.325855614973262`
CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)
`-0.08867292707260174`

How does it compare to the difference in `pregnancy length`?

firsts.prglngth.mean()
`38.60095173351461`
others.prglngth.mean()
`38.52291446673706`
CohenEffectSize(firsts.prglngth, others.prglngth)
`0.028879044654449834`
