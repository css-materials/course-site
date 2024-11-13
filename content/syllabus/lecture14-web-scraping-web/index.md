---
title: "Lecture 14"
date: 2024-11-13T12:25:00-05:00
publishDate: 2019-05-15T12:25:00-05:00
draft: false

aliases: ["/cm016.html"]

# Abstract and optional shortened version.
abstract: ""
summary: "<strong>Getting Data from the Web: Scraping.</strong>"

# Links (optional).
url_pdf: ""
url_slides: "/slides/getting-data-from-the-web-scraping/"
url_video: ""
url_code: ""

# Does the content use math formatting?
math: false
---




## Overview

* Understand the difference between web-scraping and Application Program Interface (API)
* Define HTML and CSS selectors
* Introduce the `rvest` package for scraping in R
* Demonstrate how to extract information from HTML pages
* Practice scraping data


## Before class

Several packages are needed for this and next lectures on the topic. They are all already installed on R Workbench. But if you are using R from your laptop (VS. R Workbench), I'd suggest following the scraping lectures using Workbench. 

<!--
Explore the readings and Install on your web browser (e.g., Chrome), the "Selector Gadget" tool, and explore how to use it to select tags.
-->


## Readings

Readings for all lectures on the topic (both direct web-scraping and scraping using APIs) are posted here.

General Introductions:
* Chapter 1 and 4 in [Web Scraping with R](https://steviep42.github.io/webscraping/book/)
* [`rvest` documentation](https://rvest.tidyverse.org/articles/harvesting-the-web.html)
* [`httr` documentation](https://cran.r-project.org/web/packages/httr/)
* [Web Scraping using R Cheat Sheet](https://github.com/yusuzech/r-web-scraping-cheat-sheet/blob/master/README.md)

Articles that summarize the scraping workflow:
  * [Web scraping with R](https://williammarble.co/files/webscraping_tutorial/webscraping_tutorial.pdf) by William Marble
  * [Web scraping using R](https://journals.sagepub.com/doi/pdf/10.1177/2515245919859535) by Alex Bradley and Richard J. E. James

API resources:
[Install-and-play API packages for R](https://github.com/ropensci/webservices)


## Class materials

Run the code below in your console to download today’s in-class exercises: `usethis::use_course("css-materials/getting-data-from-the-web-scraping")`

<!--
In-class materials (exercises and code) will be posted here shortly before class.
-->

<!--
* [Web scraping](/notes/web-scraping/)
* `rvest`
    * Load the library (`library(rvest)`)
    * `demo("tripadvisor")` - scraping a Trip Advisor page
    * `demo("united")` - how to scrape a web page which requires a login
    * [Scraping IMDB](https://blog.rstudio.org/2014/11/24/rvest-easy-web-scraping-with-r/)
-->
