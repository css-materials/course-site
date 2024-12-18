---
title: "Lecture 13"
date: 2024-11-11T12:25:00-05:00
publishDate: 2019-06-03T12:25:00-05:00
draft: false

aliases: ["/cm017.html"]

# Abstract and optional shortened version.
abstract: ""
summary: "<strong>Working with Strings & Regular Expressions.</strong>"

# Links (optional).
url_pdf: ""
url_slides: "/slides/regular-expr/"
url_video: ""
url_code: ""

# Does the content use math formatting?
math: false
---




## Overview

* Define Strings, Regular Expressions, and their uses
* Introduce the `stringr()` package
* Practice using Regular Expressions in R to extract info from strings


## Before class

Let me know what you want to review about past Homework Assignments: [HW2 review](https://forms.gle/VeCzrcWmNXPoaQ2m8) and [HW3 review](https://forms.gle/J15wyAsD8bNU2Yzy9). I will pick two questions for each assigment based on your suggestions. 

See [this Ed Post](https://edstem.org/us/courses/68248/discussion/5659934) for more info about the changes we are going to implement in the course based on the mid-quarter feedback. Thanks!


## Readings

* Read [Chapter 14 "Strings"](https://r4ds.hadley.nz/strings) in "R for Data Science" 2nd Edition (read it all, especially 14.4 "Extracting data from strings")
* Read [Chapter 17](https://bookdown.org/rdpeng/rprogdatascience/regular-expressions.html#the-stringr-package) from *R Programming for Data Science*. This book covers the entire range of regular expressions packages and functions: you do not need to understand everything, but you might want to refer back to this when needed. In-class we focus on `stringr()`
* [`stringr()` documentation and cheatsheet](https://stringr.tidyverse.org/)
* Optional: [Chapter 15](https://plsc-31101.github.io/course/strings-and-regular-expressions.html#applying-regex) by Rochelle Terman, further explains `stringr()` using the *R for Data Science* textbook


## Class materials 

<!--
In-class materials (exercises and code) will be posted here shortly before class.
-->

Run the code below in your console to download today’s in-class materials: `usethis::use_course("css-materials/regular-expr")`

