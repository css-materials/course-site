---
title: "Lecture 1"
date: 2024-09-30T12:25:00-05:00
publishDate: 2019-05-01T12:25:00-05:00
draft: false

# Abstract and optional shortened version.
abstract: ""
summary: "<strong>Course Logistics. Markdown. Git/GitHub in RStudio.</strong>"

# Links (optional).
url_pdf: ""
#url_slides: "/slides/git-github-and-rmarkdown/"  # old slides
url_slides: "/slides/intro-condensed/"
url_video: ""
url_code: ""

# Does the content use math formatting?
math: false

---




## Overview 

* Understand course objectives, logistics, and expectations
* Distinguish between R scripts (`.R`), Markdown documents (`.md`), and R Markdown documents (`.Rmd`)
* Identify and use the main components of R Markdown
* Familiarize with the Git and GitHub in RStudio workflow


## Before class

* Complete [this pre-course survey](https://forms.gle/ypujHgoPino1ndfx9)
* If you do not have one, create a free [GitHub account](https://happygitwithr.com/github-acct) and add your GitHub username to [this sheet](https://docs.google.com/spreadsheets/d/1M5crNtuDO-X8UrqwvTA-ekbPom-j7NO-Y5dzvDKY7-I/edit?usp=sharing); once we have your username we will send an email invitation to join our GitHub organization, please accept it
* [Setup your computer](https://computing-soc-sci.netlify.app/setup/): we encourage everyone to follow option 1 (please allow enough time as this task take might take a while)
* Make sure your Setup works as expected by completing our [Using Git within R Studio](/setup/git/git-with-rstudio) tutorial


## Readings

RStudio and R Markdown:
* Required: [Chapter 27 "R Markdown"](https://r4ds.had.co.nz/r-markdown.html) from "R for Data Science" 1st Edition
* Optional (check as needed):
  * [R Markdown the Definitive Guide](https://bookdown.org/yihui/rmarkdown/)
  * [R Markdown Cheat Sheet](https://www.rstudio.com/wp-content/uploads/2015/02/rmarkdown-cheatsheet.pdf)
  * [Markdown and R Markdown](https://pjbartlein.github.io/REarthSysSci/markdown.html) by Pat Bartlein
  * [R Markdown from R Studio](https://rmarkdown.rstudio.com/lesson-1.html) official documentation
  * [RStudio IDE Cheat Sheet](https://raw.githubusercontent.com/rstudio/cheatsheets/main/rstudio-ide.pdf)
  * Check your understanding of R Markdown by exploring [this interactive tutorial]( https://commonmark.org/help/)

Git and GitHub:
* Required: ["What are Git & GitHub?"](https://computing-soc-sci.netlify.app/faq/what-are-git-github/)
* Optional: [Chapter 1 "Why Git? Why GitHub?"](https://happygitwithr.com/big-picture) from "Happy Git and GitHub for the useR" OR read the article linked at the top of that page


## Class materials

Run the code below in your console to download today’s materials: `usethis::use_course("css-materials/intro")`[^local]

[^local]: If you are using R Workbench, ignore this note. If you are using R from your local machine: first install the package by typing in your console `install.packages("usethis")`; then load it with `library(usethis)`; finally run the code.
