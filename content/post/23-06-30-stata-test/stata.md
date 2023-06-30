---
title: "Stata testing"
format: hugo
---

Python for fun:

``` python
print("Hey world")
```

    Hey world

Load some data

``` stata
sysuse auto
```

    (1978 automobile data)

Do a t-test

     . ttest mpg, by(foreign)

    Two-sample t test with equal variances
    ------------------------------------------------------------------------------
       Group |     Obs        Mean    Std. err.   Std. dev.   [95% conf. interval]
    ---------+--------------------------------------------------------------------
    Domestic |      52    19.82692     .657777    4.743297    18.50638    21.14747
     Foreign |      22    24.77273     1.40951    6.611187    21.84149    27.70396
    ---------+--------------------------------------------------------------------
    Combined |      74     21.2973    .6725511    5.785503     19.9569    22.63769
    ---------+--------------------------------------------------------------------
        diff |           -4.945804    1.362162               -7.661225   -2.230384
    ------------------------------------------------------------------------------
        diff = mean(Domestic) - mean(Foreign)                         t =  -3.6308
    H0: diff = 0                                     Degrees of freedom =       72

        Ha: diff < 0                 Ha: diff != 0                 Ha: diff > 0
     Pr(T < t) = 0.0003         Pr(|T| > |t|) = 0.0005          Pr(T > t) = 0.9997
