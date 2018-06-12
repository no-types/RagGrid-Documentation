+++
title = "Enterprise Options"
description = ""
weight = 2
+++


## Enterprise mode

Enterprise mode will be enabled by passing the ```licenseKey``` option. Enterprise provides a lot of features like row grouping, pivoting, status bar.

```r
aggrid(iris,licenseKey=<YOUR LICENSE KEY>)
```

### Enterpise Demo
![](/assets/enterprise-options.gif)


### Default Grid options - Enterprise edition ( + Community Edition )

| Property        | Value           |
| ------------- |:-------------:|
| enableStatusBar    | true |
| alwaysShowStatusBar      | false      |
| suppressDragLeaveHidesColumns | true      |
| suppressMakeColumnVisibleAfterUnGroup | true      |
