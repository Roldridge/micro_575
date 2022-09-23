hmk_04
================
Ryan Oldridge

## Hmk_04

loading tidyverse because i have to and forgot about it and wondered why
my stuff wouldn’t work

``` r
library(tidyverse)
```

``` r
data <- read_csv("fake_data.csv")
```

making the graph because thats the homework

``` r
ggplot(data) + 
  geom_violin(aes(x=make, y=mileage, fill=make))
```

![](hmk_04_files/figure-gfm/unnamed-chunk-3-1.png)

this is good because it shows what proportion of each make is at a
particular mileage. Also, its colorful because that looks nice.
