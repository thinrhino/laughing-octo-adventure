---
title       : Study of Respirable Suspended Particulate Matter(RSPM)
subtitle    : 
author      : Aditya Laghate
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides

--- .class #id 

## What is RSPM

Respirable Suspended Particulate Matter or RSPM are those suspended particles in the air that is 10 micrometers or less.

Since these particulate matter are small enough to be breathed in, they can cause detrimental effects to man. It is said that particulate matter that is 2.5 micrometers or less is harmful as these cannot be expelled from the body and cause long term effects such as lung cancer, allergies, asthma,and other respiratory diseases, some type of birth defects as well as premature death.

--- .class #id 

## Data Source

The data for this app was downloaded from the Indian Govt. open data portal  
http://data.gov.in/catalog/air-quality-respect-respirable-suspended-particulate-matterrspm-air-quality-stations-under#web_catalog_tabs_block_10


--- .class #id 

## Thought behind the app

The idea of the app, was to showcase how the levels of RSPM have changed between 2006 & 2008.

--- .class #id 

## Code example

In the app, I have used the ```aggregate``` function.


```r
attach(mtcars)
```

```
## The following object is masked from package:ggplot2:
## 
##     mpg
```

```r
aggdata <-aggregate(mtcars, by=list(cyl,vs),
  FUN=mean, na.rm=TRUE)
print(aggdata)
```

```
##   Group.1 Group.2   mpg cyl  disp    hp  drat    wt  qsec vs     am  gear
## 1       4       0 26.00   4 120.3  91.0 4.430 2.140 16.70  0 1.0000 5.000
## 2       6       0 20.57   6 155.0 131.7 3.807 2.755 16.33  0 1.0000 4.333
## 3       8       0 15.10   8 353.1 209.2 3.229 3.999 16.77  0 0.1429 3.286
## 4       4       1 26.73   4 103.6  81.8 4.035 2.300 19.38  1 0.7000 4.000
## 5       6       1 19.12   6 204.6 115.2 3.420 3.389 19.21  1 0.0000 3.500
##    carb
## 1 2.000
## 2 4.667
## 3 3.500
## 4 1.500
## 5 2.500
```

```r
detach(mtcars)
```
