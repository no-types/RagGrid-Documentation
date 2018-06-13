+++
title = "Frequently asked questions"
description = ""
weight = 3
alwaysopen = true
+++


+ Why is the grid not working on IE 11 ?

This is a bug ( [Link](https://github.com/no-types/RagGrid/issues/10) ). This happens only on the community edition but works on the enterprise edition. We will be creating an issue with ag-grid to see if there's a fix available for this.

+ Why is the grid on Rstudio viewer shows just one row ?

This could be because the embedded browser in rstudio windows doesn't support CSS transform property which is used by ag-grid to position the rows. Please try launching it in chrome or any other modern browsers. 