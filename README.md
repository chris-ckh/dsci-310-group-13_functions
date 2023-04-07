
<!-- README.md is generated from README.Rmd. Please edit this file -->

# youtubeFunction

<!-- badges: start -->

![](https://github.com/chris-ckh/dsci-310-group-13-pkg/actions/workflows/test-coverage.yaml/badge.svg)
<!-- badges: end -->

The goal of youtubeFunction is to build functions that are used for
DSCI-310 group 13 term project. This package includes functions that
read raw data, read unclenaed data, clean the data, bind tables, and fit
the model.

## Installation

You can install the development version of youtubeFunction from
[GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("chris-ckh/dsci-310-group-13-pkg")
```

## Usage

The function read_raw_data() takes in an URL to one of raw data sets in
the data folder from our Github page :

``` r
library(youtubeFunction)
#> Loading required package: tidyverse
#> ── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
#> ✔ dplyr     1.1.1     ✔ readr     2.1.4
#> ✔ forcats   1.0.0     ✔ stringr   1.5.0
#> ✔ ggplot2   3.4.1     ✔ tibble    3.2.1
#> ✔ lubridate 1.9.2     ✔ tidyr     1.3.0
#> ✔ purrr     1.0.1     
#> ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
#> ✖ dplyr::filter() masks stats::filter()
#> ✖ dplyr::lag()    masks stats::lag()
#> ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors
## table0007 <- read_raw_data("https://raw.githubusercontent.com/chris-ckh/dsci-310-group-13/main/data/0007.txt")
```

The function bind_tables() takes in four tables that contains Youtube
data for one year, and binds them into one table:

``` r
library(youtubeFunction)
## This examples binds tables that contains YouTube data for 2007 into one table 
## data2007_uncleaned <- bind_tables(table0007,table0107,table0207, table0307)
```

The function read_uncleaned_data() takes in an path to read a saved out
uncleaned data set from load.R, for example:

``` r
## "/home/rstudio/data/" is the path to where the uncleaned data is saved
## data2007_uncleaned <- read_uncleaned_data("/home/rstudio/data/data2007_not_cleaned.txt")
```

The function wrangling_data() takes in an uncleaned youtube data set and
tidies it so that the data set only contains “age”, ‘category’,
‘length’,‘views’,‘rate’,‘ratings’,‘comments’ as columns. For instance:

``` r
## "/home/rstudio/data/" is the path to where the uncleaned data is saved
## data2007 <- wrangling_data(data2007_uncleaned)
```

The function fit_regression() takes in the training data and fits a
simple linear regression to said data with the response variable
`views`.

``` r
## lm <- fit_regression(training)
```
