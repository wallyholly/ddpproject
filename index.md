---
title       : DDP - Course Project
subtitle    : Filtering mt-cars data on the fly
author      : wally_holly
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---.class1

## Goal of the app

My little shiny app allows it to filter the mtcars dataset on the fly.

1. The user enters the number of cylinders of a car.
2. The user specify the lower and upper limit of the mpg value (Miles/(US) gallon)
3. The app selects all cars from the data set that fulfill the criteria, selected by the user. 

---.class #id

## The data set
- Data Set: mtcars
- extracted from the 1974 Motor Trend US magazine
- 32 cars; 11 variables:

```r
names(mtcars)
```

```
##  [1] "mpg"  "cyl"  "disp" "hp"   "drat" "wt"   "qsec" "vs"   "am"   "gear"
## [11] "carb"
```

---

## A quick look on the data

```r
head(mtcars)
```

```
##                    mpg cyl disp  hp drat    wt  qsec vs am gear carb
## Mazda RX4         21.0   6  160 110 3.90 2.620 16.46  0  1    4    4
## Mazda RX4 Wag     21.0   6  160 110 3.90 2.875 17.02  0  1    4    4
## Datsun 710        22.8   4  108  93 3.85 2.320 18.61  1  1    4    1
## Hornet 4 Drive    21.4   6  258 110 3.08 3.215 19.44  1  0    3    1
## Hornet Sportabout 18.7   8  360 175 3.15 3.440 17.02  0  0    3    2
## Valiant           18.1   6  225 105 2.76 3.460 20.22  1  0    3    1
```

---

## Table of the cars by number of cylinders

```
##   No. of cylinders frequency
## 1                4        11
## 2                6         7
## 3                8        14
```
We can see that there are 11 cars with 4 cylinders, 7 cars with 6 cylinders and 14 models with 8 cylinders

---

## Histogram of the cars by mileage
![plot of chunk unnamed-chunk-4](assets/fig/unnamed-chunk-4-1.png)

---
