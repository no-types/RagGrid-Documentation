+++
title = "Exporting Data"
description = ""
weight = 2
+++


## Export data as CSV in Shiny

You can export the RagGrid data as csv in shiny app. Here is an example shiny application. </br>
Please check out [agGid export](https://www.ag-grid.com/javascript-grid-export/) for all the options that can be used.
```r

library(shiny)
library(htmlwidgets)
library(shinyjs)

jsCode <- '
shinyjs.exportCsv = function() {
// You can also provide other export options here.. (https://www.ag-grid.com/javascript-grid-export/)
var exportOptions = {"fileName":"SampleExport.csv"};
window.tbl1.api.exportDataAsCsv(exportOptions); 
}'

# Define UI for application that draws a histogram
ui <- shinyUI(fluidPage(
  useShinyjs(),
  extendShinyjs(text = jsCode),
  title = 'Use the RagGrid package in shiny',
  h1('A Table Using aggrid'),
  actionButton("btn", "Export Data"),
  fluidRow(
    column(2),
    column(8, RagGrid::RagGridOutput('tbl1')),
    column(2)
  )
))
# Define server logic required to draw a histogram
server <- shinyServer(function(input, output, session) {
  observeEvent(input$btn, {
    js$exportCsv()
  })
  output$tbl1 <- renderRagGrid(
    aggrid(iris,options=list("onGridReady"=JS("function(event) { window.tbl1 =event;}")))
  )
})
# Run the application 
shinyApp(ui = ui, server = server)


```
![](/assets/export-csv.png)

