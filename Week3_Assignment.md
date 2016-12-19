Week3_Assignment
========================================================
author: Jayant Ragde
date: 2016-12-17
autosize: true

Presentation Summary
========================================================

This presentation demonstrates the creation of a web
presentation with an interactive plot using Plotly.

Unemployment data (FRED/UNRATE) and Daily Federal Funds
Rate data (FRED/MDFF) are downloaded using the Quandl package.
This data is merged to include date for the same dates only.
Data prior to 1980-01-01 is discarded.

These two data points are plotted using Plotly.


Read Data & Plot
========================================================


```r
library(plotly)
df2 <- read.csv(".\\Data1.csv")
p <- plot_ly(df2, x = ~Date, name = "Date") %>%
  add_trace(y = ~UnmpRate, name = "Unemployment Rate", type = 'scatter', mode = 'lines+markers') %>%
  add_trace(y = ~FedFundRate, name = "Fed Funds Rate", type = 'scatter', mode = 'lines+markers')
```

Plot
========================================================
[Plotly Graph](https://plot.ly/~jragde/4/)

