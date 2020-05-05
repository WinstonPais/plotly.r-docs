---
description: How to make interactive 3D mesh plots in R.
display_as: 3d_charts
language: r
layout: base
name: 3D Mesh Plots
order: 4
output:
  html_document:
    keep_md: true
page_type: example_index
permalink: r/3d-mesh/
redirect_from: r/3d-mesh-plots/
thumbnail: thumbnail/3d-mesh.jpg
---


### Basic 3D Mesh Plot


```r
library(plotly)

x <- runif(50, 0, 1)
y <- runif(50, 0, 1)
z <- runif(50, 0, 1)

fig <- plot_ly(x = ~x, y = ~y, z = ~z, type = 'mesh3d')

fig
```

<div id="htmlwidget-b5c7419f43d151ffdc56" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-b5c7419f43d151ffdc56">{"x":{"visdat":{"8f2a614a1c7c":["function () ","plotlyVisDat"]},"cur_data":"8f2a614a1c7c","attrs":{"8f2a614a1c7c":{"x":{},"y":{},"z":{},"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"mesh3d"}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"scene":{"xaxis":{"title":"x"},"yaxis":{"title":"y"},"zaxis":{"title":"z"}},"hovermode":"closest","showlegend":false,"legend":{"yanchor":"top","y":0.5}},"source":"A","config":{"showSendToCloud":false},"data":[{"colorbar":{"title":"z","ticklen":2,"len":0.5,"lenmode":"fraction","y":1,"yanchor":"top"},"colorscale":[["0","rgba(68,1,84,1)"],["0.0416666666666667","rgba(70,19,97,1)"],["0.0833333333333334","rgba(72,32,111,1)"],["0.125","rgba(71,45,122,1)"],["0.166666666666667","rgba(68,58,128,1)"],["0.208333333333333","rgba(64,70,135,1)"],["0.25","rgba(60,82,138,1)"],["0.291666666666667","rgba(56,93,140,1)"],["0.333333333333333","rgba(49,104,142,1)"],["0.375","rgba(46,114,142,1)"],["0.416666666666667","rgba(42,123,142,1)"],["0.458333333333333","rgba(38,133,141,1)"],["0.5","rgba(37,144,140,1)"],["0.541666666666667","rgba(33,154,138,1)"],["0.583333333333333","rgba(39,164,133,1)"],["0.625","rgba(47,174,127,1)"],["0.666666666666667","rgba(53,183,121,1)"],["0.708333333333333","rgba(79,191,110,1)"],["0.75","rgba(98,199,98,1)"],["0.791666666666667","rgba(119,207,85,1)"],["0.833333333333333","rgba(147,214,70,1)"],["0.875","rgba(172,220,52,1)"],["0.916666666666667","rgba(199,225,42,1)"],["0.958333333333333","rgba(226,228,40,1)"],["1","rgba(253,231,37,1)"]],"showscale":true,"x":[0.214698284631595,0.658104601316154,0.92619433416985,0.242881301790476,0.980826378799975,0.715424614958465,0.354607758112252,0.403090787585825,0.010229054838419,0.255997870117426,0.504948619287461,0.275259478483349,0.220769990701228,0.98666011588648,0.172015481162816,0.183341811178252,0.295098324306309,0.00577001995407045,0.912318429909647,0.97620682627894,0.89055868703872,0.318775548832491,0.558248400921002,0.282851276919246,0.76747287181206,0.105565674137324,0.397273935610428,0.456491397460923,0.561295472783968,0.0703345856163651,0.897309684660286,0.673998055513948,0.720308479154482,0.861854655668139,0.0272819045931101,0.319516485324129,0.20596045255661,0.377318119397387,0.751615065149963,0.442053479840979,0.284449378494173,0.4781984614674,0.0426843140739948,0.955288231838495,0.322316608857363,0.598957221955061,0.811878559645265,0.139179779449478,0.212580838939175,0.907943803351372],"y":[0.815415602643043,0.660147761926055,0.661742234602571,0.920297779142857,0.156757398508489,0.71059442916885,0.767442520475015,0.947505976539105,0.002587795490399,0.475391125539318,0.654897987144068,0.312002488411963,0.36825216258876,0.287779807113111,0.577814742689952,0.69487326592207,0.635315257823095,0.62286533229053,0.469974191160873,0.74307479034178,0.155078273033723,0.485657618613914,0.505414186744019,0.928152790293097,0.517968113999814,0.841829077340662,0.325420136097819,0.665376337477937,0.89856447186321,0.392119449796155,0.644709536572918,0.171103355241939,0.757434089202434,0.80694159399718,0.198804337764159,0.0421029422432184,0.0776980835944414,0.228875951841474,0.513265741989017,0.854617961682379,0.307498754467815,0.965836042072624,0.974265817087144,0.217352410079911,0.138368586543947,0.604583556996658,0.465138896368444,0.782367344480008,0.18677178863436,0.416592057328671],"z":[0.300279582850635,0.778318794444203,0.78711152006872,0.538889012765139,0.89433696330525,0.552560042822734,0.512002986390144,0.973147113341838,0.97925801272504,0.484642741736025,0.663700549863279,0.322337444638833,0.342770327581093,0.837277566781268,0.964165105251595,0.452311476692557,0.317272483836859,0.816365338861942,0.495936333201826,0.818470858968794,0.397482887143269,0.336209163535386,0.332533427746966,0.960300556384027,0.987108506960794,0.249921227339655,0.94586448254995,0.905174709158018,0.670403392054141,0.57406890206039,0.455260400893167,0.997874348424375,0.594468121416867,0.626956358086318,0.0540119651705027,0.683550737099722,0.457666369155049,0.987750204512849,0.483862982364371,0.829544573789462,0.969313508365303,0.930340014165267,0.367741540307179,0.655562865082175,0.930493001593277,0.952957851579413,0.0956371792126447,0.60579344118014,0.0739824576303363,0.682391915237531],"type":"mesh3d","frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script>

### Tetrahedron Mesh Plot


```r
library(plotly)

fig <- plot_ly(type = 'mesh3d',
  x = c(0, 1, 2, 0),
  y = c(0, 0, 1, 2),
  z = c(0, 2, 0, 1),
  i = c(0, 0, 0, 1),
  j = c(1, 2, 3, 2),
  k = c(2, 3, 1, 3),
  intensity = c(0, 0.33, 0.66, 1),
  color = c(0, 0.33, 0.66, 1),
  colors = colorRamp(c("red", "green", "blue"))
)

fig
```

<div id="htmlwidget-47105cb81463e3c5e02f" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-47105cb81463e3c5e02f">{"x":{"visdat":{"8f2ac6517a9":["function () ","plotlyVisDat"]},"cur_data":"8f2ac6517a9","attrs":{"8f2ac6517a9":{"x":[0,1,2,0],"y":[0,0,1,2],"z":[0,2,0,1],"i":[0,0,0,1],"j":[1,2,3,2],"k":[2,3,1,3],"intensity":[0,0.33,0.66,1],"color":[0,0.33,0.66,1],"colors":["function (x) ","roundcolor(cbind(palette[[1L]](x), palette[[2L]](x), palette[[3L]](x), ","    if (alpha) palette[[4L]](x))) * 255"],"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"mesh3d"}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"scene":{"xaxis":{"title":[]},"yaxis":{"title":[]},"zaxis":{"title":[]}},"hovermode":"closest","showlegend":false,"legend":{"yanchor":"top","y":0.5}},"source":"A","config":{"showSendToCloud":false},"data":[{"colorbar":{"title":"","ticklen":2,"len":0.5,"lenmode":"fraction","y":1,"yanchor":"top"},"colorscale":[["0","rgba(255,0,0,1)"],["0.0416666666666667","rgba(234,21,0,1)"],["0.0833333333333333","rgba(212,42,0,1)"],["0.125","rgba(191,64,0,1)"],["0.166666666666667","rgba(170,85,0,1)"],["0.208333333333333","rgba(149,106,0,1)"],["0.25","rgba(128,128,0,1)"],["0.291666666666667","rgba(106,149,0,1)"],["0.333333333333333","rgba(85,170,0,1)"],["0.375","rgba(64,191,0,1)"],["0.416666666666667","rgba(43,212,0,1)"],["0.458333333333333","rgba(21,234,0,1)"],["0.5","rgba(0,255,0,1)"],["0.541666666666667","rgba(0,234,21,1)"],["0.583333333333333","rgba(0,213,42,1)"],["0.625","rgba(0,191,64,1)"],["0.666666666666667","rgba(0,170,85,1)"],["0.708333333333333","rgba(0,149,106,1)"],["0.75","rgba(0,128,128,1)"],["0.791666666666667","rgba(0,106,149,1)"],["0.833333333333333","rgba(0,85,170,1)"],["0.875","rgba(0,64,191,1)"],["0.916666666666667","rgba(0,43,212,1)"],["0.958333333333333","rgba(0,21,234,1)"],["1","rgba(0,0,255,1)"]],"showscale":true,"x":[0,1,2,0],"y":[0,0,1,2],"z":[0,2,0,1],"i":[0,0,0,1],"j":[1,2,3,2],"k":[2,3,1,3],"intensity":[0,0.33,0.66,1],"type":"mesh3d","marker":{"line":{"colorbar":{"title":"","ticklen":2},"cmin":0,"cmax":1,"colorscale":[["0","rgba(255,0,0,1)"],["0.0416666666666667","rgba(234,21,0,1)"],["0.0833333333333333","rgba(212,42,0,1)"],["0.125","rgba(191,64,0,1)"],["0.166666666666667","rgba(170,85,0,1)"],["0.208333333333333","rgba(149,106,0,1)"],["0.25","rgba(128,128,0,1)"],["0.291666666666667","rgba(106,149,0,1)"],["0.333333333333333","rgba(85,170,0,1)"],["0.375","rgba(64,191,0,1)"],["0.416666666666667","rgba(43,212,0,1)"],["0.458333333333333","rgba(21,234,0,1)"],["0.5","rgba(0,255,0,1)"],["0.541666666666667","rgba(0,234,21,1)"],["0.583333333333333","rgba(0,213,42,1)"],["0.625","rgba(0,191,64,1)"],["0.666666666666667","rgba(0,170,85,1)"],["0.708333333333333","rgba(0,149,106,1)"],["0.75","rgba(0,128,128,1)"],["0.791666666666667","rgba(0,106,149,1)"],["0.833333333333333","rgba(0,85,170,1)"],["0.875","rgba(0,64,191,1)"],["0.916666666666667","rgba(0,43,212,1)"],["0.958333333333333","rgba(0,21,234,1)"],["1","rgba(0,0,255,1)"]],"showscale":false,"color":[0,0.33,0.66,1]}},"frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script>

### Cube Mesh Plot


```r
library(plotly)

fig <- plot_ly(type = 'mesh3d',
  x = c(0, 0, 1, 1, 0, 0, 1, 1),
  y = c(0, 1, 1, 0, 0, 1, 1, 0),
  z = c(0, 0, 0, 0, 1, 1, 1, 1),
  i = c(7, 0, 0, 0, 4, 4, 6, 6, 4, 0, 3, 2),
  j = c(3, 4, 1, 2, 5, 6, 5, 2, 0, 1, 6, 3),
  k = c(0, 7, 2, 3, 6, 7, 1, 1, 5, 5, 7, 6),
  intensity = seq(0, 1, length = 8),
  color = seq(0, 1, length = 8),
  colors = colorRamp(rainbow(8))
)

fig
```

<div id="htmlwidget-63aa33aaa001f29668e3" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-63aa33aaa001f29668e3">{"x":{"visdat":{"8f2a3155b3dd":["function () ","plotlyVisDat"]},"cur_data":"8f2a3155b3dd","attrs":{"8f2a3155b3dd":{"x":[0,0,1,1,0,0,1,1],"y":[0,1,1,0,0,1,1,0],"z":[0,0,0,0,1,1,1,1],"i":[7,0,0,0,4,4,6,6,4,0,3,2],"j":[3,4,1,2,5,6,5,2,0,1,6,3],"k":[0,7,2,3,6,7,1,1,5,5,7,6],"intensity":[0,0.142857142857143,0.285714285714286,0.428571428571429,0.571428571428571,0.714285714285714,0.857142857142857,1],"color":[0,0.142857142857143,0.285714285714286,0.428571428571429,0.571428571428571,0.714285714285714,0.857142857142857,1],"colors":["function (x) ","roundcolor(cbind(palette[[1L]](x), palette[[2L]](x), palette[[3L]](x), ","    if (alpha) palette[[4L]](x))) * 255"],"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"mesh3d"}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"scene":{"xaxis":{"title":[]},"yaxis":{"title":[]},"zaxis":{"title":[]}},"hovermode":"closest","showlegend":false,"legend":{"yanchor":"top","y":0.5}},"source":"A","config":{"showSendToCloud":false},"data":[{"colorbar":{"title":"","ticklen":2,"len":0.5,"lenmode":"fraction","y":1,"yanchor":"top"},"colorscale":[["0","rgba(255,0,0,1)"],["0.0416666666666667","rgba(255,56,0,1)"],["0.0833333333333333","rgba(255,111,0,1)"],["0.125","rgba(255,167,0,1)"],["0.166666666666667","rgba(234,202,0,1)"],["0.208333333333333","rgba(197,220,0,1)"],["0.25","rgba(160,239,0,1)"],["0.291666666666667","rgba(123,255,3,1)"],["0.333333333333333","rgba(85,255,21,1)"],["0.375","rgba(48,255,40,1)"],["0.416666666666667","rgba(11,255,59,1)"],["0.458333333333333","rgba(0,255,104,1)"],["0.5","rgba(0,255,160,1)"],["0.541666666666667","rgba(0,255,215,1)"],["0.583333333333333","rgba(0,239,255,1)"],["0.625","rgba(0,183,255,1)"],["0.666666666666667","rgba(0,128,255,1)"],["0.708333333333333","rgba(0,72,255,1)"],["0.75","rgba(32,48,255,1)"],["0.791666666666667","rgba(69,29,255,1)"],["0.833333333333333","rgba(107,11,255,1)"],["0.875","rgba(144,0,247,1)"],["0.916666666666667","rgba(181,0,228,1)"],["0.958333333333333","rgba(218,0,210,1)"],["1","rgba(255,0,191,1)"]],"showscale":true,"x":[0,0,1,1,0,0,1,1],"y":[0,1,1,0,0,1,1,0],"z":[0,0,0,0,1,1,1,1],"i":[7,0,0,0,4,4,6,6,4,0,3,2],"j":[3,4,1,2,5,6,5,2,0,1,6,3],"k":[0,7,2,3,6,7,1,1,5,5,7,6],"intensity":[0,0.142857142857143,0.285714285714286,0.428571428571429,0.571428571428571,0.714285714285714,0.857142857142857,1],"type":"mesh3d","marker":{"line":{"colorbar":{"title":"","ticklen":2},"cmin":0,"cmax":1,"colorscale":[["0","rgba(255,0,0,1)"],["0.0416666666666667","rgba(255,56,0,1)"],["0.0833333333333333","rgba(255,111,0,1)"],["0.125","rgba(255,167,0,1)"],["0.166666666666667","rgba(234,202,0,1)"],["0.208333333333333","rgba(197,220,0,1)"],["0.25","rgba(160,239,0,1)"],["0.291666666666667","rgba(123,255,3,1)"],["0.333333333333333","rgba(85,255,21,1)"],["0.375","rgba(48,255,40,1)"],["0.416666666666667","rgba(11,255,59,1)"],["0.458333333333333","rgba(0,255,104,1)"],["0.5","rgba(0,255,160,1)"],["0.541666666666667","rgba(0,255,215,1)"],["0.583333333333333","rgba(0,239,255,1)"],["0.625","rgba(0,183,255,1)"],["0.666666666666667","rgba(0,128,255,1)"],["0.708333333333333","rgba(0,72,255,1)"],["0.75","rgba(32,48,255,1)"],["0.791666666666667","rgba(69,29,255,1)"],["0.833333333333333","rgba(107,11,255,1)"],["0.875","rgba(144,0,247,1)"],["0.916666666666667","rgba(181,0,228,1)"],["0.958333333333333","rgba(218,0,210,1)"],["1","rgba(255,0,191,1)"]],"showscale":false,"color":[0,0.142857142857143,0.285714285714286,0.428571428571429,0.571428571428571,0.714285714285714,0.857142857142857,1]}},"frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script>

#Reference

See [https://plotly.com/r/reference/#mesh3d](https://plotly.com/r/reference/#mesh3d) for more information and chart attribute options!

### What About Dash?

[Dash for R](https://dashr.plot.ly/) is an open-source framework for building analytical applications, with no Javascript required, and it is tightly integrated with the Plotly graphing library. 

Learn about how to install Dash for R at https://dashr.plot.ly/installation.

Everywhere in this page that you see `fig`, you can display the same figure in a Dash for R application by passing it to the `figure` argument of the [`Graph` component](https://dashr.plot.ly/dash-core-components/graph) from the built-in `dashCoreComponents` package like this:


```r
library(plotly)

fig <- plot_ly() 
# fig <- fig %>% add_trace( ... )
# fig <- fig %>% layout( ... ) 

library(dash)
library(dashCoreComponents)
library(dashHtmlComponents)

app <- Dash$new()
app$layout(
    htmlDiv(
        list(
            dccGraph(figure=fig) 
        )
     )
)

app$run_server(debug=TRUE, dev_tools_hot_reload=FALSE)
```
