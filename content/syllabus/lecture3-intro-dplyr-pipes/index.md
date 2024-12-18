---
title: "Lecture 3"
date: 2024-10-07T12:25:00-05:00
publishDate: 2019-04-08T12:25:00-05:00
draft: false

aliases: ["/cm003.html"]

# Abstract and optional shortened version.
abstract: ""
summary: "<strong>Introduction to dplyr. Operators. Pipes.</strong>"

# Links (optional).
url_pdf: ""
url_slides: "/slides/data-transformation/"
url_video: ""
url_code: ""

# Does the content use math formatting?
math: false
---




## Overview

* Think at programming as a form of problem solving
* Learn the most important dplyr "verbs" for data manipulation
* Familiarize with "pipes"
* Understand and correctly utilize logical operators


## Before class

* This applies ONLY if you have installed R/RStudio locally (ignore this if you are using Workbench): 
    * Install the [`rcis`](https://github.com/css-materials/rcis) library by running the command `remotes::install_github("css-materials/rcis")` in your console. We will be using data from this package in class.
    * If you do not already have the `remotes` library installed, you will get an error. Install it first running `install.packages("remotes")`
    
    
## Readings

Data transformation with `dplyr`:
* Read ["Chapter 3 Data transformation"](https://r4ds.hadley.nz/data-transform) from "R for Data Science" 2nd Edition. To be able to follow today's lecture, you need to read this chapter!
* [dplyr Cheat Sheet](https://rstudio.github.io/cheatsheets/html/data-transformation.html)
* [dplyr Documentation](https://dplyr.tidyverse.org/)


## Class materials

<!--
In-class materials (exercises and code) will be posted here shortly before class.
-->

Run the code below in your console to download today’s materials: `usethis::use_course("css-materials/data-transformation")`


<!--
* [Computer programming as a form of problem solving](/notes/problem-solving/)
* [`dplyr` in brief](/notes/dplyr/)
* [Practice transforming college education data](/notes/transform-college/)
* [Pipes in R](/notes/pipes/) taken from "Functions" lecture of Oct 25
* Complete your peer evaluations for homework 01. Review the following:
    * [General Homework Rubric](/faq/homework-evaluations/)
    * [Performing peer review](/faq/peer-evaluations/)
    * To find which peers you will evaluate:
        * Navigate to the [course organization page on GitHub](https://github.coecis.cornell.edu/cis-fa22)
        * Find the `hw01` repos you can see that are not your own repo
        * Open the repos and find the pull request. You can then initiate a [code review](https://github.com/features/code-review) to leave detailed feedback.
-->
