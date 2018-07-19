+++
title = "Theme"
description = ""
weight = 8
+++


## Theme

Theme Options can be passed to ```aggrid()``` using the ```theme``` arguments.
```ag-theme-balham``` the default light theme provided by ag-grid is set as default. 

The other options available are

1. ag-theme-balham-dark
2. ag-theme-blue
3. ag-theme-bootstrap
4. ag-theme-dark
5. ag-theme-fresh
6. ag-theme-material

Here is an quick example

```r
library(RagGrid)
aggrid(iris,theme = "ag-theme-balham-dark")

```

![](/assets/theme.png)