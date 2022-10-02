---
title: "Why visualize data?"
date: 2019-03-01

type: book
toc: false
draft: true
aliases: ["/dataviz_why.html", "/notes/why-visualize-data/"]
categories: ["dataviz"]

weight: 21
---





Research methods classes in graduate school generally teach important skills such as probability and statistical theory, regression, analysis of variance (ANOVA), maximum likelihood estimation (MLE), etc. While these are important methods for analyzing data and assessing research questions, sometimes drawing a picture (aka **visualization**) can be more precise than conventional statistical computations.[^dozen]

Consider the following 13 data sets. What are the corresponding relationships between $X$ and $Y$? Using traditional metrics, the relationships appear identical across the samples:


| ID| $N$| $\bar{X}$| $\bar{Y}$| $\sigma_{X}$| $\sigma_{Y}$|    $R$|
|--:|---:|---------:|---------:|------------:|------------:|------:|
|  1| 142|      54.3|      47.8|         16.8|         26.9| -0.064|
|  2| 142|      54.3|      47.8|         16.8|         26.9| -0.069|
|  3| 142|      54.3|      47.8|         16.8|         26.9| -0.068|
|  4| 142|      54.3|      47.8|         16.8|         26.9| -0.064|
|  5| 142|      54.3|      47.8|         16.8|         26.9| -0.060|
|  6| 142|      54.3|      47.8|         16.8|         26.9| -0.062|
|  7| 142|      54.3|      47.8|         16.8|         26.9| -0.069|
|  8| 142|      54.3|      47.8|         16.8|         26.9| -0.069|
|  9| 142|      54.3|      47.8|         16.8|         26.9| -0.069|
| 10| 142|      54.3|      47.8|         16.8|         26.9| -0.063|
| 11| 142|      54.3|      47.8|         16.8|         26.9| -0.069|
| 12| 142|      54.3|      47.8|         16.8|         26.9| -0.067|
| 13| 142|      54.3|      47.8|         16.8|         26.9| -0.066|

$X$ and $Y$ have the same mean and standard deviation in each dataset, and the correlation coefficient (Pearson's $r$) is virtually identical. If we estimated linear regression models for each dataset, we would obtain virtually identical coefficients (again suggesting the relationships are identical):

<img src="{{< blogdown/postref >}}index_files/figure-html/datasaurus-lm-1.png" width="672" />

But what happens if we draw a picture?[^dozen-pic]


```
## Warning: No renderer available. Please install the gifski, av, or magick package
## to create animated output
```

```
## NULL
```

<img src="{{< blogdown/postref >}}index_files/figure-html/datasaurus-graph-static-1.png" width="768" />

Remarkably each of the datasets have the same summary statistics and linear relationships, yet they are drastically different in appearance! A good picture tells the reader much more than any table or text can provide.

# Session Info



```
## - Session info ---------------------------------------------------------------
##  setting  value
##  version  R version 4.1.3 (2022-03-10)
##  os       Windows 10 x64 (build 19044)
##  system   x86_64, mingw32
##  ui       RTerm
##  language (EN)
##  collate  English_United States.1252
##  ctype    English_United States.1252
##  tz       America/Chicago
##  date     2022-10-02
##  pandoc   2.17.1.1 @ C:/Program Files/RStudio/bin/quarto/bin/ (via rmarkdown)
## 
## - Packages -------------------------------------------------------------------
##  package       * version    date (UTC) lib source
##  assertthat      0.2.1      2019-03-21 [1] CRAN (R 4.1.3)
##  backports       1.4.1      2021-12-13 [1] CRAN (R 4.1.2)
##  blogdown        1.11       2022-08-09 [1] CRAN (R 4.1.3)
##  bookdown        0.28       2022-08-09 [1] CRAN (R 4.1.3)
##  broom         * 1.0.1      2022-08-29 [1] CRAN (R 4.1.3)
##  bslib           0.4.0      2022-07-16 [1] CRAN (R 4.1.3)
##  cachem          1.0.6      2021-08-19 [1] CRAN (R 4.1.3)
##  cellranger      1.1.0      2016-07-27 [1] CRAN (R 4.1.3)
##  class           7.3-20     2022-01-16 [2] CRAN (R 4.1.3)
##  cli             3.3.0      2022-04-25 [1] CRAN (R 4.1.3)
##  codetools       0.2-18     2020-11-04 [2] CRAN (R 4.1.3)
##  colorspace    * 2.0-3      2022-02-21 [1] CRAN (R 4.1.3)
##  crayon          1.5.1      2022-03-26 [1] CRAN (R 4.1.3)
##  datasauRus    * 0.1.6      2022-05-04 [1] CRAN (R 4.1.3)
##  DBI             1.1.3      2022-06-18 [1] CRAN (R 4.1.3)
##  dbplyr          2.2.1      2022-06-27 [1] CRAN (R 4.1.3)
##  dials           1.0.0      2022-06-14 [1] CRAN (R 4.1.3)
##  DiceDesign      1.9        2021-02-13 [1] CRAN (R 4.1.3)
##  digest          0.6.29     2021-12-01 [1] CRAN (R 4.1.3)
##  dplyr         * 1.0.9      2022-04-28 [1] CRAN (R 4.1.3)
##  ellipsis        0.3.2      2021-04-29 [1] CRAN (R 4.1.3)
##  evaluate        0.16       2022-08-09 [1] CRAN (R 4.1.3)
##  fansi           1.0.3      2022-03-24 [1] CRAN (R 4.1.3)
##  farver          2.1.1      2022-07-06 [1] CRAN (R 4.1.3)
##  fastmap         1.1.0      2021-01-25 [1] CRAN (R 4.1.3)
##  forcats       * 0.5.2      2022-08-19 [1] CRAN (R 4.1.3)
##  foreach         1.5.2      2022-02-02 [1] CRAN (R 4.1.3)
##  fs              1.5.2      2021-12-08 [1] CRAN (R 4.1.3)
##  furrr           0.3.1      2022-08-15 [1] CRAN (R 4.1.3)
##  future          1.28.0     2022-09-02 [1] CRAN (R 4.1.3)
##  future.apply    1.9.1      2022-09-07 [1] CRAN (R 4.1.3)
##  gargle          1.2.0      2021-07-02 [1] CRAN (R 4.1.3)
##  generics        0.1.3      2022-07-05 [1] CRAN (R 4.1.3)
##  gganimate     * 1.0.8      2022-09-08 [1] CRAN (R 4.1.3)
##  ggplot2       * 3.3.6      2022-05-03 [1] CRAN (R 4.1.3)
##  globals         0.16.1     2022-08-28 [1] CRAN (R 4.1.3)
##  glue            1.6.2      2022-02-24 [1] CRAN (R 4.1.3)
##  googledrive     2.0.0      2021-07-08 [1] CRAN (R 4.1.3)
##  googlesheets4   1.0.1      2022-08-13 [1] CRAN (R 4.1.3)
##  gower           1.0.0      2022-02-03 [1] CRAN (R 4.1.2)
##  GPfit           1.0-8      2019-02-08 [1] CRAN (R 4.1.3)
##  gtable          0.3.1      2022-09-01 [1] CRAN (R 4.1.3)
##  hardhat         1.2.0      2022-06-30 [1] CRAN (R 4.1.3)
##  haven           2.5.1      2022-08-22 [1] CRAN (R 4.1.3)
##  here            1.0.1      2020-12-13 [1] CRAN (R 4.1.3)
##  highr           0.9        2021-04-16 [1] CRAN (R 4.1.3)
##  hms             1.1.2      2022-08-19 [1] CRAN (R 4.1.3)
##  htmltools       0.5.2      2021-08-25 [1] CRAN (R 4.1.3)
##  httr            1.4.4      2022-08-17 [1] CRAN (R 4.1.3)
##  ipred           0.9-13     2022-06-02 [1] CRAN (R 4.1.3)
##  iterators       1.0.14     2022-02-05 [1] CRAN (R 4.1.3)
##  jquerylib       0.1.4      2021-04-26 [1] CRAN (R 4.1.3)
##  jsonlite        1.8.0      2022-02-22 [1] CRAN (R 4.1.3)
##  knitr         * 1.40       2022-08-24 [1] CRAN (R 4.1.3)
##  labeling        0.4.2      2020-10-20 [1] CRAN (R 4.1.1)
##  lattice         0.20-45    2021-09-22 [2] CRAN (R 4.1.3)
##  lava            1.6.10     2021-09-02 [1] CRAN (R 4.1.3)
##  lhs             1.1.5      2022-03-22 [1] CRAN (R 4.1.3)
##  lifecycle       1.0.1      2021-09-24 [1] CRAN (R 4.1.3)
##  listenv         0.8.0      2019-12-05 [1] CRAN (R 4.1.3)
##  lubridate       1.8.0      2021-10-07 [1] CRAN (R 4.1.3)
##  magrittr        2.0.3      2022-03-30 [1] CRAN (R 4.1.3)
##  MASS            7.3-55     2022-01-16 [2] CRAN (R 4.1.3)
##  Matrix          1.4-0      2021-12-08 [2] CRAN (R 4.1.3)
##  modelr          0.1.9      2022-08-19 [1] CRAN (R 4.1.3)
##  munsell         0.5.0      2018-06-12 [1] CRAN (R 4.1.3)
##  nnet            7.3-17     2022-01-16 [2] CRAN (R 4.1.3)
##  parallelly      1.32.1     2022-07-21 [1] CRAN (R 4.1.3)
##  parsnip         1.0.2      2022-10-01 [1] CRAN (R 4.1.3)
##  pillar          1.8.1      2022-08-19 [1] CRAN (R 4.1.3)
##  pkgconfig       2.0.3      2019-09-22 [1] CRAN (R 4.1.3)
##  prettyunits     1.1.1      2020-01-24 [1] CRAN (R 4.1.3)
##  prodlim         2019.11.13 2019-11-17 [1] CRAN (R 4.1.3)
##  progress        1.2.2      2019-05-16 [1] CRAN (R 4.1.3)
##  purrr         * 0.3.4      2020-04-17 [1] CRAN (R 4.1.3)
##  R6              2.5.1      2021-08-19 [1] CRAN (R 4.1.3)
##  Rcpp            1.0.9      2022-07-08 [1] CRAN (R 4.1.3)
##  readr         * 2.1.2      2022-01-30 [1] CRAN (R 4.1.3)
##  readxl          1.4.1      2022-08-17 [1] CRAN (R 4.1.3)
##  recipes         1.0.1      2022-07-07 [1] CRAN (R 4.1.3)
##  reprex          2.0.2      2022-08-17 [1] CRAN (R 4.1.3)
##  rlang           1.0.4      2022-07-12 [1] CRAN (R 4.1.3)
##  rmarkdown       2.16       2022-08-24 [1] CRAN (R 4.1.3)
##  rpart           4.1.16     2022-01-24 [2] CRAN (R 4.1.3)
##  rprojroot       2.0.3      2022-04-02 [1] CRAN (R 4.1.3)
##  rsample         1.1.0      2022-08-08 [1] CRAN (R 4.1.3)
##  rstudioapi      0.14       2022-08-22 [1] CRAN (R 4.1.3)
##  rvest           1.0.3      2022-08-19 [1] CRAN (R 4.1.3)
##  sass            0.4.2      2022-07-16 [1] CRAN (R 4.1.3)
##  scales          1.2.1      2022-08-20 [1] CRAN (R 4.1.3)
##  sessioninfo     1.2.2      2021-12-06 [1] CRAN (R 4.1.3)
##  stringi         1.7.6      2021-11-29 [1] CRAN (R 4.1.2)
##  stringr       * 1.4.1      2022-08-20 [1] CRAN (R 4.1.3)
##  survival        3.2-13     2021-08-24 [2] CRAN (R 4.1.3)
##  tibble        * 3.1.8      2022-07-22 [1] CRAN (R 4.1.3)
##  tidyr         * 1.2.0      2022-02-01 [1] CRAN (R 4.1.3)
##  tidyselect      1.1.2      2022-02-21 [1] CRAN (R 4.1.3)
##  tidyverse     * 1.3.2      2022-07-18 [1] CRAN (R 4.1.3)
##  timeDate        4021.106   2022-09-30 [1] CRAN (R 4.1.3)
##  tune            1.0.0      2022-07-07 [1] CRAN (R 4.1.3)
##  tweenr          2.0.1      2022-08-22 [1] CRAN (R 4.1.3)
##  tzdb            0.3.0      2022-03-28 [1] CRAN (R 4.1.3)
##  utf8            1.2.2      2021-07-24 [1] CRAN (R 4.1.3)
##  vctrs           0.4.1      2022-04-13 [1] CRAN (R 4.1.3)
##  withr           2.5.0      2022-03-03 [1] CRAN (R 4.1.3)
##  workflows       1.1.0      2022-09-26 [1] CRAN (R 4.1.3)
##  xfun            0.30       2022-03-02 [1] CRAN (R 4.1.3)
##  xml2            1.3.3      2021-11-30 [1] CRAN (R 4.1.3)
##  yaml            2.3.5      2022-02-21 [1] CRAN (R 4.1.2)
##  yardstick       1.1.0      2022-09-07 [1] CRAN (R 4.1.3)
## 
##  [1] C:/Users/Sabrina Nardin/Documents/R/win-library/4.1
##  [2] C:/Program Files/R/R-4.1.3/library
## 
## ------------------------------------------------------------------------------
```

[^dozen]: Example drawn from [*The Datasaurus Dozen* by Justin Matejka and George Fitzmaurice](https://www.autodeskresearch.com/publications/samestats).
[^dozen-pic]: Source code from [Recreating the Datasaurus Dozen Using `tweenr` and `ggplot2`](https://www.wjakethompson.com/post/datasaurus-dozen/) and [Reanimating the Datasaurus](https://r-mageddon.netlify.com/post/reanimating-the-datasaurus/).
