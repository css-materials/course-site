---
title: "Introduction to computing for the social sciences"
date: 2023-09-27T12:25:00-05:00
publishDate: 2019-08-01T12:25:00-05:00
draft: false

aliases: ["/cm001.html", "/syllabus/introduction-to-computing-for-the-social-sciences/"]

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
#time_end: 2022-08-22T14:20:00-05:00
all_day: false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors: []

# Abstract and optional shortened version.
abstract: ""
summary: "Topics: course logistics; overview of programming and reproducible research; intro to R."

# Location of event.
location: MACSS Bldg, Room 295

# Is this a selected talk? (true/false)
selected: false

# Tags (optional).
#   Set `tags: []` for no tags, or use the form `tags: ["A Tag", "Another Tag"]` for one or more tags.
tags: []

# Links (optional).
url_pdf: ""
url_slides: "/slides/intro/"
url_video: ""
url_code: ""

# Does the content use math formatting?
math: false
---



## Overview

* Understand course objectives, logistics, and expectations
* Familiarize with basic principles of programming and reproducible workflow
* Overview of basic R syntax
* Install and troubleshoot the required software


## Before class

* If you do not have one already, create a free [GitHub account](https://happygitwithr.com/github-acct). As a university student, also check to see if you are eligible for [GitHub Education offers](https://education.github.com/). Some of these are very useful, such as unlimited private repositories. Remember that once you create a GitHub account, you are stuck with that username: choose something professional. 
* Complete [this survey](https://forms.gle/4avJpvcPseP1NQpB8)
* [Setup your computer](https://computing-soc-sci.netlify.app/setup/)
* Readings (we will review them only briefly in class, I take for granted you have read them):
  * Chapter 1 "Introduction" and Chapter 4 "Workflow Basics" in [R for Data Science](http://r4ds.had.co.nz/)
  * [Introduction to the course](/notes/intro-to-course/) 


## Class materials

* Access RStudio Workbench [here](https://macss-r.uchicago.edu/s/57ea13c286bd33c286bd3/auth-sign-in?appUri=%2Fworkspaces%2F)
* Run the code below in your console to download today’s materials: `usethis::use_course("css-materials/intro-r")`[^local]


## Additional resources

* Practice your R skills with [DataCamp free Introduction to R course](https://www.datacamp.com/courses/free-introduction-to-r) (module one is free, the other modules require a subscription) 
* Read [Good Enough Practices in Scientific Computing](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510)

[^local]: If you are using R from your local machine: first install the package by typing in your console `install.packages("usethis")`; then load it with `library(usethis)`; finally run the code. If you are using Workbench, everything is already installed for you.
