+++
title = "Frequently asked questions"
description = ""
weight = 8
+++


## Why is the table in rstudio(Windows) viewer shows one row ?

This could be because the embedded browser in rstudio windows doesn't support CSS transform property which is used by ag-grid to position the rows. It will work fine if you use open it in chrome or any other modern browsers. 


## Why is the grid not working on IE 11 ?

This is a bug ( link to bug in our GitHub issues ). This happens only on the community edition but works on the enterprise edition. We will be creating an issue with ag-grid to see if there's a fix available for this.
