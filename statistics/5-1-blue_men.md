[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

```python
import brfss
df = brfss.ReadBrfss()
df = df[df.sex == 1]
htin = df.htm3/2.54
# 5'10" = 70 in // 6'1" = 73 in
count_in = len(htin[htin>=70]) - len(htin[htin>=73])
count_out = len(htin)-count_in
print("There are",count_in,"men between 5\'10\" (70 in) and 6\'1\" (73 in), and",
      count_out,"men outside of this range.\nThis represents",str(int(count_in/len(htin)*100)/100)+
      "% of the population of men in the sample data.")
pmf = thinkstats2.Pmf(htin,label="Heights of Men")
thinkplot.Hist(pmf)
```
