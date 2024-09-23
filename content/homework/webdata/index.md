---
title: "HW06: Collecting and analyzing data from the web"
date: 2024-07-09T13:30:00-06:00  # Schedule page publish date
type: book
toc: true
draft: true
categories: []
weight: 60
---



# Overview

**Due Tuesday, July 16th (11:59 PM).**

This past week, we learned two main methods for collecting data from the web:

* directly scraping websites
* using APIs (with and without ad-hoc R wrapper packages that wrap APIs) 

The goals of this assignment are (1) to practice your web scraping skills using one of these two methods of your choice, and (2) to review and apply your previously acquired data manipulation and visualization skills (practice makes perfect!).


# Accessing and cloning your `hw06` repository

* Go [at this link](https://classroom.github.com/a/0UfENWcR) to accept the invitation and create your private `hw06` repository on GitHub. Once you do so, your repo will be built in a few seconds. It follows the naming convention `hw06-<USERNAME>`
* Once your repository has been created, click on the provided link to access it. 
* Finally, follow the [same steps you completed for `hw01`](/homework/edit-readme/) to clone the repository to your R Workbench.

Notice that, unlike previous assignments, the repo you clone for this assignment is almost empty: **you will have to add your scraped data and code** to the Git repo, and push them to your Github online repo.

Refer to Homework 1 for the General Git/GitHub workflow to follow.


# Assignment description

For this assignment, you will gather data from the web and analyze it. You can either use an API or scrape a website directly. This assignment is more flexible than the previous ones, giving you a chance to dive into something that interests you!

No matter what your project is, you are expected to complete the following tasks and adhere to the guidelines provided below. If you have any questions, feel free to reach out!


## Assignment tasks:

**1. Scrape your data with an API or directly.**

You can scrape anything that interests you, with either method (API or direct scraping). Here are some guidelines and suggestions:

* If you choose to scrape using an API, we strongly recommend selecting an API with an R wrapper for ease of use. If you are unsure which API to choose, consider the following options that have been successful for previous students:
  * NYT API
  * Spotify API
  * Manifesto or Census APIs: Tutorials for both can be found in the in-class materials for [Lecture 16](https://computing-soc-sci.netlify.app/syllabus/16.-getting-data-from-the-web-api/). Use these tutorials as a foundation and expand upon them.
  * Any examples mentioned in the assigned readings listed in [Lecture 15](https://computing-soc-sci.netlify.app/syllabus/15.-getting-data-from-the-web-scraping/)

* If you prefer to scrape directly, and are unsure what to scrape, consider the following sources that have proven successful for previous students:
  * Presidential Statements: Refer to the in-class tutorial from Lecture 15 and build upon it (e.g., scrape different content from the same website and/or tackle the challenges at the end of that tutorial).
  * Wikipedia
  * Websites from UChicago (e.g., MACSS website) or other universities
  * Any examples mentioned in the assigned readings listed in [Lecture 15](https://computing-soc-sci.netlify.app/syllabus/15.-getting-data-from-the-web-scraping/)


**2. Clean and wrangle your scraped data.**

The final outcome should be a cleaned and tidy data frame. Save your scraped data as a `.csv` file(s) and upload that file(s) in your repository. 

The extent of data cleaning and wrangling will vary based on your project: 

* Some scraping projects may require extensive data manipulation, such as unnesting nested lists or using regular expressions to clean text, while others may require minimal cleaning.
* If your project requires less cleaning and wrangling (e.g., only a few lines of code), consider adding complexity to your scraper to balance out. See next point for more. 


**3. Include data analysis with exploratory descriptions and visualizations**

These should show something interesting to you about your data. It is up to you to decide what to display and how: as long as they make sense, and they follow what we have learned in this course, will accept them! 

As a guideline, the extent of your data analysis and visualization should correspond to the complexity of obtaining your data (point 1 above) and cleaning/wrangling them (point 2 above). For example: 

 * If you develop a complex and unique scraper (e.g., one that performs beyond basic functions and is not adapted from other sources) and you need to conduct extensive data cleaning and wrangling, your data analysis and visualization efforts can be minimal (e.g., basic descriptive statistics and one or two well-done graphs).
 
* Conversely, if your scraping task is less extensive — such as using an API with a well-documented R wrapper, adapting an online tutorial (note that "adapting" means modifying and making it your own, as copying code is considered plagiarism), or building upon in-class tutorials — your data analysis and visualization efforts should be more detailed. This might involve performing more in-depth exploratory analysis and creating multiple comprehensive graphs. If you are unsure, feel free to ask for guidance!


**4. Your `.Rmd` should read as a tutorial**

Your final report should be read as a tutorial, and be clear and well-explained. Refer to the tutorials from Lectures 15 and 16 as examples. In addition to your R code and analysis, include textual explanations to ensure that we fully understand your work; make sure to include a description of the API and API wrapper for R, or of the webpage you are scraping.



## Further guidelines (please read!): 

  * You can scrape any data that is publicly available. You cannot scrape any data that is password protected or requires a username and passcode to access (if you need to log in to access the data, do not scrape it). Refer to the slides for the definition of "public VS private data."
  
  * If you plan on using an API, I recommend the following:
    * Select an API with an R wrapper, ideally a wrapper that is up to date. I advise against interacting directly with APIs without wrappers for this assignment. If you do not know where to start, you can find inspiration [in this list of APIs]( https://ucsd.libguides.com/c.php?g=90743&p=3202435) (check that the API you want to use has a R wrapper).
    * Using social media APIs is not recommended for this assignment, as it has become increasingly difficult to access or obtain API permissions in a timely manner. However, if you have a specific idea in mind, feel free to check with me. My suggestions aim to minimize potential frustrations, but I am happy to work with you to check project feasibility!
    * Most APIs require registration to use them. Complete this process as early as possible, as it can sometimes be immediate but may also take longer. Ensure you store authentication keys and passwords securely, as demonstrated in class.
  
  * If you plan to scrape a website directly, do not scrape websites with dynamic components (e.g., if you need to scroll down to load all the data, or need to click on pop-up windows). These websites require advanced scraping skills that are not covered in this course; if you are unsure, feel free to check in with me!
  
  * If you need additional packages, you should be able to install them on your own in Workbench. Please try installing any required packages as early as possible, and let me know if you encounter any issues.
  
  * How do I know if I have "done enough"? 
    * While it is difficult to provide a precise estimate of the time needed, you can use the average time you spent on each previous assignment as a reference
    * Make sure to follow the instructions
  
  
## Notes on getting help and plagiarism 

* Quote All Sources: Cite all the sources you consulted and explain in your reflections how you used them. You are welcome to draw inspiration from online tutorials, assigned readings, and other resources, including AI. However, if you rely on online sources, we expect you to cite them (at the end of your `.Rmd`) and explain what you added or modified. The code you produce for the assignment must be primarily original and written by you; it should not closely replicate code found from online sources.

* Note on getting help: We haven't tested or run code for every website and API. We are happy to help you debugging, but ensure you study the API or website you are scraping beforehand. The primary goal of this homework is for you to choose an API or website that interests you and learn how to extract data from it independently!


# Submit the assignment

To submit the assignment, follow these steps:

* First push to your repository the last version of your assignment before the deadline. 
    * Your repo should include everything you have used to collect the data and produce your analyses (R Markdown files, data files, plots, etc.). Submit also the data you collected, unless they are too big (see the Final Project on what this means)
    * Your code should be put in a `Rmd` file and knitted as `md`. Make sure to stage-commit-push your original `.Rmd` file, knit it as `.md` (e.g., `github_document`) and submit both the `.Rmd` and `.md`

* When you are ready to submit, copy your repository URL (e.g. https://github.com/css-summer24/hw6-brinasab) and submit it on Canvas under HW06 before the deadline. Do not submit files on Canvas, we only need the link to your repository 

* As part of your submission, at the end of your `.Rmd` file write 1-2 paragraphs of reflections about the homework (what was hard/easy, what you learned, use of AI, list the resources you used, etc.)


# Assessment

All homework assignments are evaluated using a rubric: see [here](/faq/homework-evaluations/) and [here](https://docs.google.com/spreadsheets/d/1h7_TmhUr5k7BGT3h-F4VJMUEEUtvvhqw/edit?usp=sharing&ouid=112534119211880791899&rtpof=true&sd=true) (this file is also accessible from the top of the "Lectures" page from our website).

Further guidelines for this specific homework to help you assessing your work before submitting it:
In the past, "Excellent" or "Very good" work included submissions that
completed all components of the assignment correctly and demonstrated an in-depth understanding of course materials on scraping, including data analysis and coding skills. The code was clear and refined, effectively retrieving data and producing graphs and tables. Code was functionalized where appropriate, and secure methods were implemented for storing authentication keys or passwords when using an API and/or API wrapper. The scraper went beyond the basics and showcased the student's ability to write their own code. Multiple commits were made with meaningful messages, showing a progression in the work and providing a backup.
