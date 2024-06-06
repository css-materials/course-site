---
title: "Data transformation: intro to dplyr & pipes"
date: 2024-06-12T12:25:00-05:00
publishDate: 2019-04-08T12:25:00-05:00
draft: false

aliases: ["/cm003.html"]

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
#time_end: 2022-08-29T14:20:00-05:00
all_day: false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors: []

# Abstract and optional shortened version.
abstract: ""
summary: "Topics: programming as problem-solving; operators; fundamental dplyr verbs for data manipulation; pipes."

# Location of event.
location: ""

# Is this a selected talk? (true/false)
selected: false

# Tags (optional).
#   Set `tags: []` for no tags, or use the form `tags: ["A Tag", "Another Tag"]` for one or more tags.
tags: []

# Links (optional).
url_pdf: ""
#url_slides: "/slides/data-transformation/"
url_video: ""
url_code: ""

# Does the content use math formatting?
math: false
---



## Overview

* Think at programming as a form of problem solving
* Identify the most common dplyr "verbs" for data manipulation
* Familiarize with "pipes"
* Operators


## Before class

* Read ["Chapter 3 Data transformation"](https://r4ds.hadley.nz/data-transform) from "R for Data Science" 2nd Edition. To be able to follow today's lecture, you need to read this chapter. 
* This applies only if you have installed R/RStudio locally: 
    * Install the [`rcis`](https://github.com/css-materials/rcis) library from GitHub. To do so, run the command `remotes::install_github("css-materials/rcis")` in your console. We will be using data from this package in class.
    * If you do not already have the `remotes` library installed, you will get an error. Install it first using `install.packages("remotes")`, then run `remotes::install_github("css-materials/rcis")`.
    

## Class materials

TBA. In-class materials (code, exercises, etc.) will be posted right before class.

<!--
* Run the code below in your console to download today’s materials: `usethis::use_course("css-materials/data-transformation")`
-->


## Additional resources

* Cheat sheet [Data Wrangling with `dplyr` and `tidyr`](https://www.rstudio.com/wp-content/uploads/2015/02/data-wrangling-cheatsheet.pdf)


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
