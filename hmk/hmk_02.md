hmk_02
================

## tidyverse packages stuff 1

Quarto enables you to weave together content and executable code into a
finished document. To learn more about Quarto see <https://quarto.org>.

## along with creating objects

When you click the **Render** button a document will be generated that
includes both content and the output of embedded code. You can embed
code like this:

``` r
library(tidyverse)

a <- 1
b <- 2

ls()
```

    [1] "a" "b"

``` r
rm(list = ls())
```

You can add options to executable code like this

    [1] 4

The `echo: false` option disables the printing of code (only output is
displayed).
