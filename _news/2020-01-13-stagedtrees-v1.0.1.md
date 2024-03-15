---
layout: default
title:  "stagedtrees v1.0.1"
---

The new version of the R-package stagedtrees is available on
[CRAN](https://cran.r-project.org/package=stagedtrees). 

This new version implements some bug fixes and two new functions:
`get_stage` and `get_path`.

The new functions can be used to obtain the stage associated to a given
path or viceversa, the paths relative to a given stage.

``` r
model <- PhDArticles[,1:3] %>% full %>% bhc.sevt

get_stage(model, c(Articles = "1-2",Gender = "male"))
```

    ## [1] "5"

``` r
get_path(model, "Kids", 5)
```

    ##   Articles Gender
    ## 1        0   male
    ## 3      1-2   male
    ## 5       >2   male

### News

  - fix \#73; naive.sevt not passing distance arg
  - fix `indep`, probabilities should not be of class table (it was
    triggering a bug in summary)
  - fix `subtree`, now removing unused probabilities (it was triggering
    a bug in summary)
  - fixing testing without long double
  - fixing some errors in testing
  - update some tests with unquoted expression
  - new functions `get_stage` and `get_path` and relative tests
