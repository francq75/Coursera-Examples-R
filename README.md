# Coursera-Examples-R

---
title: "Ggplot Markdown exercise"
author: "Francho"
date: "2024-01-09"
output: html_document
---

# **Francho Excercise**
## *GGplot Example coursera*
### Markdown written

Notes: setting up my R environment by loading "tidyverse" and "ggplot" packages:

```{r}
library (tidyverse)
library (ggplot2)
```


```{r}
# library
library(ggplot2)

# basic graph
p <- ggplot(mtcars, aes(x = wt, y = mpg)) + 
  geom_point()

# a data frame with all the annotation info
annotation <- data.frame(
  x = c(2,4.5),
  y = c(20,25),
  label = c("label 1", "label 2")
)

p + geom_text(data=annotation, aes( x=x, y=y, label=label),                 , 
              color="orange", 
              size=7 , angle=45, fontface="bold" )

png(file = "exampleplot.png", bg = "transparent")
plot(1:10)
rect(1, 5, 3, 7, col = "white")
dev.off()

```


