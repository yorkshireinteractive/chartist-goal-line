---
title: Chartist Goal Line Demo
description: A simple Chartist JavaScript plugin to put goal lines on your charts
layout: default.html
---

# Chartist Goal Line Demo

A simple Chartist JavaScript plugin to put goal lines on your charts. Check out the
project page too: <a
href="https://github.com/YorkshireInteractive/chartist-bar-labels">YorkshireInteractive/chartist-goal-line</a>.

      
## Default usage

<div class="ct-chart"><img src="images/ct-chart.png"></div>

```js
var chart1 = new Chartist.Bar('.ct-chart', {
  labels: ['Feb', 'Mar', 'Apr', 'May'],
  series: [
    [19, 15, 9, 13]
  ],
  },{
  height: 400,
  axisY: {
    onlyInteger: true
  },
  plugins: [
    Chartist.plugins.ctTargetLine({
      value: 14
    })
  ]
});
```
      

## Horizontal bar usage

<div class="ct-chart-2"><img src="images/ct-chart-2.png"></div>

```js
var chart2 = new Chartist.Bar('.ct-chart-2', {
  labels: ['% to Campaign Goal', '% to Prior Month', '% to Prior Year'],
  series: [
    [127, 211, 146]
  ]
}, {
  chartPadding: {
    right: 50
  },
  height: 350,
  horizontalBars: true,
  reverseData: true,
  axisX: {
    labelInterpolationFnc: function(value) {
      return value + '%';
    },
    onlyInteger: true,
  },
  axisY: {
    offset: 135,
  },
  plugins: [
    Chartist.plugins.ctTargetLine({
      value: 100,
      axis: 'x'
    })
  ]
});
```
