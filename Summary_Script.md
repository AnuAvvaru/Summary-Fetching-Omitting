R Markdown
----------

This is an R Markdown document. Markdown is a simple formatting syntax
for authoring HTML, PDF, and MS Word documents. For more details on
using R Markdown see <http://rmarkdown.rstudio.com>.

When you click the **Knit** button a document will be generated that
includes both content as well as the output of any embedded R code
chunks within the document. You can embed an R code chunk like this:

    summary(cars)

    ##      speed           dist       
    ##  Min.   : 4.0   Min.   :  2.00  
    ##  1st Qu.:12.0   1st Qu.: 26.00  
    ##  Median :15.0   Median : 36.00  
    ##  Mean   :15.4   Mean   : 42.98  
    ##  3rd Qu.:19.0   3rd Qu.: 56.00  
    ##  Max.   :25.0   Max.   :120.00

Including Plots
---------------

You can also embed plots, for example:

![](Summary_Script_files/figure-markdown_strict/pressure-1.png)

Note that the `echo = FALSE` parameter was added to the code chunk to
prevent printing of the R code that generated the plot.

Assigning Values
================

    choco_price <- c(20,50,80,100,120,40,30)
    choco_price

    ## [1]  20  50  80 100 120  40  30

Basic Summary Statistics
========================

    summary(choco_price)

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   20.00   35.00   50.00   62.86   90.00  120.00

Assigning Values
================

    products <- c(1:50)
    products

    ##  [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21 22 23
    ## [24] 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46
    ## [47] 47 48 49 50

Assigning missing Values
========================

    products[c(2,5,10,13,24,30,40,14)] <- NA
    products

    ##  [1]  1 NA  3  4 NA  6  7  8  9 NA 11 12 NA NA 15 16 17 18 19 20 21 22 23
    ## [24] NA 25 26 27 28 29 NA 31 32 33 34 35 36 37 38 39 NA 41 42 43 44 45 46
    ## [47] 47 48 49 50

Find missing values
===================

    is.na(products)

    ##  [1] FALSE  TRUE FALSE FALSE  TRUE FALSE FALSE FALSE FALSE  TRUE FALSE
    ## [12] FALSE  TRUE  TRUE FALSE FALSE FALSE FALSE FALSE FALSE FALSE FALSE
    ## [23] FALSE  TRUE FALSE FALSE FALSE FALSE FALSE  TRUE FALSE FALSE FALSE
    ## [34] FALSE FALSE FALSE FALSE FALSE FALSE  TRUE FALSE FALSE FALSE FALSE
    ## [45] FALSE FALSE FALSE FALSE FALSE FALSE

Place Missing values False
==========================

    !is.na(products)

    ##  [1]  TRUE FALSE  TRUE  TRUE FALSE  TRUE  TRUE  TRUE  TRUE FALSE  TRUE
    ## [12]  TRUE FALSE FALSE  TRUE  TRUE  TRUE  TRUE  TRUE  TRUE  TRUE  TRUE
    ## [23]  TRUE FALSE  TRUE  TRUE  TRUE  TRUE  TRUE FALSE  TRUE  TRUE  TRUE
    ## [34]  TRUE  TRUE  TRUE  TRUE  TRUE  TRUE FALSE  TRUE  TRUE  TRUE  TRUE
    ## [45]  TRUE  TRUE  TRUE  TRUE  TRUE  TRUE

Displays missing values
=======================

    products[is.na(products)]

    ## [1] NA NA NA NA NA NA NA NA

Inserting missing values in one object
======================================

    count <- products[is.na(products)]
    count

    ## [1] NA NA NA NA NA NA NA NA

Missing values count
====================

    length(count)

    ## [1] 8

Assigning Values
================

    product1 <- c(1:20)
    product1

    ##  [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20

Inserting missing values in particular Index
============================================

    product1[c(2,5,10,4,6,16,18,13)] <- NA
    product1

    ##  [1]  1 NA  3 NA NA NA  7  8  9 NA 11 12 NA 14 15 NA 17 NA 19 20

    length(product1)

    ## [1] 20

Objects available
=================

    ls()

    ## [1] "choco_price" "count"       "product1"    "products"
