---
title: "HW06: Collecting and analyzing data from the web"
date: 2024-11-13T13:30:00-06:00  # Schedule page publish date
type: book
toc: true
draft: false
categories: []
weight: 60
---




# Overview

**Due ~~Thursday, November 21st~~ Friday, November 22nd (11:59 PM).**

*The deadline has been extended to the last day before the break, allowing some extra time to incorporate content from Monday’s lecture (11/18), if you wish to do so.*

This past week, we began a new module on web scraping: an applied module designed to integrate substantive knowledge (e.g., web scraping concepts) with the R skills you have developed so far. We have introduced two main methods for collecting data from the web: direct scraping and accessing data through APIs. This assignment focuses exclusively on direct scraping.

<!-- with or without specific R packages designed to interact with those APIs. --> 


# Accessing and cloning your `hw06` repository

* Go [at this link](https://classroom.github.com/a/553DpYYR) to accept the invitation and create your private `hw06` repository on GitHub. Once you do so, your repo will be built in a few seconds. It follows the naming convention `hw06-<USERNAME>`
* Once your repository has been created, click on the provided link to access it. 
* Finally, follow the [same steps you completed for `hw01`](/homework/edit-readme/) to clone the repository to your R Workbench.

Unlike previous assignments, the repo you clone for this assignment is almost empty: **you will need to add your scraped data and your code** to the Git repo, and push them to your Github online repo. See below for details on what to submit. 

Refer to Homework 1 for the General Git/GitHub workflow to follow.


# Assignment description and tasks

<!--For this assignment, you will gather data from the web and analyze it. You can either use an API or scrape a website directly. This assignment is more flexible than the previous ones, giving you a chance to dive into something that interests you!-->

This assignment has two main learning goals: (1) to help you practice and strengthen your web scraping skills, and (2) to review and apply in a new context your previously learned R skills in programming, data manipulation, visualization, etc.
 
For this assignment, you will scrape and analyze web data of your choice, allowing you to focus on something that interests you. Regardless of your focus, ensure your project fully adheres to the guidelines provided below. If you have any questions, don’t hesitate to reach out. 

Your assignment should: scrape data, clean and put them in a dataframe, analyze and visualize them. Submit a report (a `Rmd` knitted as `md`) that incorporates codes and explanation for every step.

### 1. Scrape your data

**What to scrape:**

You can scrape anything that interests you using direct scraping!

<!-- NOTES FALL 2024 TO ADD NEXT TIME
If you are unsure what to scrape, consider the following sources that have proven successful for previous students (ensure that whatever you scrape has data that you can analyze and plot, not only textual info):
  * Websites from UChicago (e.g., MACSS website) or other universities
  * Government websites (usually they have data about socio-economic status, neighborhood, education, etc.)
  * Wikipedia (ensure there are tables or data you can analyze); if the scraping is too straightforward scale up by scraping multiple wiki pages with data you can merge
  * Housing market websites (like the in-class example)
  * Any of the examples mentioned in the assigned readings 
  * U.S. Presidential Statements: build on the scraper we created in class
-->

If you are unsure what to scrape, consider the following sources that have proven successful for previous students:
  * Wikipedia
  * Websites from UChicago (e.g., MACSS website) or other universities
  * Government websites 
  * Any of the examples mentioned in the assigned readings listed in [Lecture 14](https://computing-soc-sci.netlify.app/syllabus/lecture-14/) 
  * U.S. Presidential Statements: build on the scraper we created in class

If you build on in-class materials (e.g., the Presidential Statements scraper), examples from readings, or online tutorials, or any other source that provide a starter code (including AI), your code should go beyond simple adjustments (e.g. beyond changing variable names or changing syntax). It should scrape different content and introduce new elements not included in the original source, such as added functions, loops, or other enhancements that increase the scraper's complexity demonstrating both your unique contribution and your learning.

Feel free to use tools like the "SelectorGadget" we explored in class to help identify the correct HTML tags and attributes for your code. However, keep in mind that these tools are far from perfect and sometimes they fail. In such cases, manually navigate the HTML page to find the appropriate tags and attributes.

**What not to scrape:**

  * Do not scrape private data. You can scrape any data that is publicly available. You cannot scrape any data that is password protected or requires a username and passcode to access: if you need to log in to access the data, do not scrape it. Do not scrape social media data, usually they do require a log in.
  
  * Do not scrape websites with dynamic components—specifically, sites that require scrolling to load additional data or interacting with pop-up windows. These types of websites require advanced scraping techniques that are not covered in this course. If you're unsure, feel free to reach out to me and I can check for you.
  
  * Do not scrape data using an API. While APIs are a valuable alternative to direct scraping, for this homework, we want you to focus on direct scraping.

<!--
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
-->

### 2. Clean and wrangle your scraped data

The final outcome of your data collection should be a cleaned and tidy data frame.

Save your scraped data as a `.csv` file(s) and upload that file(s) in your repository. If your `.csv` is 100 MB or larger (this occasionally happens but it is rare), upload a smaller portion of the data.

The extent of data cleaning and wrangling will vary based on your project: 

* Some scraping projects require extensive data manipulation, such as unnesting nested lists or using regular expressions to clean text, while others may require minimal cleaning.
* If your project requires less cleaning (e.g., only a few lines of code), add more complexity to your scraper to balance out. See next point for more. 


### 3. Include data analysis with exploratory descriptions and visualizations

These should show something interesting to you about your data. It is up to you to decide what to display and how; just ensure your graphs/tables are correct and follow what we have learned in this course.

As a guideline, the extent of your data analysis and visualization should correspond to the complexity of obtaining your data (point 1 above) and cleaning/wrangling them (point 2 above). For example: 

 * If you develop a complex and unique scraper (e.g., one that performs beyond basic functions and is not adapted from other sources) and you need to conduct extensive data cleaning and wrangling, your data analysis and visualization efforts can be minimal (e.g., basic descriptive statistics and one or max two well-done graphs).
 
* Conversely, if your scraping task is less extensive — such as adapting an online tutorial (note that "adapting" means modifying and making it your own, as copying code is considered plagiarism), or building upon in-class tutorials — your data analysis and visualization efforts should be more detailed. This might involve performing more in-depth exploratory analysis and creating multiple comprehensive graphs. 

*How do I know if I have "done enough"?* If you are unsure about the scope of your project, don’t hesitate to ask for guidance. Here are a few tips: (1) Use the average time spent on previous assignments as a reference for allocating time to this one; (2) Start early to identify a suitable website to scrape, and change it if it does not work; (3) Ensure your work follows the instructions provided above

If you need additional packages to complete your project, you should be able to install them on your own in Workbench. Let me know if you encounter any issues.


### 4. Your `.Rmd` should read as a tutorial

Your final report should be read as a tutorial, with code and text. Your text should introduce what data and website(s) you choose to scrape, and should explain both the logical steps of scraping (e.g., saving the HTML into an object, collecting elements, etc.) and the results. 


<!--
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
-->
  
### Quote your sources and Plagiarism 

Cite all the sources you consulted and explain in your reflections how you used them. You are welcome to draw inspiration from online tutorials, assigned readings, and other resources, including AI. However, if you rely on online sources, we expect you to cite them (at the end of your `.Rmd`) and explain what you added or modified. The code you produce for the assignment must be primarily original and written by you; it should not closely replicate code found from online sources.

<!-- Note on getting help: We haven't tested or run code for every website out there! We are happy to help you debugging, but ensure you come to us the website you are scraping beforehand. The primary goal of this homework is for you to choose an API or website that interests you and learn how to extract data from it independently! -->


# Submit the assignment

To submit the assignment, follow these steps:

* First push to your repository the last version of your assignment before the deadline. 
    * Your repo should include everything you have used to collect the data and produce your analyses such as R Markdown files, data files, plots, etc. 
    * Submit also the data you collected, unless they are too big: the max file size you can push on GitHub is 100 MB (if your data is too big reach out to the instructor)
    * Your code should be in a `Rmd` file and knitted as `md`. Make sure to stage-commit-push your original `.Rmd` file, knit it as `.md` (e.g., `github_document`) and submit both the `.Rmd` and `.md`

* When you are ready to submit, copy your repository URL (e.g. `https://github.com/css-fall24/hw6-brinasab`) and submit it on Canvas under HW06 before the deadline. Do not submit files on Canvas, we only need the link to your repository 

* As part of your submission, at the end of the `.Rmd` for this homework, include a few reflections on your experience with this assignment, list any help you might have received (from both humans and AI), as specified in the instructions.


# Assessment

All homework assignments are evaluated using a rubric which you can access from the assignment submission folder on Canvas. See also [here](/faq/homework-evaluations/) for more. 

Further guidelines for this specific homework to help you assess your work before submitting it.

In the past, "Excellent" or "Very Good" work included submissions that completed all components of the assignment correctly and accurately. Code ran correctly, followed proper style, and was well-documented without excessive comments. The code and answers demonstrated strong grasp of class materials on web scraping, and demonstrated data analysis and coding skills. Submitted work fully complied with the assignment's instructions and relied on course materials. 
The scraper went beyond the basics and showcased the student's ability to write their own code. For example. the code uses functions, loops, or other key coding concepts where appropriate. Additionally, the repository showed a history of multiple informative commits, reflecting the progression and backup of work. Command of R Markdown syntax was evident, with no errors.


<!-- If an API was used, secure methods were implemented for storing authentication keys or passwords when using an API and/or API wrapper.
