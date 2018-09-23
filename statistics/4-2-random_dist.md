[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

```python
rand_one_k = np.random.random(1000)
pmf_r1k = thinkstats2.Pmf(rand_one_k,label='random numbers')

thinkplot.preplot(1)
thinkplot.Hist(pmf_r1k, align='left', width=width)
thinkplot.Config(xlabel='random numbers', ylabel='PMF')
```
It looks like the distribution of random numbers is uniform. This casts some doubt as to the 'randomness' of the random numbers as even random numbers don't result in a completely uniform distribution.

```python
cdf_r1k = thinkstats2.Cdf(rand_one_k,label='random_numbers')
thinkplot.Hist(cdf_r1k, align='left', width=width)
thinkplot.Config(xlabel='random numbers', ylabel='PMF')
```

Plotting the CDF it no longer appears to be a uniform distribution as there is some wavyness to the cdf.
