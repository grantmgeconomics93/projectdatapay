giyyuitt
================
2022-07-10

``` r
library(dbplyr)
library(tidyverse)
library(stringi)
```

``` r
library(readxl)
```

    ## Warning: package 'readxl' was built under R version 4.1.3

``` r
data_cleaned_2021 <- read_excel("data_cleaned_2021.xlsx")
View(data_cleaned_2021)
```

    ## Warning in gsub("K", "", (newmin)) %>% as.numeric(): NAs introduced by coercion

``` r
 newmax=substr(data_cleaned_2021$`Salary Estimate`,7,9)
newdata$newmax=gsub("K","",(newmax))%>%as.numeric()
```

    ## Warning in gsub("K", "", (newmax)) %>% as.numeric(): NAs introduced by coercion

``` r
#new=separate(#,col= `Salary Estimate`,into= c("emp","glassdoor","o","my") ,sep ="([$()])")z
```

``` r
df=data_cleaned_2021%>%select(`Salary Estimate`)%>%sample_n(100)
```

``` r
dff=data_cleaned_2021%>%select(`Salary Estimate`)%>%sample_n(100)
```

Note that the `echo = FALSE` parameter was added to the code chunk to
prevent printing of the R code that generated the plot.
