[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

```python
resp = nsfg.ReadFemResp()
pmf = thinkstats2.Pmf(resp.numkdhh, label='actual kids in hh')
biased_pmf = BiasPmf(pmf, label='observed kids in hh')
thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf, biased_pmf])
thinkplot.Config(xlabel='Family Size', ylabel='PMF')
print('Actual mean', pmf.Mean())
print('Observed mean', biased_pmf.Mean())
print(pmf.Items())```
