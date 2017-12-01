---
title       : reproducible-researchR
subtitle    : An app
date        : 2017-11-30
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Introduction

This is the documentation for an app created for the final project in coursera's data products course.

The app not only performs calculations, but it lets the user edit the calculations by presenting an RMarkdown scripting environment within the app.

---

## Usage

To edit the markdown rendering, edit the markdown text within the textbox.
If rendering is taking a long time, you may wish to temporarily disable rendering by toggling the "Update continuously" checkbox.

Use normal rmarkdown, like:

```r
str(mtcars)
```

```
## 'data.frame':	32 obs. of  11 variables:
##  $ mpg : num  21 21 22.8 21.4 18.7 18.1 14.3 24.4 22.8 19.2 ...
##  $ cyl : num  6 6 4 6 8 6 8 4 4 6 ...
##  $ disp: num  160 160 108 258 360 ...
##  $ hp  : num  110 110 93 110 175 105 245 62 95 123 ...
##  $ drat: num  3.9 3.9 3.85 3.08 3.15 2.76 3.21 3.69 3.92 3.92 ...
##  $ wt  : num  2.62 2.88 2.32 3.21 3.44 ...
##  $ qsec: num  16.5 17 18.6 19.4 17 ...
##  $ vs  : num  0 0 1 1 0 1 0 1 1 1 ...
##  $ am  : num  1 1 1 0 0 0 0 0 0 0 ...
##  $ gear: num  4 4 4 3 3 3 3 4 4 4 ...
##  $ carb: num  4 4 1 1 2 1 4 2 2 4 ...
```

---

## Calculations

The app essentially runs reactive code when the textbox contents change.
It saves the textbox contents to file and runs a markdown rendering to html, updating the UiOutput.
It's not much different than doing this in RStudio, but it is your shiny session that is doing the rendering.

---

## Reporting Results

Once you are satisfied with your markdown document, you can print it to pdf, docx, or html.
The app will perform a server-side rendering of your RMarkdown and download the resulting document.
You can then print the report and hand it to your boss to put on the company fridge.

Have a great day!
