---
title: "Plotly 8/17/2020"
author: "Brian Stewart"
date: "8/17/2020"
output: html_document
---


```r
library(plotly)
library(wesanderson)
```


```r
data('mtcars')
```


```r
fig <- plot_ly(mtcars, x = ~hp, y = ~mpg, mode = 'markers', color = as.factor(mtcars$cyl), type = 'scatter')
fig <- fig %>% layout(
        title = "Horsepower's affect on Miles Per Gallon by Cylinder Type",
        xaxis = list(title = 'Horsepower'),
        yaxis = list(title = 'Miles Per Gallon'),
        legend = list(title = list(text='<b> Cylinder </b>'))
)

fig
```

```
## PhantomJS not found. You can install it with webshot::install_phantomjs(). If it is installed, please make sure the phantomjs executable can be found via the PATH variable.
```

```
## Warning in normalizePath(path.expand(path), winslash, mustWork): path[1]="webshot285c27e45ae0.png": The system cannot find
## the file specified
```

```
## Warning in file(con, "rb"): cannot open file 'C:
## \Users\JASON_~1\AppData\Local\Temp\RtmpYDb88E\file285c33fa2031\webshot285c27e45ae0.png': No such file or directory
```

```
## Error in file(con, "rb"): cannot open the connection
```
