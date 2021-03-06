---
title       : Scatterplot Matrix Generator
subtitle    : A Shiny Application
author      : Leonard Greski
job         : Developing Data Products Course Project, December 2015 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : standalone # {standalone, selfcontained, draft}
logo        : AgereBlack.png
knit        : slidify::knit2slides
output: 
  html_document: 
    fig_height: 2
    fig_width: 2
    
--- 
<style>.title-slide{background-color: white; </style>

## Overview

- mtcars is an important data set in the Data Science Curriculum
- Used to illustrate a variety of concepts across multiple classes
- It's a good candidate for a starter shiny application
<br><br>
<b>Application:</b> mtcars [Scatterplot Matrix Generator](https://lgreski.shinyapps.io/mtcars_Scatterplot_Matrix_Generator)

--- .class #id

## The Concept


```r
library(datasets)
data(mtcars)
pairs(~ mpg + wt + hp + disp,data=mtcars,
      main="Pairwise plots of mtcars data")
```

![plot of chunk unnamed-chunk-1](assets/fig/unnamed-chunk-1-1.png) 


--- 

## A Simple User Interface

![](./assets/fig/ui.png)

--- 

## Design Considerations

- Handling situation with 0 or 1 checkbox selected
- Parsing the selections and generating a list containing the selected columns
- Converting the selections into the proper format for the `pairs()` function
- Rendering the instructions, and turning them off when two or more variables are selected
- Rendering the scatterplot matrix
- Adding summary statistics for each variable in the scatterplot matrix, so it's clear that "calculations" are made on the server

--- 

## Additional Features to Be Considered in the Future

1. Starting with a list of data sets rather than a pre-selected one
2. Allowing for a user selected graph type (e.g. group of box plots, etc.)
3. Combining a chart with a statistical analysis (e.g. regression analysis)
4. Allowing the user to print the resulting chart 

## 








