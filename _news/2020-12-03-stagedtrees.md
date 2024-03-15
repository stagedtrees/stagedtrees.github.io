---
layout: default
title:  "stagedtrees v2.0.0"
---

A major update of stagedtrees (v2.0.0) is available on 
[CRAN](https://cran.r-project.org/package=stagedtrees).

 The update will almost surely break any code written with v1.0.2. Functions naming and functions parameters have been updated to simplify user experience. Check the complete changelog for details.

# 2.0.0

This version introduces major changes, in functions capabilities
and in functions naming. 
These changes are almost surely breaking any previous code 
using older versions of the package.
In particular, all functions named `*.sevt` but class methods are now
called differently.
Moreover, various improvements and functionalities are added 
to better deal with unobserved situations and to improve 
computations. 
Additional model selection methods based on clustering are
now available.

COMPLETE CHANGELOG:

* DESCRIPTION updated.
* documentation updated.
* improve code comments.
* reduced exported functions.
* removed the `fit` parameter from `full`, `indep`. 
   Now `full` and `indep` always fit the model while
  `sevt` is just the basic constructor of the `sevt` class.
* in `full` and `indep` by default unobserved situations are joined
  using `join_unobserved`, and probabilities are fitted only after 
  the unobserved situations are joined, improving speed. Moreover, the 
  name of the unobserved stages are stored as `name_unobserved` in the 
  staged tree object.
* update internal function `new_label` to improve speed.
* `plot.sevt` allows now to set edges color with 
   `col_edges`.
* In `plot.sevt` and `barplot.sevt` it
  is possible to specify stages that should be ignored
  and not plotted via the `ignore` argument, by default the 
  `name_unobserved` stages are ignored.
* `plot.sevt` adds variables names by default (`var_names` argument).
* fix in `compare_stages`: because of changes in `plot.sevt` 
  we need to specify that the root is always considered identical.
* internal function `stndnaming` accepts now `uniq`, `prefix` and  
  `ignore` arguments, which control how stage names are generated and   
  if some stage names should be left untouched (default: the `name_unobserved`
  stages). 
* in `stages_bj` (previously `bj.sevt`) distance is now passed with a 
  character and no longer as a function.
* two new model selection function: `stages_hclust` and 
  `stages_kmeans`, to learn stage structure using hierarchical or        
  k-means clustering.
*  all model selection functions accept `scope` and `ignore`   
   parameters that allow to specify among which variables
   run the algorithm and which stages should be left untouched 
   (default: the `name_unobserved` stages). 
*  replace `1:length(x)` with the suggested `seq_along` in all code.
* distance names in `stages_bj` and `stages_hclust` are compatibles.
* fixed bug in some probability distance functions when 0 probabilities. 
* Conversion generic function `as.sevt`, only implemented one method 
  for `bn.fit` class from bnlearn package
* fix `inclusions_stages` and provide better output. 

