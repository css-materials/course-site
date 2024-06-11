---
title: "2. Data Visualization & the grammar of graphics"
date: 2024-06-11T12:25:00-05:00
publishDate: 2019-04-03T12:25:00-05:00
draft: false

aliases: ["/cm002.html"]

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
#time_end: 2022-08-24T14:20:00-05:00
all_day: false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors: []

# Abstract and optional shortened version.
abstract: ""
summary: "Topics: introduction to data visualizations; ggplot2 and the grammar of graphics; coding style."

# Location of event.
location: ""

# Is this a selected talk? (true/false)
selected: false

# Tags (optional).
#   Set `tags: []` for no tags, or use the form `tags: ["A Tag", "Another Tag"]` for one or more tags.
tags: []

# Links (optional).
url_pdf: ""
url_slides: "/slides/visualizations-and-the-grammar-of-graphics/"
url_video: ""
url_code: ""

# Does the content use math formatting?
math: false
---



## Overview

* Identify the importance of graphics in communicating information
* Define the layered grammar of graphics
* Demonstrate how to use layered grammar of graphics
* Practice generating layered graphics using [`ggplot2`](https://github.com/hadley/ggplot2)


## Before class

Tasks:

* Make sure your setup is completed and works as expected! See the "Before class" from [Lecture 1](https://computing-soc-sci.netlify.app/syllabus/1.-introduction-to-the-course-and-software-setup/) and let us know (OHs, Ed Discussion) if you have questions!
* [Homework 1](https://computing-soc-sci.netlify.app/homework/edit-readme/) is due tomorrow, Wednesday June 12. Let us know if you have questions!

Readings:

* Required: read ["Chapter 1 Data visualization"](https://r4ds.hadley.nz/data-visualize) from "R for Data Science" 2nd Edition. To be able to follow today's lecture, you need to read this chapter. 
* Optional: read Hadley Wickham [A Layered Grammar of Graphics](https://vita.had.co.nz/papers/layered-grammar.html) -- the "pre-print" version of the article can be downloaded for free. This article is optional, but I encourage you to skim through it to familiarize with the theory of the grammar of graphics; especially section 3 "Components of the Layered Grammar" and section 4 "A Hierarchy of Defaults." Understanding the "logic" of the Grammar of Graphic will make using it in R much easier.
    

## Class materials

Run the code below in your console to download today’s materials: `usethis::use_course("css-materials/grammar-of-graphics")`[^local]

<!--
More info
* [The Grammar of Graphics](/notes/grammar-of-graphics/)
Exercise solutions can be found [here](https://jrnold.github.io/r4ds-exercise-solutions/).
-->

## Additional resources

Cheatsheets
* [Data visualization with ggplot2 cheat sheet](https://raw.githubusercontent.com/rstudio/cheatsheets/main/data-visualization.pdf)
* [RStudio IDE Cheat Sheet](https://raw.githubusercontent.com/rstudio/cheatsheets/main/rstudio-ide.pdf)

Graphical design
* [Tufte, Edward R. *The Visual Display of Quantitative Information*.](https://www.edwardtufte.com/tufte/books_vdqi) Classic book on statistical graphics and visualization design.
* [Healey, Kieran. *Data Visualization: A Practical Guide*.](https://socviz.co/) An applied introduction to graphical design with lots of applications in `ggplot2` and many code examples.

ggplot2
* Why do we learn the `ggplot2` graphics library and not the base [`graphics`](https://cran.r-project.org/web/views/Graphics.html) system? David Robinson explains it well in [Don't teach built-in plotting to beginners (teach ggplot2)](http://varianceexplained.org/r/teach_ggplot2_to_beginners/), and follows up with a defense of `ggplot2` in [Why I use ggplot2](http://varianceexplained.org/r/why-I-use-ggplot2/)
* [ggplot2: Elegant Graphics for Data Analysis, 2nd Edition](https://ggplot2-book.org/) -- Hadley Wickham. Excellent resource for learning the intricacies of `ggplot2`.
* [R Graphics Cookbook, 2nd edition](https://r-graphics.org/) -- Winston Chang. A practical guide with 150 examples to generate quality statistical graphics based on the data you wish to present.
* [Documentation for ggplot2](https://ggplot2.tidyverse.org/index.html)


[^local]: If you are using R from your local machine: make sure you have installed "usethis" (see Lecture 1 footnote to install it) and  "gapminder" by typing `install.packages("gapminder")` in your console 

<!--
Optional:
* [How to build a complicated, layered graphic](/notes/minard/)
* [Exploring Minard's 1812 plot with `ggplot2`](https://github.com/andrewheiss/fancy-minard) - a much fancier (and more complex) version
-->
