---
title: "HW07: Final Project"
date: 2024-11-20T13:30:00-06:00  # Schedule page publish date
type: book
toc: true
draft: false
categories: []
weight: 70
---



**Due ~~Thursday, December 5th (11:59 PM)~~ Friday, December 6th (11:59 PM)**

*The deadline has been extended, allowing some extra time to incorporate our feedback from [Lecture 18](https://computing-soc-sci.netlify.app/syllabus/lecture-18/), if you wish to do so.*


# Accessing and Cloning the `hw07` Repository

* Go [at this link](https://classroom.github.com/a/2kbDfJcT) to accept the invitation and create your private `hw07` repository on GitHub. Once you do so, your repo will be built in a few seconds. It follows the naming convention `hw07-<USERNAME>`
* Once your repository has been created, click on the provided link to access it. 
* Finally, follow the [same steps you completed for `hw01`](/homework/edit-readme/) to clone the repository to your R Workbench. Refer to the same link also for the general workflow of using Git/GitHub. 

Like for HW6, the repo you clone for this assignment is almost empty: **you will need to add your scraped data and your code** to the Git repo, and push them to your Github online repo. See below for details on what to submit (remember to submit the knitted `md` along with other files!)


# Assignment Description

In this course, you have acquired a range of skills, ranging from working with Git/GitHub and creating R Markdown documents, to processing and visualizing data (check the homepage for the course learning objectives).

This final assignment serves as the final project for the course and provides an opportunity to showcase and further practice your R skills by applying them to a research topic that interests you!

**Goal:** For this assignment, formulate one or more questions that interest you and answer them using code and data. Your main deliverable should be a report that includes the code used for the analysis, graphs and tables presenting your findings, and your interpretation of the results.

The following sections provide further instructions for each part of the assignment to help you complete it successfully...


### Report Instructions

**Report Format:** Your report should be an `Rmd` file (knitted as `md` and also as `pdf` or `world`) and must include written text, code, and outputs from the code (such as graphs, tables, and descriptive statistics). If you prefer not to include all of your code in the report, you can place the additional code in a separate file, such as a simple R script or another `Rmd` document. In this case, please include a note in your `README.md` to inform us that additional code is available in the repository and specify its location.

**Report Framing and Length:** Frame your report as if you were submitting it for a seminar in your field or preparing it for the clients of a company you work for. The written sessions of your report should explain your project, including its purpose and questions, and should interpret your graphs and code output. These should be approximately 700-750 words in length (this total includes the project explanation, interpretation of output, graphs, and tables). While the report can be longer (up to 1000 words), it should not be shorter than 700 words.

**Specifically, your report should include the following elements** (use R Markdown syntax like titles, subtitles, bold, etc. to ensure we can identify them in your report; add a table of content):

* **Research Question(s):** state your question(s), ideally they should have social science relevance

* **Project Description:** provide a narrative that explains what you are working on and why

* **Data Description:** describe the data (total observations, time period, variables, etc.), including how you obtained it and any relevant links and information. Place the data in your repository. If the data is larger than 100 MB, refer to the instructions below to avoid issues with GitHub.

* **Descriptive Statistics and Plots:** include tables using `kable()`, plots, and your interpretation of them:
  * While the exact number of graphs depends on your project, we expect that you generate several exploratory charts (recall our EDA lecture) and include in your report only 4 or 5 well designed plots with title, labels, scales, etc.
  * The plots should be of different types (do not repeat the same type of plot multiple times, e.g. line chart, histogram, etc.) and each plot should match the variable type
  * You are not expected or required to include statistical modeling beyond what we have covered in the course (unless you want to do so). Excellent projects can be based on simple analyses, such as descriptive statistics or the graphs you created for HW2 and HW3. If you decide to incorporate statistical models (e.g., regression, ANOVA, etc.), be sure to apply them correctly. For example, if you run a linear regression, check the data distribution, interpret the coefficients, and ensure your dependent variable is continuous. If you have questions, feel free to reach out!
  * We want to hear your explanation and interpretation of the analyses: describe each graph, hypothesize about the relationships between variables, discuss any limitations, suggest potential hypotheses or directions for future research, etc.

<!-- 
You do not have to, but you are welcome to work with textual data and produce analyses such as word frequencies, correlations, tm, sentiment analysis, etc.
-->

### Code Instructions

This is class with a strong coding component, so the quality of your code is an important part of the project.

* **Library Loading and Data Import:** Include code to load the required libraries and import the data at the top of the document only. Avoid loading libraries or importing data in other parts of the script. If you are scraping data, place your scraper in a separate script (see the last point on Code Organization).

* **Data Cleaning, Wrangling and Tidying:** Provide code to clean the data (e.g., renaming variables, recoding variables, aggregating variables, etc.) and/or tidy the data as necessary. The amount of this code will vary from project to project.

* **Data Analysis and Plots:** Include code to generate descriptive statistics (tables, summaries) and plots (roughly 4-5 well-designed; we expect more sophisticated graphs if your data requires minimal cleaning and tidying). Plots must vary: do not repeat the same type of plot multiple times, see above for details about the plots.

* **Programming Techniques:** Your code must incorporate programming techniques such as for loops (or R alternatives to for loops), conditional statements, and user-defined functions. We expect at least one of each, but if this doesn’t seem feasible for your project, please consult with us. We can discuss the best approach for your project (e.g., there might be no use of conditional statements in your project, but there might be room to write multiple user-defined functions, etc.).

* **Code Organization:** 
  *  Include relevant output, but omit lengthy, irrelevant, and hard-to-read results (e.g., print the head of the dataset, but not the entire dataset).
  * Ensure your code reflects the topics we have covered in the course, including coding style, reproducible workflow, and the use of Markdown syntax. Customize your final document using Markdown options, see the last lecture on this. When similar functions exist both in base R and the tiydverse, give priority to what we learned in class (e.g. use `read_csv()` rather than `read.csv()`)
  * You can, but don't need to include all code and output in the final report. Think of it like a traditional report. For instance, if you write extensive data cleaning and tidying code, write that code in a separate `Rmd` or R script, and load only the cleaned data into the final `Rmd`; or, if you create multiple plots, select a few for the report, and store the rest of the code separately. As long as all your code is stored in the repo, you ensure reproducibility and we will access and grade everything in the repo. Refer to the extra code in the `README.md` to make us aware of its presence.


### Repository and `README.md` Instructions

Your repository must include a `README.md` with the following information:

* **Purpose of the Repository:** Write a few sentences explaining the purpose of the repository. For example, "This repo includes the data (include sample size and data source) and code for a project that investigates x and y."

* **List of Scripts:** Provide a list of all the R scripts and `.Rmd` files contained in the repository with a one-sentence description of each. Format the list as an actual list.

* **Required Packages:** List any additional packages a user needs to install before executing the files. There is no need to specify basic packages like  `tidyverse` or `rmarkdown`.

* **Additional Information:** Include any other relevant information the user needs to know to use your repository and replicate your results.

<!-- add example README here -->

# FAQs

### How do I know if I have "done enough"?

* Make sure you have followed the instructions (e.g., ensure the requirements for the report, code, and `README.md` are met).
* While it is difficult to provide a precise estimate of the time needed for this assignment (people, interests, and working habits vary!), you can use the average time you spent on each previous assignment as a reference: this final homework should take at least as long as the average time you spent on other assignments for this course. Another element to consider is that this final assignment is worth 20 points, while previous assignments are worth 15 points.
* As you complete the assignment, aim to review what you have learned in the course and try to push a bit beyond your comfort zone. If you have any doubts, check in with us: we can help you assess if your plan meets the minimum requirements.
* The goal of this homework is to demonstrate and reinforce what you have learned throughout the course. You are expected to complete it independently (you may seek advice from classmates or resources, but the work itself must be your own). We expect you to submit original code that you have written independently and you can fully understand and debug on your own. Our AI policy applies to this assignment as well.


### What data should I use?

While we encourage you to find data related to the social sciences, we may allow other types of data -- just check with us to ensure it’s a good fit. The most important thing is that your assignment demonstrates the skills you have learned in class and is useful to you. 


### I can't think of anything to analyze!

You can analyze one of the datasets we have used in the class, as long as we have not used them for past homework assignments and as long as it is not teaching-related data (e.g., penguins, cars, flowers, won't be appropriate).

For example, you could use:

* `gapminder` in `library(gapminder)`
* `gun_deaths` in `library(rcis)` or the raw data is available in  [FiveThirtyEight](https://github.com/fivethirtyeight/guns-data)
* `scorecard` in `library(rcis)` or use the [`rscorecard library`](https://github.com/btskinner/rscorecard) to download your own subset of the Department of Education's College Scorecard data
* Check out [this archive of datasets](https://docs.google.com/spreadsheets/d/1wZhPLMCHKJvwOkP4juclhjFgqIY8fQFMemwKL2c64vk/edit#gid=0) from the Data Is Plural Newsletter
* Check out #TidyTuesday, a weekly data analysis challenge for individuals to practice and develop their data analysis skills in R. They publish [a complete archive of all of their past challenges and source data](https://github.com/rfordatascience/tidytuesday).


### How can I download the data?

There are functions in R and shell programs (see Syllabus & FAQ) that allow you to do automatically download data. If you are using one of the data sets provided in `library(rcis)`, you do not need to download them again, though you can if you prefer. For example, to download `gapminder` from the [original GitHub repo](https://github.com/jennybc/gapminder), there are three options:

+ Option 1: via an R script using [downloader::download](https://cran.r-project.org/web/packages/downloader/downloader.pdf) or [RCurl::getURL](http://www.omegahat.net/RCurl/installed/RCurl/html/getURL.html).

    ```r
    downloader::download("https://raw.githubusercontent.com/fivethirtyeight/guns-data/master/full_data.csv", "gun_deaths.csv")
    cat(file = "gun_deaths.csv",
    RCurl::getURL("https://raw.githubusercontent.com/fivethirtyeight/guns-data/master/full_data.csv"))
    ```

+ Option 2: in a shell script using `curl` or `wget`.

    ```bash
    curl -O https://raw.githubusercontent.com/fivethirtyeight/guns-data/master/full_data.csv
    wget https://raw.githubusercontent.com/fivethirtyeight/guns-data/master/full_data.csv
    ```

+ Option 3: manually download and save a copy of the data file(s) in your repo. Make sure to commit and push them to GitHub.


### What if my data file is too large?

Due to the way Git tracks changes in files, GitHub will not allow you to commit and push a file larger than 100MB. If you try to do so, you will receive an error message, and the commit will not push. Worse yet, you will have to find a way to strip all traces of the data file from the Git repository (including previous commits) before you can sync up your fork. This is a pain, so it's best to avoid it as much as possible.
 
If your data is considerably smaller than 100 MB, push it to your repo. If it is larger or about 100 MB: do not push the data to your repo. Instead store the data outside GitHub (e.g., Google Drive, etc.) and add a link to the data in the `README.md`. 

<!-- If you want store a large data file in your repo, use [**Git Large File Storage**](https://git-lfs.github.com/). It is a separate program you need to install via the shell, but the instructions are straightforward. It integrates smoothly into GitHub, and makes version tracking of large files much easier. If you want to use Git LFS for your own work, there are separate fees charged by GitHub for storage and bandwidth usage.
-->
<!--
   * To emulate RStudio's "render" button from a [shell](/setup/shell/):
        `Rscript -e "quarto::quarto_render('input = myAwesomeAnalysis.qmd')"`
    * To emulate RStudio's "Knit" button within an R script:
        `quarto::quarto_render('input = myAwesomeAnalysis.qmd')`
-->


# Quote your Sources and Plagiarism Policy

Cite all the sources you consulted and explain in your reflections how you used them. You are welcome to draw inspiration from online tutorials, assigned readings, and other resources, including AI. 

However, if you rely on online sources, we expect you to cite them (at the end of your `.Rmd`) and explain what you added or modified. The code you produce for the assignment must be primarily original and written by you; it should not closely replicate code found from online sources.


# Submit the Assignment

* First push to your repository the last version of your assignment before the deadline. Make sure to stage-commit-push:

  - everything you have done to collect the data and produce your analyses, e.g., R Markdown files or R scripts, graphs, data (unless they are too large, see above for details)
  - your report should integrate code and written text and should be generated using a `Rmd` file. Knit this file in two ways: as `md`, and as `pdf` or `world`. Submit the original `Rmd`, the `md`, and the `pdf` or `world`

* When you are ready to submit, copy your repository URL (e.g. `https://github.com/css-fall24/hw7-brinasab`) and submit it on Canvas under HW07 before the deadline. Do not submit files on Canvas, we only need the link to your repository 

* As part of your submission, at the end of the `.Rmd`, include a few reflections on your experience with this assignment, and list any help you might have received (from both humans and AI).


# Assessment

All homework assignments are evaluated using a rubric which you can access from the assignment submission folder on Canvas. It is the same rubric as in previous HWs, but the points distribution is different since this homework is worth 20 points. See also [here](/faq/homework-evaluations/) for more. 

Further guidelines for this specific homework to help you assess your work before submitting it.

In the past, "Excellent" or "Very Good" work included submissions that completed all components of the assignment correctly and accurately.
Submitted work fully complied with the assignment's instructions and relied on course materials, demonstrating a solid understanding of them.
Code ran correctly, followed proper style,  was of adequate complexity, and was well-documented without excessive comments. Tables and graphs were clear and well-formatted, removing irrelevant data, and aggregating data appropriately. Graphs were well-crafted and diverse, each appropriately matching the variable type. High-quality submissions included detailed and insightful analyses and write-ups. Additionally, the repository featured an informative `README.md` and demonstrated a history of multiple meaningful commits, reflecting the progression and backup of work. Proficiency with R Markdown syntax beyond the basics was evident, with no errors.
