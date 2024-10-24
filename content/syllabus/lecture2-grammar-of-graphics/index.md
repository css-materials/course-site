---
title: "Lecture 2"
date: 2024-10-02T12:25:00-05:00
publishDate: 2019-04-03T12:25:00-05:00
draft: false

aliases: ["/cm002.html"]

# Abstract and optional shortened version.
abstract: ""
summary: "<strong>Grammar of Graphics and ggplot2. Coding style in R.</strong>"

# Links (optional).
url_pdf: ""
url_slides: "/slides/visualizations-and-the-grammar-of-graphics/"
url_video: ""
url_code: ""

# Does the content use math formatting?
math: false

---



## Overview

* Identify the importance of graphics in data analysis
* Define the layered grammar of graphics
* Practice generating layered graphics using [`ggplot2`](https://github.com/hadley/ggplot2)
* Learn best practices for coding style in R


## Before class

* Make sure your setup is completed and works as expected! See the "Before class" from Lecture 1 for details, and let us know (via Ed Discussion) if you have questions!
* Check [Homework 1](https://computing-soc-sci.netlify.app/homework/edit-readme/)


## Readings

Coding style:
* [Chapter 4 "Workflow: code style"](https://r4ds.hadley.nz/workflow-style) from "R for Data Science" 2nd Edition
* ["The `tidyverse` style guide"](https://style.tidyverse.org/index.html): skim it for today, and refer back to it whenever you are unsure!

Grammar of Graphics and `ggplot2`:
* Required: read ["Chapter 1 Data visualization"](https://r4ds.hadley.nz/data-visualize) from "R for Data Science" 2nd Edition. To be able to follow today's lecture, you need to read this chapter! 
* Recommended: read Hadley Wickham [A Layered Grammar of Graphics](https://vita.had.co.nz/papers/layered-grammar.html) -- the "pre-print" version of the article can be downloaded for free. This article is optional, but I encourage you to skim through it to familiarize yourself with the theory behind the Grammar of Graphics. See especially section 3 "Components of the Layered Grammar" and section 4 "A Hierarchy of Defaults." Understanding the logic of the Grammar of Graphics will make it much easier to apply it in R
    
Additional resources on `ggplot2` (check these out whenever you need to make plots for this class or later on):
* [ggplot2 Cheat Sheet](https://raw.githubusercontent.com/rstudio/cheatsheets/main/data-visualization.pdf)
* [ggplot2 Documentation](https://ggplot2.tidyverse.org/index.html)
* [ggplot2: Elegant Graphics for Data Analysis, 2nd Edition](https://ggplot2-book.org/) by Hadley Wickham. Excellent resource for learning the intricacies of `ggplot2`
* [R Graphics Cookbook, 2nd edition](https://r-graphics.org/) by Winston Chang. A practical guide with 150 examples to generate quality statistical graphics based on the data you wish to present
* [Tufte, Edward R. The Visual Display of Quantitative Information.](https://www.edwardtufte.com/tufte/books_vdqi) Classic book on statistical graphics and visualization design.
* [Healey, Kieran. Data Visualization: A Practical Guide.](https://socviz.co/) An applied introduction to graphical design with lots of code examples.


## Class materials

<!--
In-class materials (exercises and code) will be posted here shortly before class.
-->

Run the code below in your console to download today’s materials: `usethis::use_course("css-materials/grammar-of-graphics")`[^local]

<!--
More info
* [The Grammar of Graphics](/notes/grammar-of-graphics/)
Exercise solutions can be found [here](https://jrnold.github.io/r4ds-exercise-solutions/).
ggplot2:
* Why do we learn the `ggplot2` graphics library and not the base [`graphics`](https://cran.r-project.org/web/views/Graphics.html) system? David Robinson explains it well in [Don't teach built-in plotting to beginners (teach ggplot2)](http://varianceexplained.org/r/teach_ggplot2_to_beginners/), and follows up with a defense of `ggplot2` in [Why I use ggplot2](http://varianceexplained.org/r/why-I-use-ggplot2/)
-->

[^local]: If you are using R from your local machine: make sure you have installed "usethis" (see Lecture 1 footnote to install it) and  "gapminder" by typing `install.packages("gapminder")` in your console 
