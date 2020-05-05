---
name: geom_errorbar
permalink: ggplot2/geom_errorbar/
description: Examples of geom_errobar in R and ggplot2
layout: base
thumbnail: thumbnail/error-bar.jpg
language: ggplot2
page_type: example_index
display_as: statistics
order: 2
output:
  html_document:
    keep_md: true
---


### Basic Error Bar


```r
library(plotly)

df <- data.frame(x = 1:10,
                 y = 1:10,
                 ymin = (1:10) - runif(10),
                 ymax = (1:10) + runif(10),
                 xmin = (1:10) - runif(10),
                 xmax = (1:10) + runif(10))

p <- ggplot(data = df,aes(x = x,y = y)) + 
    geom_point() + 
    geom_errorbar(aes(ymin = ymin,ymax = ymax)) + 
    geom_errorbarh(aes(xmin = xmin,xmax = xmax))

fig <- ggplotly(p)

fig
```

<div id="htmlwidget-04a8b05464d2177e6393" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-04a8b05464d2177e6393">{"x":{"data":[{"x":[1,2,3,4,5,6,7,8,9,10],"y":[1,2,3,4,5,6,7,8,9,10],"text":["x:  1<br />y:  1","x:  2<br />y:  2","x:  3<br />y:  3","x:  4<br />y:  4","x:  5<br />y:  5","x:  6<br />y:  6","x:  7<br />y:  7","x:  8<br />y:  8","x:  9<br />y:  9","x: 10<br />y: 10"],"type":"scatter","mode":"markers","marker":{"autocolorscale":false,"color":"rgba(0,0,0,1)","opacity":1,"size":5.66929133858268,"symbol":"circle","line":{"width":1.88976377952756,"color":"rgba(0,0,0,1)"}},"hoveron":"points","showlegend":false,"xaxis":"x","yaxis":"y","hoverinfo":"text","frame":null},{"x":[1,2,3,4,5,6,7,8,9,10],"y":[1,2,3,4,5,6,7,8,9,10],"text":["ymin: 0.3957514<br />ymax:  1.293297<br />x:  1<br />y:  1","ymin: 1.5092966<br />ymax:  2.947228<br />x:  2<br />y:  2","ymin: 2.4248633<br />ymax:  3.032028<br />x:  3<br />y:  3","ymin: 3.9449888<br />ymax:  4.405556<br />x:  4<br />y:  4","ymin: 4.5885687<br />ymax:  5.776324<br />x:  5<br />y:  5","ymin: 5.7407845<br />ymax:  6.763464<br />x:  6<br />y:  6","ymin: 6.5912222<br />ymax:  7.458298<br />x:  7<br />y:  7","ymin: 7.7827978<br />ymax:  8.831165<br />x:  8<br />y:  8","ymin: 8.2389830<br />ymax:  9.575145<br />x:  9<br />y:  9","ymin: 9.2804516<br />ymax: 10.903669<br />x: 10<br />y: 10"],"type":"scatter","mode":"lines","opacity":1,"line":{"color":"transparent"},"error_y":{"array":[0.293296896386892,0.947228127392009,0.0320284406188875,0.405556270852685,0.776324481004849,0.763464235933498,0.458297616802156,0.831165010575205,0.575145334471017,0.903669187799096],"arrayminus":[0.604248624760658,0.490703424671665,0.575136683648452,0.0550112368073314,0.411431342130527,0.259215527446941,0.408777780598029,0.217202178901061,0.761017023120075,0.71954835113138],"type":"data","width":18.5123966942149,"symmetric":false,"color":"rgba(0,0,0,1)"},"showlegend":false,"xaxis":"x","yaxis":"y","hoverinfo":"text","frame":null},{"x":[1,2,3,4,5,6,7,8,9,10],"y":[1,2,3,4,5,6,7,8,9,10],"text":["xmin: 0.8793793<br />xmax:  1.291705<br />x:  1<br />y:  1","xmin: 1.0272102<br />xmax:  2.453277<br />x:  2<br />y:  2","xmin: 2.2331808<br />xmax:  3.011180<br />x:  3<br />y:  3","xmin: 3.7730360<br />xmax:  4.193144<br />x:  4<br />y:  4","xmin: 4.8387706<br />xmax:  5.238419<br />x:  5<br />y:  5","xmin: 5.4136717<br />xmax:  6.977255<br />x:  6<br />y:  6","xmin: 6.9052555<br />xmax:  7.105952<br />x:  7<br />y:  7","xmin: 7.8628794<br />xmax:  8.027861<br />x:  8<br />y:  8","xmin: 8.7339340<br />xmax:  9.439316<br />x:  9<br />y:  9","xmin: 9.8225662<br />xmax: 10.296307<br />x: 10<br />y: 10"],"type":"scatter","mode":"lines","opacity":1,"line":{"color":"transparent"},"error_x":{"array":[0.291705493815243,0.45327657670714,0.0111798611469567,0.193143600597978,0.238418797962368,0.977254833327606,0.105952437501401,0.0278610095847398,0.439316260162741,0.29630735469982],"arrayminus":[0.120620678178966,0.972789831226692,0.76681924238801,0.226963988738135,0.161229432094842,0.58632827270776,0.0947445118799806,0.13712059147656,0.266066010342911,0.177433838834986],"type":"data","width":12.4581380673362,"symmetric":false,"color":"rgba(0,0,0,1)"},"showlegend":false,"xaxis":"x","yaxis":"y","hoverinfo":"text","frame":null}],"layout":{"margin":{"t":26.2283105022831,"r":7.30593607305936,"b":40.1826484018265,"l":31.4155251141553},"plot_bgcolor":"rgba(235,235,235,1)","paper_bgcolor":"rgba(255,255,255,1)","font":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187},"xaxis":{"domain":[0,1],"automargin":true,"type":"linear","autorange":false,"range":[0.0550000000000001,10.945],"tickmode":"array","ticktext":["2.5","5.0","7.5","10.0"],"tickvals":[2.5,5,7.5,10],"categoryorder":"array","categoryarray":["2.5","5.0","7.5","10.0"],"nticks":null,"ticks":"outside","tickcolor":"rgba(51,51,51,1)","ticklen":3.65296803652968,"tickwidth":0.66417600664176,"showticklabels":true,"tickfont":{"color":"rgba(77,77,77,1)","family":"","size":11.689497716895},"tickangle":-0,"showline":false,"linecolor":null,"linewidth":0,"showgrid":true,"gridcolor":"rgba(255,255,255,1)","gridwidth":0.66417600664176,"zeroline":false,"anchor":"y","title":{"text":"x","font":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187}},"hoverformat":".2f"},"yaxis":{"domain":[0,1],"automargin":true,"type":"linear","autorange":false,"range":[-0.129644515388645,11.4290650784271],"tickmode":"array","ticktext":["0","3","6","9"],"tickvals":[0,3,6,9],"categoryorder":"array","categoryarray":["0","3","6","9"],"nticks":null,"ticks":"outside","tickcolor":"rgba(51,51,51,1)","ticklen":3.65296803652968,"tickwidth":0.66417600664176,"showticklabels":true,"tickfont":{"color":"rgba(77,77,77,1)","family":"","size":11.689497716895},"tickangle":-0,"showline":false,"linecolor":null,"linewidth":0,"showgrid":true,"gridcolor":"rgba(255,255,255,1)","gridwidth":0.66417600664176,"zeroline":false,"anchor":"x","title":{"text":"y","font":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187}},"hoverformat":".2f"},"shapes":[{"type":"rect","fillcolor":null,"line":{"color":null,"width":0,"linetype":[]},"yref":"paper","xref":"paper","x0":0,"x1":1,"y0":0,"y1":1}],"showlegend":false,"legend":{"bgcolor":"rgba(255,255,255,1)","bordercolor":"transparent","borderwidth":1.88976377952756,"font":{"color":"rgba(0,0,0,1)","family":"","size":11.689497716895}},"hovermode":"closest","barmode":"relative"},"config":{"doubleClick":"reset","showSendToCloud":false},"source":"A","attrs":{"19704dd8c1ef":{"x":{},"y":{},"type":"scatter"},"19704d1e12a9":{"ymin":{},"ymax":{},"x":{},"y":{}},"197055cb601d":{"xmin":{},"xmax":{},"x":{},"y":{}}},"cur_data":"19704dd8c1ef","visdat":{"19704dd8c1ef":["function (y) ","x"],"19704d1e12a9":["function (y) ","x"],"197055cb601d":["function (y) ","x"]},"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script>

### Margin Error Bar


```r
library(plotly)

population <- data.frame(Year=seq(1790, 1970, length.out=length(uspop)), 
                         Population=uspop, 
                         Error=rnorm(length(uspop), 5))

library(ggplot2)
p <- ggplot(population, aes(x=Year, y=Population, 
                       ymin=Population-Error, ymax=Population+Error))+
  geom_line()+
  geom_point(pch=2)+
  geom_errorbar(width=0.9)

fig <- ggplotly(p)

fig
```

<div id="htmlwidget-75ee5ec562c1065667cf" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-75ee5ec562c1065667cf">{"x":{"data":[{"x":[1790,1800,1810,1820,1830,1840,1850,1860,1870,1880,1890,1900,1910,1920,1930,1940,1950,1960,1970],"y":[3.93,5.31,7.24,9.64,12.9,17.1,23.2,31.4,39.8,50.2,62.9,76,92,105.7,122.8,131.7,151.3,179.3,203.2],"text":["Year: 1790<br />Population:   3.93<br />Population - Error:  -1.0897653<br />Population + Error:   8.949765","Year: 1800<br />Population:   5.31<br />Population - Error:   0.5202076<br />Population + Error:  10.099792","Year: 1810<br />Population:   7.24<br />Population - Error:   4.1374919<br />Population + Error:  10.342508","Year: 1820<br />Population:   9.64<br />Population - Error:   4.4018853<br />Population + Error:  14.878115","Year: 1830<br />Population:  12.90<br />Population - Error:   8.8408517<br />Population + Error:  16.959148","Year: 1840<br />Population:  17.10<br />Population - Error:  11.7035027<br />Population + Error:  22.496497","Year: 1850<br />Population:  23.20<br />Population - Error:  19.6079545<br />Population + Error:  26.792046","Year: 1860<br />Population:  31.40<br />Population - Error:  27.4883275<br />Population + Error:  35.311672","Year: 1870<br />Population:  39.80<br />Population - Error:  32.8771906<br />Population + Error:  46.722809","Year: 1880<br />Population:  50.20<br />Population - Error:  44.0225666<br />Population + Error:  56.377433","Year: 1890<br />Population:  62.90<br />Population - Error:  57.7419350<br />Population + Error:  68.058065","Year: 1900<br />Population:  76.00<br />Population - Error:  69.6935499<br />Population + Error:  82.306450","Year: 1910<br />Population:  92.00<br />Population - Error:  86.2203306<br />Population + Error:  97.779669","Year: 1920<br />Population: 105.70<br />Population - Error: 101.5964872<br />Population + Error: 109.803513","Year: 1930<br />Population: 122.80<br />Population - Error: 116.5440435<br />Population + Error: 129.055956","Year: 1940<br />Population: 131.70<br />Population - Error: 126.5539399<br />Population + Error: 136.846060","Year: 1950<br />Population: 151.30<br />Population - Error: 146.3276796<br />Population + Error: 156.272320","Year: 1960<br />Population: 179.30<br />Population - Error: 173.7347713<br />Population + Error: 184.865229","Year: 1970<br />Population: 203.20<br />Population - Error: 198.1957442<br />Population + Error: 208.204256"],"type":"scatter","mode":"lines+markers","line":{"width":1.88976377952756,"color":"transparent","dash":"solid"},"hoveron":"points","showlegend":false,"xaxis":"x","yaxis":"y","hoverinfo":"text","marker":{"autocolorscale":false,"color":"rgba(0,0,0,1)","opacity":1,"size":5.66929133858268,"symbol":"triangle-up-open","line":{"width":1.88976377952756,"color":"rgba(0,0,0,1)"}},"opacity":1,"error_y":{"array":[5.01976533410629,4.78979237114787,3.10250809145722,5.23811474272095,4.0591482571518,5.39649729710803,3.59204554797888,3.91167245196004,6.92280938572637,6.17743343033118,5.15806498494313,6.30645012389765,5.77966942654008,4.10351284588396,6.25595649884035,5.1460600780967,4.97232039151064,5.56522871864428,5.00425577770613],"arrayminus":[5.01976533410629,4.78979237114787,3.10250809145721,5.23811474272095,4.0591482571518,5.39649729710803,3.59204554797888,3.91167245196004,6.92280938572637,6.17743343033118,5.15806498494312,6.30645012389765,5.77966942654008,4.10351284588396,6.25595649884035,5.1460600780967,4.97232039151064,5.56522871864428,5.00425577770613],"type":"data","width":1.01311623699693,"symmetric":false,"color":"rgba(0,0,0,1)"},"frame":null}],"layout":{"margin":{"t":26.2283105022831,"r":7.30593607305936,"b":40.1826484018265,"l":43.1050228310502},"plot_bgcolor":"rgba(235,235,235,1)","paper_bgcolor":"rgba(255,255,255,1)","font":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187},"xaxis":{"domain":[0,1],"automargin":true,"type":"linear","autorange":false,"range":[1780.505,1979.495],"tickmode":"array","ticktext":["1800","1850","1900","1950"],"tickvals":[1800,1850,1900,1950],"categoryorder":"array","categoryarray":["1800","1850","1900","1950"],"nticks":null,"ticks":"outside","tickcolor":"rgba(51,51,51,1)","ticklen":3.65296803652968,"tickwidth":0.66417600664176,"showticklabels":true,"tickfont":{"color":"rgba(77,77,77,1)","family":"","size":11.689497716895},"tickangle":-0,"showline":false,"linecolor":null,"linewidth":0,"showgrid":true,"gridcolor":"rgba(255,255,255,1)","gridwidth":0.66417600664176,"zeroline":false,"anchor":"y","title":{"text":"Year","font":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187}},"hoverformat":".2f"},"yaxis":{"domain":[0,1],"automargin":true,"type":"linear","autorange":false,"range":[-11.5544663896969,218.668956833297],"tickmode":"array","ticktext":["0","50","100","150","200"],"tickvals":[0,50,100,150,200],"categoryorder":"array","categoryarray":["0","50","100","150","200"],"nticks":null,"ticks":"outside","tickcolor":"rgba(51,51,51,1)","ticklen":3.65296803652968,"tickwidth":0.66417600664176,"showticklabels":true,"tickfont":{"color":"rgba(77,77,77,1)","family":"","size":11.689497716895},"tickangle":-0,"showline":false,"linecolor":null,"linewidth":0,"showgrid":true,"gridcolor":"rgba(255,255,255,1)","gridwidth":0.66417600664176,"zeroline":false,"anchor":"x","title":{"text":"Population","font":{"color":"rgba(0,0,0,1)","family":"","size":14.6118721461187}},"hoverformat":".2f"},"shapes":[{"type":"rect","fillcolor":null,"line":{"color":null,"width":0,"linetype":[]},"yref":"paper","xref":"paper","x0":0,"x1":1,"y0":0,"y1":1}],"showlegend":false,"legend":{"bgcolor":"rgba(255,255,255,1)","bordercolor":"transparent","borderwidth":1.88976377952756,"font":{"color":"rgba(0,0,0,1)","family":"","size":11.689497716895}},"hovermode":"closest","barmode":"relative"},"config":{"doubleClick":"reset","showSendToCloud":false},"source":"A","attrs":{"19702d8cab4c":{"x":{},"y":{},"ymin":{},"ymax":{},"type":"scatter"},"197059fbf08a":{"x":{},"y":{},"ymin":{},"ymax":{}},"19707d45606b":{"x":{},"y":{},"ymin":{},"ymax":{}}},"cur_data":"19702d8cab4c","visdat":{"19702d8cab4c":["function (y) ","x"],"197059fbf08a":["function (y) ","x"],"19707d45606b":["function (y) ","x"]},"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script>

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
