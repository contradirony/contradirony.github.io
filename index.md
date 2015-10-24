---
title       : Simple Fuel Explorer App
subtitle    : Do I spend more money when fuel is cheaper?
author      : slam
job         : data scientist
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []           # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides

---

## What is the App?

. It is a very simple app to view relationships between some simple attributes of fuel data I've gathered in my spare time.

. The dataset is stored as a data frame as follows:




```r
head(dataset)
```

```
##   PricePerLitre MoneySpent LitresOfPetrol
## 1         1.629      30.00       18.41621
## 2         1.599      30.00       18.76173
## 3         1.619      20.13       12.43360
## 4         1.589      40.00       25.17306
## 5         1.629      40.07       24.59791
## 6         1.579      30.05       19.03103
```

--- .class #id 

## 



Example output:

```r
 ggplot(dataset, aes_string('MoneySpent', 'PricePerLitre')) +  geom_point(size=3) 
```

![plot of chunk unnamed-chunk-4](assets/fig/unnamed-chunk-4-1.png) 

--- .class #id 

## How to use it

1. There are 3 attributes in the dataset: MoneySpent, LitresOfPetrol and PricePerLitre
2. Select one of the three for the *x*-axis and a different one for the *y*-axis.
3. See the graph update reactively in real-time after selection!


**Example interpretation**

In the previous graph you can see there are slightly more dots in the bottom right side which means that the cheaper the price per litre, the more instances of money spent, especially when you compare the 15-20 range to the 45-50 range.

However, it is more evenly distributed between 30 and 40 as I drove regularly enough to have to buy petrol regardless of the price.

--- .class #id 

## In conclusion...

. Please try it out!


. It can be found at: https://contradirony.shinyapps.io/fuelApp

