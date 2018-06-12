+++
title = "Cell Formatting"
description = ""
weight = 4
+++

## Conditional Cell Formatting

Here's an example of how you can conditionally color the table cells using cellStyling callback of aggrid. 

Let's color the negative values of Column A in red color.

```r
library(RagGrid)
m = cbind(matrix(rnorm(60, 1e5, 1e6), 20), runif(20), rnorm(20, 100))
colnames(m) = head(LETTERS, ncol(m))
 colorIfNegative = JS("function(params) {
                        if (params.value < 0) {
                                return {color: 'white', backgroundColor: 'red'};
                            } else {
                                return null;
                            }
                        }").
 colOpts <- list("A"=list("cellStyle"=colorIfNegative))
 aggrid(m,colOpts = colOpts)

```
![](/assets/cell-formatting.png)

Check out [Aggrid Cell Styling](https://www.ag-grid.com/javascript-grid-cell-styling/) to know more about cell formatting.
