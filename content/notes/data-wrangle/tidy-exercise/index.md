---
title: "Practice tidying data"
date: 2022-10-13

type: book
toc: true
draft: false
aliases: ["/datawrangle_tidy_exercise.html", "/notes/tidy-exercise/"]
categories: ["datawrangle"]

weight: 38
---




```r
library(tidyverse)
```


{{% callout note %}}
Run the code below in your console to download this exercise as a set of R scripts.
```r
usethis::use_course("css-materials/data-wrangling-tidy-data")
```
{{% /callout %}}


For each exercise, tidy the data frame. Before you write any code examine the structure of the data frame and mentally (or with pen-and-paper) sketch out what you think the tidy data structure should be.

## Race data


```r
library(rcis)
race
```

```
## # A tibble: 4 x 8
##   Name   `50` `100` `150` `200` `250` `300` `350`
##   <chr> <dbl> <dbl> <dbl> <dbl> <dbl> <dbl> <dbl>
## 1 Carla   1.2   1.8   2.2   2.3   3     2.5   1.8
## 2 Mace    1.5   1.1   1.9   2     3.6   3     2.5
## 3 Lea     1.7   1.6   2.3   2.7   2.6   2.2   2.6
## 4 Karen   1.3   1.7   1.9   2.2   3.2   1.5   1.9
```

Important info:

* `Name` - pretty obvious
* `50`:`350` - column names define different lengths of time
* Cell values are scores associated with each name and length of time

{{< spoiler text="Click for a hint" >}}

**Tidy data structure**


```
## # A tibble: 28 x 3
##    Name   Time Score
##    <chr> <dbl> <dbl>
##  1 Carla    50   1.2
##  2 Carla   100   1.8
##  3 Carla   150   2.2
##  4 Carla   200   2.3
##  5 Carla   250   3  
##  6 Carla   300   2.5
##  7 Carla   350   1.8
##  8 Mace     50   1.5
##  9 Mace    100   1.1
## 10 Mace    150   1.9
## # ... with 18 more rows
```

{{< /spoiler >}}

{{< spoiler text="Click for the solution" >}}


```r
pivot_longer(
  data = race,
  cols = -Name,
  names_to = "Time",
  values_to = "Score",
  # ensure the Time column is stored as a numeric column
  names_transform = parse_number
)
```

```
## # A tibble: 28 x 3
##    Name   Time Score
##    <chr> <dbl> <dbl>
##  1 Carla    50   1.2
##  2 Carla   100   1.8
##  3 Carla   150   2.2
##  4 Carla   200   2.3
##  5 Carla   250   3  
##  6 Carla   300   2.5
##  7 Carla   350   1.8
##  8 Mace     50   1.5
##  9 Mace    100   1.1
## 10 Mace    150   1.9
## # ... with 18 more rows
```

Except for the `Name` column, the remaining columns are actually one variable spread across multiple columns. The column names are a distinct variable, and the columns' values are another variable. `pivot_longer()` is the appropriate function.

{{% callout note %}}

Because the column names are actually numeric values, we use `names_transform = parse_number` to coerce the new `Time` column into a numeric column. `names_transform` allows us to manually specify the column type for the `names_to` column. `parse_number()` is a function from the `readr` package for converting a character vector to a numeric vector, so `names_transform = parse_number` ensures the `Time` column is stored as a numeric column.

{{% /callout %}}

{{< /spoiler >}}

## Grades


```r
grades
```

```
## # A tibble: 12 x 6
##       ID Test     Year  Fall Spring Winter
##    <dbl> <chr>   <dbl> <dbl>  <dbl>  <dbl>
##  1     1 Math     2008    15     16     19
##  2     1 Math     2009    12     13     27
##  3     1 Writing  2008    22     22     24
##  4     1 Writing  2009    10     14     20
##  5     2 Math     2008    12     13     25
##  6     2 Math     2009    16     14     21
##  7     2 Writing  2008    13     11     29
##  8     2 Writing  2009    23     20     26
##  9     3 Math     2008    11     12     22
## 10     3 Math     2009    13     11     27
## 11     3 Writing  2008    17     12     23
## 12     3 Writing  2009    14      9     31
```

This one is a bit tougher. Important info:

* **The unit of analysis is ID-Year-Quarter.** That is, in the tidy formulation each observation represents one individual during one quarter in a given year.
* **Each test is unique.** As in they should be treated as two separate variables.

{{< spoiler text="Click for a hint" >}}

**Tidy data structure**


```
## # A tibble: 18 x 5
##       ID  Year Quarter  Math Writing
##    <dbl> <dbl> <chr>   <dbl>   <dbl>
##  1     1  2008 Fall       15      22
##  2     1  2008 Spring     16      22
##  3     1  2008 Winter     19      24
##  4     1  2009 Fall       12      10
##  5     1  2009 Spring     13      14
##  6     1  2009 Winter     27      20
##  7     2  2008 Fall       12      13
##  8     2  2008 Spring     13      11
##  9     2  2008 Winter     25      29
## 10     2  2009 Fall       16      23
## 11     2  2009 Spring     14      20
## 12     2  2009 Winter     21      26
## 13     3  2008 Fall       11      17
## 14     3  2008 Spring     12      12
## 15     3  2008 Winter     22      23
## 16     3  2009 Fall       13      14
## 17     3  2009 Spring     11       9
## 18     3  2009 Winter     27      31
```

{{< /spoiler >}}

{{< spoiler text="Click for the solution" >}}


```r
pivot_longer(
  data = grades,
  cols = c(Fall:Winter),
  names_to = "Quarter",
  values_to = "Score"
) %>%
  pivot_wider(
    names_from = Test,
    values_from = Score
  )
```

```
## # A tibble: 18 x 5
##       ID  Year Quarter  Math Writing
##    <dbl> <dbl> <chr>   <dbl>   <dbl>
##  1     1  2008 Fall       15      22
##  2     1  2008 Spring     16      22
##  3     1  2008 Winter     19      24
##  4     1  2009 Fall       12      10
##  5     1  2009 Spring     13      14
##  6     1  2009 Winter     27      20
##  7     2  2008 Fall       12      13
##  8     2  2008 Spring     13      11
##  9     2  2008 Winter     25      29
## 10     2  2009 Fall       16      23
## 11     2  2009 Spring     14      20
## 12     2  2009 Winter     21      26
## 13     3  2008 Fall       11      17
## 14     3  2008 Spring     12      12
## 15     3  2008 Winter     22      23
## 16     3  2009 Fall       13      14
## 17     3  2009 Spring     11       9
## 18     3  2009 Winter     27      31
```

In this example, the basic unit of observation is the test. Each individual takes two separate tests (`Math` or `Writing`) at multiple points in time: during each quarter (`Fall`, `Winter`, `Spring`) as well as in multiple years (`2008` and `2009`). So our final data frame should contain five columns: `ID` (identifying the student), `Year` (year the test was taken), `Quarter` (quarter in which the test was taken), `Math` (score on the math test), and `Writing` (score on the writing test).

Where can we begin? Initially we can make the data frame longer by making `Fall`, `Winter`, and `Spring` into a single column (we can use the inclusive select function `:` to gather these three columns):


```r
pivot_longer(
  data = grades,
  cols = c(Fall:Winter),
  names_to = "Quarter",
  values_to = "Score"
)
```

```
## # A tibble: 36 x 5
##       ID Test     Year Quarter Score
##    <dbl> <chr>   <dbl> <chr>   <dbl>
##  1     1 Math     2008 Fall       15
##  2     1 Math     2008 Spring     16
##  3     1 Math     2008 Winter     19
##  4     1 Math     2009 Fall       12
##  5     1 Math     2009 Spring     13
##  6     1 Math     2009 Winter     27
##  7     1 Writing  2008 Fall       22
##  8     1 Writing  2008 Spring     22
##  9     1 Writing  2008 Winter     24
## 10     1 Writing  2009 Fall       10
## # ... with 26 more rows
```

Good, but now we have observations spread across multiple rows. Remember that we want each test to be a separate variable. To do that, we can `pivot_wider()` those values across two columns.


```r
pivot_longer(
  data = grades,
  cols = c(Fall:Winter),
  names_to = "Quarter",
  values_to = "Score"
) %>%
  pivot_wider(
    names_from = Test,
    values_from = Score
  )
```

```
## # A tibble: 18 x 5
##       ID  Year Quarter  Math Writing
##    <dbl> <dbl> <chr>   <dbl>   <dbl>
##  1     1  2008 Fall       15      22
##  2     1  2008 Spring     16      22
##  3     1  2008 Winter     19      24
##  4     1  2009 Fall       12      10
##  5     1  2009 Spring     13      14
##  6     1  2009 Winter     27      20
##  7     2  2008 Fall       12      13
##  8     2  2008 Spring     13      11
##  9     2  2008 Winter     25      29
## 10     2  2009 Fall       16      23
## 11     2  2009 Spring     14      20
## 12     2  2009 Winter     21      26
## 13     3  2008 Fall       11      17
## 14     3  2008 Spring     12      12
## 15     3  2008 Winter     22      23
## 16     3  2009 Fall       13      14
## 17     3  2009 Spring     11       9
## 18     3  2009 Winter     27      31
```

{{< /spoiler >}}

## Activities


```r
activities
```

```
## # A tibble: 10 x 8
##    id    trt   work.T1 play.T1 talk.T1 work.T2 play.T2 talk.T2
##    <chr> <chr>   <dbl>   <dbl>   <dbl>   <dbl>   <dbl>   <dbl>
##  1 x1    cnt    0.652    0.865  0.536   0.275    0.354  0.0319
##  2 x2    cnt    0.568    0.615  0.0931  0.229    0.936  0.114 
##  3 x3    tr     0.114    0.775  0.170   0.0144   0.246  0.469 
##  4 x4    tr     0.596    0.356  0.900   0.729    0.473  0.397 
##  5 x5    tr     0.358    0.406  0.423   0.250    0.192  0.834 
##  6 x6    cnt    0.429    0.707  0.748   0.161    0.583  0.761 
##  7 x7    tr     0.0519   0.838  0.823   0.0170   0.459  0.573 
##  8 x8    tr     0.264    0.240  0.955   0.486    0.467  0.448 
##  9 x9    cnt    0.399    0.771  0.685   0.103    0.400  0.0838
## 10 x10   cnt    0.836    0.356  0.501   0.802    0.505  0.219
```

This one is also pretty difficult, but if you think it through conceptually it is doable. The unit of analysis is a single individual (identified by `id`) observed at two different times (`T1` and `T2`) performing different actions (`work`, `play`, `talk`, and `total` - note that `total` is not merely the sum of the first three values). Individuals in this experiment were assigned to either treatment or control (`trt`) and this information should be preserved in the final data frame.

{{< spoiler text="Click for a hint" >}}

**Tidy data structure**


```
## # A tibble: 20 x 6
##    id    trt   time    work  play   talk
##    <chr> <chr> <chr>  <dbl> <dbl>  <dbl>
##  1 x1    cnt   T1    0.652  0.865 0.536 
##  2 x1    cnt   T2    0.275  0.354 0.0319
##  3 x2    cnt   T1    0.568  0.615 0.0931
##  4 x2    cnt   T2    0.229  0.936 0.114 
##  5 x3    tr    T1    0.114  0.775 0.170 
##  6 x3    tr    T2    0.0144 0.246 0.469 
##  7 x4    tr    T1    0.596  0.356 0.900 
##  8 x4    tr    T2    0.729  0.473 0.397 
##  9 x5    tr    T1    0.358  0.406 0.423 
## 10 x5    tr    T2    0.250  0.192 0.834 
## 11 x6    cnt   T1    0.429  0.707 0.748 
## 12 x6    cnt   T2    0.161  0.583 0.761 
## 13 x7    tr    T1    0.0519 0.838 0.823 
## 14 x7    tr    T2    0.0170 0.459 0.573 
## 15 x8    tr    T1    0.264  0.240 0.955 
## 16 x8    tr    T2    0.486  0.467 0.448 
## 17 x9    cnt   T1    0.399  0.771 0.685 
## 18 x9    cnt   T2    0.103  0.400 0.0838
## 19 x10   cnt   T1    0.836  0.356 0.501 
## 20 x10   cnt   T2    0.802  0.505 0.219
```

{{< /spoiler >}}

{{< spoiler text="Click for the solution" >}}

This is a more complex operation. The basic problem is that we have variables stored in multiple columns (location, with possible values of `work`, `play`, and `talk`). We need to combine these columns into a single column for each variable. But what happens if we just make the data frame longer in this way?


```r
pivot_longer(
  data = activities,
  cols = c(work.T1:talk.T2),
  names_to = "variable",
  values_to = "value"
)
```

```
## # A tibble: 60 x 4
##    id    trt   variable  value
##    <chr> <chr> <chr>     <dbl>
##  1 x1    cnt   work.T1  0.652 
##  2 x1    cnt   play.T1  0.865 
##  3 x1    cnt   talk.T1  0.536 
##  4 x1    cnt   work.T2  0.275 
##  5 x1    cnt   play.T2  0.354 
##  6 x1    cnt   talk.T2  0.0319
##  7 x2    cnt   work.T1  0.568 
##  8 x2    cnt   play.T1  0.615 
##  9 x2    cnt   talk.T1  0.0931
## 10 x2    cnt   work.T2  0.229 
## # ... with 50 more rows
```

We've created a new problem! Actually, two problems:

1. We have a single observation stored across multiple rows: we want a single row for each `id` x `trt` pairing
2. We have two variables stored in a single column: `variable` contains the information on both location (`work`, `play`, and `talk`) as well as when the measurement was taken (`T1` or `T2`)

The best approach is to fix the second problem by separating the columns, then spreading the different types of measurements back into their own columns.


```r
pivot_longer(
  data = activities,
  cols = c(work.T1:talk.T2),
  names_to = "variable",
  values_to = "value"
) %>%
  separate(variable, into = c("location", "time"))
```

```
## # A tibble: 60 x 5
##    id    trt   location time   value
##    <chr> <chr> <chr>    <chr>  <dbl>
##  1 x1    cnt   work     T1    0.652 
##  2 x1    cnt   play     T1    0.865 
##  3 x1    cnt   talk     T1    0.536 
##  4 x1    cnt   work     T2    0.275 
##  5 x1    cnt   play     T2    0.354 
##  6 x1    cnt   talk     T2    0.0319
##  7 x2    cnt   work     T1    0.568 
##  8 x2    cnt   play     T1    0.615 
##  9 x2    cnt   talk     T1    0.0931
## 10 x2    cnt   work     T2    0.229 
## # ... with 50 more rows
```

```r
pivot_longer(
  data = activities,
  cols = c(work.T1:talk.T2),
  names_to = "variable",
  values_to = "value"
) %>%
  separate(variable, into = c("location", "time")) %>%
  pivot_wider(names_from = location, values_from = value)
```

```
## # A tibble: 20 x 6
##    id    trt   time    work  play   talk
##    <chr> <chr> <chr>  <dbl> <dbl>  <dbl>
##  1 x1    cnt   T1    0.652  0.865 0.536 
##  2 x1    cnt   T2    0.275  0.354 0.0319
##  3 x2    cnt   T1    0.568  0.615 0.0931
##  4 x2    cnt   T2    0.229  0.936 0.114 
##  5 x3    tr    T1    0.114  0.775 0.170 
##  6 x3    tr    T2    0.0144 0.246 0.469 
##  7 x4    tr    T1    0.596  0.356 0.900 
##  8 x4    tr    T2    0.729  0.473 0.397 
##  9 x5    tr    T1    0.358  0.406 0.423 
## 10 x5    tr    T2    0.250  0.192 0.834 
## 11 x6    cnt   T1    0.429  0.707 0.748 
## 12 x6    cnt   T2    0.161  0.583 0.761 
## 13 x7    tr    T1    0.0519 0.838 0.823 
## 14 x7    tr    T2    0.0170 0.459 0.573 
## 15 x8    tr    T1    0.264  0.240 0.955 
## 16 x8    tr    T2    0.486  0.467 0.448 
## 17 x9    cnt   T1    0.399  0.771 0.685 
## 18 x9    cnt   T2    0.103  0.400 0.0838
## 19 x10   cnt   T1    0.836  0.356 0.501 
## 20 x10   cnt   T2    0.802  0.505 0.219
```

{{< /spoiler >}}

## Session Info



```r
sessioninfo::session_info()
```

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
##  date     2022-10-13
##  pandoc   2.17.1.1 @ C:/Program Files/RStudio/bin/quarto/bin/ (via rmarkdown)
## 
## - Packages -------------------------------------------------------------------
##  package       * version date (UTC) lib source
##  assertthat      0.2.1   2019-03-21 [1] CRAN (R 4.1.3)
##  backports       1.4.1   2021-12-13 [1] CRAN (R 4.1.2)
##  blogdown        1.11    2022-08-09 [1] CRAN (R 4.1.3)
##  bookdown        0.28    2022-08-09 [1] CRAN (R 4.1.3)
##  broom           1.0.1   2022-08-29 [1] CRAN (R 4.1.3)
##  bslib           0.4.0   2022-07-16 [1] CRAN (R 4.1.3)
##  cachem          1.0.6   2021-08-19 [1] CRAN (R 4.1.3)
##  cellranger      1.1.0   2016-07-27 [1] CRAN (R 4.1.3)
##  cli             3.3.0   2022-04-25 [1] CRAN (R 4.1.3)
##  codetools       0.2-18  2020-11-04 [2] CRAN (R 4.1.3)
##  colorspace      2.0-3   2022-02-21 [1] CRAN (R 4.1.3)
##  crayon          1.5.1   2022-03-26 [1] CRAN (R 4.1.3)
##  DBI             1.1.3   2022-06-18 [1] CRAN (R 4.1.3)
##  dbplyr          2.2.1   2022-06-27 [1] CRAN (R 4.1.3)
##  digest          0.6.29  2021-12-01 [1] CRAN (R 4.1.3)
##  dplyr         * 1.0.9   2022-04-28 [1] CRAN (R 4.1.3)
##  ellipsis        0.3.2   2021-04-29 [1] CRAN (R 4.1.3)
##  evaluate        0.16    2022-08-09 [1] CRAN (R 4.1.3)
##  fansi           1.0.3   2022-03-24 [1] CRAN (R 4.1.3)
##  fastmap         1.1.0   2021-01-25 [1] CRAN (R 4.1.3)
##  forcats       * 0.5.2   2022-08-19 [1] CRAN (R 4.1.3)
##  fs              1.5.2   2021-12-08 [1] CRAN (R 4.1.3)
##  gargle          1.2.0   2021-07-02 [1] CRAN (R 4.1.3)
##  generics        0.1.3   2022-07-05 [1] CRAN (R 4.1.3)
##  ggplot2       * 3.3.6   2022-05-03 [1] CRAN (R 4.1.3)
##  glue            1.6.2   2022-02-24 [1] CRAN (R 4.1.3)
##  googledrive     2.0.0   2021-07-08 [1] CRAN (R 4.1.3)
##  googlesheets4   1.0.1   2022-08-13 [1] CRAN (R 4.1.3)
##  gtable          0.3.1   2022-09-01 [1] CRAN (R 4.1.3)
##  haven           2.5.1   2022-08-22 [1] CRAN (R 4.1.3)
##  here            1.0.1   2020-12-13 [1] CRAN (R 4.1.3)
##  hms             1.1.2   2022-08-19 [1] CRAN (R 4.1.3)
##  htmltools       0.5.2   2021-08-25 [1] CRAN (R 4.1.3)
##  httr            1.4.4   2022-08-17 [1] CRAN (R 4.1.3)
##  jquerylib       0.1.4   2021-04-26 [1] CRAN (R 4.1.3)
##  jsonlite        1.8.0   2022-02-22 [1] CRAN (R 4.1.3)
##  knitr           1.40    2022-08-24 [1] CRAN (R 4.1.3)
##  lifecycle       1.0.2   2022-09-09 [1] CRAN (R 4.1.3)
##  lubridate       1.8.0   2021-10-07 [1] CRAN (R 4.1.3)
##  magrittr        2.0.3   2022-03-30 [1] CRAN (R 4.1.3)
##  modelr          0.1.9   2022-08-19 [1] CRAN (R 4.1.3)
##  munsell         0.5.0   2018-06-12 [1] CRAN (R 4.1.3)
##  pillar          1.8.1   2022-08-19 [1] CRAN (R 4.1.3)
##  pkgconfig       2.0.3   2019-09-22 [1] CRAN (R 4.1.3)
##  purrr         * 0.3.4   2020-04-17 [1] CRAN (R 4.1.3)
##  R6              2.5.1   2021-08-19 [1] CRAN (R 4.1.3)
##  rcis          * 0.2.5   2022-10-07 [1] Github (css-materials/rcis@c0a0358)
##  readr         * 2.1.2   2022-01-30 [1] CRAN (R 4.1.3)
##  readxl          1.4.1   2022-08-17 [1] CRAN (R 4.1.3)
##  reprex          2.0.2   2022-08-17 [1] CRAN (R 4.1.3)
##  rlang           1.0.6   2022-09-24 [1] CRAN (R 4.1.3)
##  rmarkdown       2.16    2022-08-24 [1] CRAN (R 4.1.3)
##  rprojroot       2.0.3   2022-04-02 [1] CRAN (R 4.1.3)
##  rstudioapi      0.14    2022-08-22 [1] CRAN (R 4.1.3)
##  rvest           1.0.3   2022-08-19 [1] CRAN (R 4.1.3)
##  sass            0.4.2   2022-07-16 [1] CRAN (R 4.1.3)
##  scales          1.2.1   2022-08-20 [1] CRAN (R 4.1.3)
##  sessioninfo     1.2.2   2021-12-06 [1] CRAN (R 4.1.3)
##  stringi         1.7.6   2021-11-29 [1] CRAN (R 4.1.2)
##  stringr       * 1.4.1   2022-08-20 [1] CRAN (R 4.1.3)
##  tibble        * 3.1.8   2022-07-22 [1] CRAN (R 4.1.3)
##  tidyr         * 1.2.0   2022-02-01 [1] CRAN (R 4.1.3)
##  tidyselect      1.1.2   2022-02-21 [1] CRAN (R 4.1.3)
##  tidyverse     * 1.3.2   2022-07-18 [1] CRAN (R 4.1.3)
##  tzdb            0.3.0   2022-03-28 [1] CRAN (R 4.1.3)
##  utf8            1.2.2   2021-07-24 [1] CRAN (R 4.1.3)
##  vctrs           0.4.1   2022-04-13 [1] CRAN (R 4.1.3)
##  withr           2.5.0   2022-03-03 [1] CRAN (R 4.1.3)
##  xfun            0.30    2022-03-02 [1] CRAN (R 4.1.3)
##  xml2            1.3.3   2021-11-30 [1] CRAN (R 4.1.3)
##  yaml            2.3.5   2022-02-21 [1] CRAN (R 4.1.2)
## 
##  [1] C:/Users/Sabrina Nardin/Documents/R/win-library/4.1
##  [2] C:/Program Files/R/R-4.1.3/library
## 
## ------------------------------------------------------------------------------
```

## Acknowledgments


* This page has been developed starting from Benjamin Soltoff’s “Computing for the Social Sciences” course materials, licensed under the CC BY-NC 4.0 Creative Commons License.
