[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

```ce_totwt = CohenEffectSize(firsts.totalwgt_lb,others.totalwgt_lb)
```print(ce_totwt)

```print("Cohen Effect of Total Weight (Firsts vs Others):",ce_totwt)
```print("Cohen Effect of Pregnancy Length (Firsts vs Others):",ce_prglngth)
```if abs(ce_totwt) > abs(ce_prglngth):
```    print("Total Weight is",str(ce_totwt/ce_prglngth)+"x larger than Pregnancy Length")
```else:
```    print("Pregnancy Length is",str(ce_prglngth/ce_totwt)+"x larger than Total Weight")
