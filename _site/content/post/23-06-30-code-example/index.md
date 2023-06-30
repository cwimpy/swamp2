---
title: "Code Example Post"
author: "Cameron Wimpy"
format: hugo
editor: visual
---

## Quarto

Quarto enables you to weave together content and executable code into a finished document. To learn more about Quarto see <https://quarto.org>.

## Running Code

When you click the **Render** button a document will be generated that includes both content and the output of embedded code. You can embed code like this:

``` r
1 + 1
```

    [1] 2

You can add options to executable code like this

    [1] 4

The `echo: false` option disables the printing of code (only output is displayed).

``` r
library(ggplot2)
library(hrbrthemes)
```

    NOTE: Either Arial Narrow or Roboto Condensed fonts are required to use these themes.

          Please use hrbrthemes::import_roboto_condensed() to install Roboto Condensed and

          if Arial Narrow is not on your system, please see https://bit.ly/arialnarrow

``` r
mtcars |> 
  ggplot(aes(wt, mpg)) + 
  geom_smooth(method = lm) +
  geom_point() +
  labs(title = "Relationship Between Car Weight and Miles Per Gallon",
       y = "Miles Per Gallon", x = "Car Weight") +
  theme_ipsum()
```

    `geom_smooth()` using formula = 'y ~ x'

<img src="index.markdown_strict_files/figure-markdown_strict/unnamed-chunk-3-1.png" width="768" />
