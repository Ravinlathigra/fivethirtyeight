
<!-- README.md is generated from README.Rmd. Please edit that file -->
fivethirtyeight
===============

[![Build Status](https://travis-ci.org/rudeboybert/fivethirtyeight.svg?branch=master)](https://travis-ci.org/rudeboybert/fivethirtyeight) [![CRAN\_Status\_Badge](http://www.r-pkg.org/badges/version/fivethirtyeight)](http://cran.r-project.org/package=fivethirtyeight) [![CRAN RStudio mirror downloads](http://cranlogs.r-pkg.org/badges/fivethirtyeight)](http://www.r-pkg.org/pkg/fivethirtyeight)

An R package that provides access to the code and data sets published by FiveThirtyEight <https://github.com/fivethirtyeight/data>. Note that while we received guidance from editors at 538, this package is not officially published by 538.

Installation
------------

Get the released version from CRAN:

``` r
install.packages("fivethirtyeight")
```

Or the development version from GitHub:

``` r
# If you haven't installed devtools yet, do so:
# install.packages("devtools")
devtools::install_github("rudeboybert/fivethirtyeight")
```

Usage
-----

### Example Usage

``` r
library(fivethirtyeight)

# Bechdel data set (note that data is lazy loaded so one can also just access `bechdel` without running `data(bechdel)`):
data(bechdel)
head(bechdel)
?bechdel
# If using RStudio:
View(bechdel)

# To see a list of all data sets:
data(package = "fivethirtyeight")

# To see a more detailed list of all data sets, see the package vignette:
vignette("fivethirtyeight", package = "fivethirtyeight")
```

### Data Analysis Examples in Vignettes

For some data sets, there is an example analysis in a package vignette. For example, we did this using the [R code](https://github.com/fivethirtyeight/data/blob/master/bechdel/analyze-bechdel.R) for the article [The Dollar-And-Cents Case Against Hollywood’s Exclusion of Women](http://fivethirtyeight.com/features/the-dollar-and-cents-case-against-hollywoods-exclusion-of-women) here:

``` r
vignette("bechdel", package = "fivethirtyeight")
```

For a complete list of vignettes run:

``` r
browseVignettes(package = "fivethirtyeight")
```

More Information
----------------

See the package vignette for:

1.  Our motivation for creating this package.
2.  Guidelines we followed preparing the data sets and links to the code.
3.  A more detailed list of all data sets.

``` r
vignette("fivethirtyeight", package = "fivethirtyeight")
```

Collaborate
-----------

### Code

In many instances, the data sets on the original 538 GitHub repository had the R code used in the analysis. We would love to have these in the form of package vignettes that:

1.  Convert the code to use [`tidyverse`](https://blog.rstudio.org/2016/09/15/tidyverse-1-0-0/) package tools
2.  Present the code in [R Markdown](http://rmarkdown.rstudio.com/) format

### Contributing to the Package

If you want to contribute to the package:

-   We followed the principles in Hadley Wickham's [R packages](http://r-pkgs.had.co.nz/) book
-   Preliminary instructions for automating R package documentation and collecting data about the data sets is available [here](https://github.com/rudeboybert/fivethirtyeight/blob/master/data_import_procedure.md).
