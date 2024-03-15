---
layout: default
title:  "stagedtrees preprint and new version"
---

Preprint describing [stagedtrees](https://cran.r-project.org/package=stagedtrees) is
available on [arxiv](https://arxiv.org/abs/2004.06459). 

A new version (1.0.2) of stagedtrees is also available on [CRAN](https://cran.r-project.org/package=stagedtrees), below the summary of changes, in particular a new function
is available to visualize stage probabilities. 

# 1.0.2

* fix bug in `summary`, stages were wrongly matched to probabilities
* new function `barplot_stages` to draw barplots of the 
  floret probabilities. Implemented relative tests.
* new example in `plot.sevt`.
* now `order` can be passed to `staged_ev_tree.bn.fit`
* `join_zero` alias for `join_zero_counts` 
* more tests  


