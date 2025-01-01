---
title: "An Rmarkdown post"
subtitle: ""
excerpt: "testing the excerpt field"
date: 2020-12-30
author: "Alison Hill"
draft: false
images:
series:
tags:
categories:
layout: single
---


```r
knitr::opts_chunk$set(fig.path = "figs/", collapse = TRUE)
```

## An empty post

<i class="fas fa-mug-hot"></i> woot

Yay fontawesome works.

## Well let's try penguins


```r
library(tidyverse)
## -- Attaching packages --------------------------------------- tidyverse 1.3.0 --
## v ggplot2 3.3.2     v purrr   0.3.4
## v tibble  3.0.4     v dplyr   1.0.2
## v tidyr   1.1.2     v stringr 1.4.0
## v readr   1.4.0     v forcats 0.5.0
## -- Conflicts ------------------------------------------ tidyverse_conflicts() --
## x dplyr::filter() masks stats::filter()
## x dplyr::lag()    masks stats::lag()
library(palmerpenguins)
## Warning: package 'palmerpenguins' was built under R version 4.0.4
```


```r
ggplot(data = penguins, aes(x = flipper_length_mm)) +
  geom_histogram(aes(fill = species), alpha = 0.5, position = "identity") +
  scale_fill_manual(values = c("darkorange","darkorchid","cyan4"))
## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
## Warning: Removed 2 rows containing non-finite values (stat_bin).
```

<img src="figs/unnamed-chunk-3-1.png" width="672" />


