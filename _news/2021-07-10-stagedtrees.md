---
layout: default
title:  "stagedtree v2.2.0"
---

A new minor version of the `stagedtrees` package is available 
on [CRAN](https://cran.r-project.org/package=stagedtrees). 

Numerous new functions are available, such as a 
confidence interval method, likelihood ratio test and 
chain event graph plotting using the `igraph` package.  

#### NEWS 

* `plot.ceg` new plotting functions using `igraph` plotting.
* new util function `make_stages_col` which help computing 
  stages colors for `sevt` and `ceg` plotting.
* `sample_from` now returns a data.frame of factors. 
* `prob` earns a new argument `conditional_on`, that 
   makes easier to compute conditional probabilities. 
* `confint.sevt`, implement a method for confidence intervals
   for the parameters of a model of class `sevt`. 
* `lr_test` new function, implementing likelihood-ratio 
   test.
* functions to search optimal staged trees among different orders:
  `search_best` and `search_greedy`.
* `cid` function that implements context intervention discrepancy
* more and better testing and documentation.
