Gapminder project
================
Abdullah Farouk
2017-09-15

What does Gapminder do?
-----------------------

Gapminder is a **fact tank** that aims to educate the world about global development. It hopes to do so with the use of statistical information deemed reliable. They collaborate with the UN, universities and various public agents to undertake their research. For more details on them see <http://www.gapminder.org/about-gapminder/>.

I initialize my exploration of the dataset with the following code:

``` r
library(tidyverse)
```

    ## Loading tidyverse: ggplot2
    ## Loading tidyverse: tibble
    ## Loading tidyverse: tidyr
    ## Loading tidyverse: readr
    ## Loading tidyverse: purrr
    ## Loading tidyverse: dplyr

    ## Conflicts with tidy packages ----------------------------------------------

    ## filter(): dplyr, stats
    ## lag():    dplyr, stats

``` r
library(gapminder)
```

To study the structure of the dataset and learn more about it's variables and their values, I do the following:

``` r
str(gapminder)
```

    ## Classes 'tbl_df', 'tbl' and 'data.frame':    1704 obs. of  6 variables:
    ##  $ country  : Factor w/ 142 levels "Afghanistan",..: 1 1 1 1 1 1 1 1 1 1 ...
    ##  $ continent: Factor w/ 5 levels "Africa","Americas",..: 3 3 3 3 3 3 3 3 3 3 ...
    ##  $ year     : int  1952 1957 1962 1967 1972 1977 1982 1987 1992 1997 ...
    ##  $ lifeExp  : num  28.8 30.3 32 34 36.1 ...
    ##  $ pop      : int  8425333 9240934 10267083 11537966 13079460 14880372 12881816 13867957 16317921 22227415 ...
    ##  $ gdpPercap: num  779 821 853 836 740 ...

``` r
head(gapminder)
```

    ## # A tibble: 6 × 6
    ##       country continent  year lifeExp      pop gdpPercap
    ##        <fctr>    <fctr> <int>   <dbl>    <int>     <dbl>
    ## 1 Afghanistan      Asia  1952  28.801  8425333  779.4453
    ## 2 Afghanistan      Asia  1957  30.332  9240934  820.8530
    ## 3 Afghanistan      Asia  1962  31.997 10267083  853.1007
    ## 4 Afghanistan      Asia  1967  34.020 11537966  836.1971
    ## 5 Afghanistan      Asia  1972  36.088 13079460  739.9811
    ## 6 Afghanistan      Asia  1977  38.438 14880372  786.1134

``` r
tail(gapminder)
```

    ## # A tibble: 6 × 6
    ##    country continent  year lifeExp      pop gdpPercap
    ##     <fctr>    <fctr> <int>   <dbl>    <int>     <dbl>
    ## 1 Zimbabwe    Africa  1982  60.363  7636524  788.8550
    ## 2 Zimbabwe    Africa  1987  62.351  9216418  706.1573
    ## 3 Zimbabwe    Africa  1992  60.377 10704340  693.4208
    ## 4 Zimbabwe    Africa  1997  46.809 11404948  792.4500
    ## 5 Zimbabwe    Africa  2002  39.989 11926563  672.0386
    ## 6 Zimbabwe    Africa  2007  43.487 12311143  469.7093

``` r
length(gapminder$country)
```

    ## [1] 1704

The gapminder dataset has information on three interesting variables, for 1704 countries from around the world. They are: 1. Life Expectancy 2. Population 3. GDP per capita

They provide some fascinating interactions for us to study.

### Brief Analysis of Life Expectancy Trends

To begin lets visualize the variation, accross time, in life expectancy using a bar chart.

``` r
hist(gapminder$lifeExp, main = 'Histogram of Life Expectancy')
```

![](hw01-Exploring_Gapminder_Dataset_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-3-1.png)

We see that there are a lot of countries with high life expectancies. Has this always been the case?

``` r
plot(gapminder$year, gapminder$lifeExp)
```

![](hw01-Exploring_Gapminder_Dataset_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-4-1.png)

We notice that the average life span has been going up over time. Might this be because people around the world are simply richer today than they were before?

``` r
plot(gapminder$year, gapminder$gdpPercap)
```

![](hw01-Exploring_Gapminder_Dataset_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-5-1.png)

This does seem to be the case. Hence this could be one possible explanation of the trends we see in this variable. I hope to explore more such trends in the next class.
