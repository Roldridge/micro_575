Homework 3 template
================
Ryan Oldridge

# Data input/output

loading tidyverse and reading the data file and making it an object

``` r
library(tidyverse)

fake_data <- read_csv(file = "fake_date.csv")
```

``` r
read_csv("fake_date.csv")
```

    Rows: 10 Columns: 2
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    dbl (2): days, something

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

    # A tibble: 10 × 2
        days something
       <dbl>     <dbl>
     1     1         3
     2     2         6
     3     3         5
     4     4         6
     5     5         2
     6     6         6
     7     7         7
     8     8         8
     9     9         5
    10    10         7

``` r
print("fake_data")
```

    [1] "fake_data"

# Investigating the properties of data frames

Use two different functions that both give some kind of summary or
overview of the data frame. Which one do you think is more useful?

``` r
str(fake_data)
```

    spec_tbl_df [10 × 2] (S3: spec_tbl_df/tbl_df/tbl/data.frame)
     $ days     : num [1:10] 1 2 3 4 5 6 7 8 9 10
     $ something: num [1:10] 3 6 5 6 2 6 7 8 5 7
     - attr(*, "spec")=
      .. cols(
      ..   days = col_double(),
      ..   something = col_double()
      .. )
     - attr(*, "problems")=<externalptr> 

``` r
glimpse(fake_data)
```

    Rows: 10
    Columns: 2
    $ days      <dbl> 1, 2, 3, 4, 5, 6, 7, 8, 9, 10
    $ something <dbl> 3, 6, 5, 6, 2, 6, 7, 8, 5, 7

glimpse is more useful here because it shows the data clearly laid out
in an organized way.

# Manipulating data frames

Create a new column of your data frame by performing some kind of
arithmetic operation on an existing column.

``` r
fake_data$newsomething <- fake_data$something + 2 

glimpse(fake_data)
```

    Rows: 10
    Columns: 3
    $ days         <dbl> 1, 2, 3, 4, 5, 6, 7, 8, 9, 10
    $ something    <dbl> 3, 6, 5, 6, 2, 6, 7, 8, 5, 7
    $ newsomething <dbl> 5, 8, 7, 8, 4, 8, 9, 10, 7, 9

created a new column by adding 2 to the column “something”

# Working on columns

Calculate the mean of a numeric column in your data frame.

``` r
mean(fake_data$newsomething)
```

    [1] 7.5

found that the mean of the new column i made is 7.5

# Accessing elements of data frames

``` r
cats <- data.frame(coat = c("calico", "black", "tabby", "calico"),
                   weight = c(2.1, 5.0, 3.2, 4.4),
                   likes.string = c(TRUE, FALSE, TRUE, TRUE))
```

``` r
cats[1]
```

        coat
    1 calico
    2  black
    3  tabby
    4 calico

shows the first list which is the coat of the cats

``` r
cats[[1]]
```

    [1] "calico" "black"  "tabby"  "calico"

listed the first column as a vector

``` r
cats$coat
```

    [1] "calico" "black"  "tabby"  "calico"

listed the values within the first column which happen to be the coats.

``` r
cats[1, 1]
```

    [1] "calico"

this called the first value of the first column

``` r
cats[ , 1]
```

    [1] "calico" "black"  "tabby"  "calico"

this gave me every value of the first column

``` r
cats[1, ]
```

        coat weight likes.string
    1 calico    2.1         TRUE

gives me all of the first row of each column
