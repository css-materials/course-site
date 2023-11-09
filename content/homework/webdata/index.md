---
title: "HW06: Collecting and analyzing data from the web"
date: 2023-11-7T13:30:00-06:00  # Schedule page publish date
type: book
toc: true
draft: false
categories: []
weight: 60
---



# Overview

**Due Thursday, November 16th (11:59 PM).**

We learned two main ways of collecting data from the web: using APIs (with and without ad-hoc packages that wrap APIs), and scraping a website directly. The goal of this assignment is to practice your scraping skills and review previously acquired data manipulation and visualization skills. 


# Accessing the `hw06` repository

* Go [at this link](https://classroom.github.com/a/xOJgAbBN) to accept and create your private `hw06` repository on GitHub. Once you do so, your repository will be built in a few seconds. It follows the naming convention `hw06-<USERNAME>`  
* Once your repository has been created, click on the link you see, which will take you to your repository. 
* Finally, clone the repository to your R Workbench (or your computer if you have installed R there) following the process below.

Notice that, unlike previous assignments, the repo you clone for this assignment is almost empty: **you will have to add your scraped data and code** to the repo (and push them to your Github repo).


# Cloning your `hw06` repository and general workflow

After you have accessed the `hw06` repository (see above), follow the [same steps you completed for `hw01`](/homework/edit-readme/) to clone the repository.


# Assignment description

For this assignment, you will create a new dataset by getting data from the web and analyzing it. You can create a new dataset by using an API or by directly scraping a website. This assignment is more open-ended than the previous. Below are the expected tasks you should accomplish and some rules to follow.

**Assignment tasks:**

1. Scrape your data (directly or with an API)
1. Clean and wrangle your scraped data: the end result must be a cleaned and tidy data frame. This task will vary depending on your project: some scraping projects require lots of data cleaning and wrangling, others do not.
1. Save your scraped data as a `.csv` file and upload that file(s) in your repository.
1. Add a data analysis component (exploratory descriptions and visualizations) that shows something interesting about your data; it is up to you to decide what to display and how. To give you some reference: I expect that the extent of the data analysis will vary depending on how challenging it was to get the data (if you set up a complex scraper, the data cleaning/wrangling/visualization should be minimal; if you use an R wrapper for an API that has lots of resources, the data cleaning/wrangling/visualization should be more extended -- ask me if in doubt).
1. Submit code that works (e.g., no bugs, document your code, etc.)[^repro]. The expected minimal complexity of the scraping code, should be along the same lines of the "presidential statements" example that we saw in class (for scraping), including functions and anything else that would make the scraper more efficient; or should be a full developed example (with R wrapper package for an API) that explores several functions provided by the wrapper. You can use, but need to substantially expand on, the examples we have reviewed in class. 


**Rules of the game** (please read!): 

  * Everything that is publicly available can be scraped (see slides on what is defined as "public data") VS. everything that is password protected cannot be scraped (private data that requires a username and passcode cannot be scraped; if you need to log in to scrape data, do not scrape them).
  * If you are interested in scraping data from a given social media, I suggest using their APIs; in general, if there is an API, use the API and do not scrape. Some websites have stricter rules, and they make them explicit, either in their robots.txt or Terms of Service (ToS).  
  * If you want to use an API, I recommend selecting one with an R wrapper; I advise against interacting directly with APIs for this assignment, but you can do so if you want. If you do not know where to start, you can find inspiration [in this list of APIs]( https://ucsd.libguides.com/c.php?g=90743&p=3202435) (you need to check that the API you want to use has a R wrapper).
  * If you plan to use an API, store authentication keys/passwords in a secure way, as shown in class.
  * If you plan to scrape a website, do not scrape pages that have dynamic components (e.g., if you need to scroll down a page to visualize the data, or need to click on pop-up windows, etc. -- those websites require advanced scraping skills that are not covered in this course; if you would like to that in any case, contact me first).
  * If you need additional packages, you should be able to install packages on your own on Workbench, but please try it out earlier rather than later and let me know if you run into issues.
  * Quote all sources you consulted and explain (in your reflections) how you used them. You are welcome to find inspirations/suggestions from online tutorials, assigned readings, etc. However, if students rely upon online sources, they must quote them and explain what they added/modified. The code produced for the assignment must be mostly novel and written by you (e.g., it cannot mirror code found from online sources). 
  * **Please notice**: we have not tested or run code for all possible websites and APIs that exist in this world. Please, refrain from asking the instructional staff questions on how to use a specific API or scrape a specific website. This homework's primary goal is for you to commit to one specific API that you find interesting and learn how to get data from it, or to commit to one specific website you want to get data from and learn how to scrape it.


# Submit the assignment

Your repo should include everything you have used to collect the data and produce your analyses (R Markdown files, data files, etc.). Submit also the data you collected.

Your code should be put in a `Rmd` file and knitted as `md`. Make sure to stage-commit-push your original `.Rmd` file, knit it as `.md` (e.g., `github_document`) and submit both the `.Rmd` and `.md`

Your `.Rmd` should read as a tutorial (along the same lines of the four examples shared on Wednesday class): start with a description of the API (and of the API wrapper for R) or a description of the webpage you are scraping. More generally, other than your R code, make sure to include textual explanation that allows us to understand your work.

When you are ready to submit, copy your repository URL (e.g. https://github.com/css-fall23/hw6-brinasab) and submit it on Canvas under HW06 before the deadline. Do not submit files on Canvas, we only need the link to your repository 

As part of your submission:
  * write 1-2 paragraphs of reflections about the homework
  * list the first and last name of eventual collaborators with whom you worked with to complete this assignment
  * list all the resources you consulted
  

# Assessment

All homework assignments are evaluated using [this general rubric](/faq/homework-evaluations/). Make sure to check it. 

Below are further guidelines for this specific homework to help you assess your work before submitting it.

*Needs improvement:* Data collection requires short/elementary code, and/or so do the analyses (e.g., graphs do not include any element more than basic ggplot code, they are unclear, and/or don't have appropriate labels or formatting). There is little attention to reproducibility issues and little consistency in the code's style. Code might not run or has bugs

*Good:* Solid effort. Hits all the elements. Finished all components of the assignment with only minor deficiencies. Easy to follow (both the code and the output). 

*Excellent:* Displays in-depth understanding of course materials, including data analysis and coding skills. Write complex and refined code to get data and/or to produce graphs and tables. An appropriate way to store authentication keys/passwords is implemented (if using an API or API wrapper).

[^repro]: If you are scraping from a web page that frequently updates its content, we may not perfectly reproduce your results. That's fine - just make sure you've saved a copy of the data frame in the repo (as a `.csv`). Same for APIs that have an authentication key. 
