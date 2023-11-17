---
title: "HW07: Generating reproducible social science research"
date: 2023-11-15T13:30:00-06:00  # Schedule page publish date
type: book
toc: true
draft: false
categories: []
weight: 70
---



# Overview

**Due by 11:59 pm on Thursday, November 30th.**

The goal of this final assignment is to practice and further consolidate what we have been learning in this course, by applying these skills and tools to a social science research context. 

# Accessing and cloning the `hw07` repository

* Go [at this link](https://classroom.github.com/a/00oq06oE) to accept and create your private `hw07` repository on GitHub. Once you do so, your repository will be built in a few seconds. It follows the naming convention `hw07-<USERNAME>`  
* Once your repository has been created, click on the link you see, which will take you to your repository. 
* Finally, clone the repository to your Workbench (or your computer if you have installed R there) following the process below.

Notice that the repo you clone for this assignment is almost empty: **you will have to add your data and code** to the repo (and push them to your Github repo).

After you have accessed the `hw07` repository (see above), follow the [same steps you completed for `hw01`](/homework/edit-readme/) to clone the repository.


# Assignment description

The main goal of this assignment is to check your acquisition of the following course learning objectives:

* Gathering data
* Importing and tidying data
* Processing and transforming data
* Exploring and visualizing data (numerical and textual data)
* Interpreting and communicating results
* Basic programming principles (conditional statements, functions, etc.)
* Debugging and defensive programming
* Working with R Markdown documents

I ask you to show these skills by applying them to research **that interests you**. Therefore, in this assignment, develop a research question of your interest, answer it with data, and write a report (in `Rmd`) that includes your code and your interpretation of the data. 


### Guidelines for your report

Frame your report as you would if you were submitting it for a substantive seminar in your research field, or imagine preparing it for a company. It should be approximately 700-750 words in length. It is okay if the report is more extended (up to 1000 words), but it should not be shorter than 700 words. Write your report as `Rmd` and knit and push it on Github as `md` (i.e., `github_document`)

Specifically your report should include the following:
* A research question, or set of questions, of social science relevance 
* A description of your project, that is, a narrative that provides some context for us to be able to understand what you are working on and why it is important
* A description of the data for the reader (the data themselves should placed in your repo -- see below for details) and how you obtained them, including all relevant links and info
* Some descriptive statistics (tables!), some plots of the data, and your interpretation of them:
  * It is hard to provide you with an exact number of graphs (because that depends on the overall complexity of the project), but, as a reference, we expect that you generate several exploratory charts and include only the most relevant (4 or 5 well-designed plots); please, review the lecture on EDA on the different purpose of graphs
  * You are not expected and do not need to (unless you want to!) include complex statistical modeling that we have not learned in the course. The actual analysis can be relatively simple: think about the graphs you generated for HW2 and HW3
  * You do not have to, but you are welcome to work with textual data and produce analyses such as word frequencies, correlations, tm, sentiment analysis, etc.
  * We care about your explanation and interpretation: please explain each graph you decide to include in your report, and why it is important; conjecture as to why a given relationship between two variables occurs and/or why they may be [spurious](https://en.wikipedia.org/wiki/Spurious_relationship), and further hypotheses to evaluate

### Guidelines for your code

In terms of code, your submission should contain the following:
* Code to load the required libraries and import the data. This code must be at the top of the document only (do not import libraries or load data in other parts of the script). If you are scraping data, put your scraper in another script (see last point)
* Code to clean the data (e.g., rename variables, recode variables, etc.) as necessary and/or code to tidy the data as necessary; this will vary from project to project
* Code to generate descriptive statistics (tables, summaries, etc.) and plots (roughly 4-5 well-designed plots, I expect more if your data require only minimal data cleaning/tidying)
* Your code should incorporate programming techniques such as loops (or R alternatives to loops), if-else statements, and user-defined functions
* Your code should take into account all topics we learned in the course, including coding style, reproducible workflow, and use of Rmd documents (I expect you to consult the slides and the assigned readings)
* Include relevant output, but omit lengthy, irrelevant, and hard-to-read output (e.g., include the head of the data set but do not include the full print of it, suppress irrelevant messages, etc.)
* Use code chunk and YAML options to customize your final document
* You can, but do not need to stuff everything into the final report. Think of this like a traditional report. You might describe how you obtained and prepared the data, but you won't include all the code and output from that process in the final document. For example: if you write several lines of code for data cleaning and tidying, you can write that code in a separate `Rmd` or script, and load only the cleaned data into the final `Rmd`; or, if you create multiple plots, write the code in a R script, and select only a few plots for the report, etc. As long as all your code is stored in the repo, you ensure reproducibility. We will access and grade everything that is in the repo: refer to the extra code in the README so we know where to search for it.

### Your repository should include a `README.md` 

Your README should include the following:
* Explains the purpose of the repository
* Lists all scripts contained in the repo and explains how to execute them to produce the same results as you (if you only have the main `Rmd` document for the report, that's fine but list it)
* Lists any additional packages a user should be expected to install prior to executing the files (you don't need to specify basic packages like `dplyr`, `tidyverse`, `rmarkdown`, etc.)
* Provides any other relevant information that the user needs to know in order to use your repo and replicate your results 
* Provide 1-2 paragraphs of reflections on what was hard/easy about this homework, what was enjoyable, problems you solved and how you solved them, helpful resources, etc.


# Other useful information

### What data should I use?

Whatever you want! The important thing is that your assignment shows the skills you learned so far in the class, and it is useful for YOU. You can, but you do not necessarily have to answer something directly related to your own research: feel free to explore something for fun or something that will give you a chance to consolidate and expand what you have learned so far. 

### How do I know if I have "done enough"?

* Make sure you have followed the instructions (e.g., make sure that all requirements for the code, report, and README are met)
* It is difficult for us to provide a precise estimate of the time you should spend on this assignment (too many variables to consider), but you can take as a reference the average time you spent on each assignment so far. The time spent on this homework should be at least equal to that average time
* As you complete the assignment, aim to review what you have learned in the course and try to push a bit outside your comfort zone. If in doubt, I can help you assess if your plan is appropriate
* **Please notice**: The goal of this homework is to show and strengthen what you have learned so far in the course. We expect you to complete it alone (you can rely on classmates for advice, but the homework itself needs to be completed alone). We expect you to submit your own original code (code you write), adopt coding strategies that make sense to you, and code that you fully understand and can debug on your own

### I can't think of anything to analyze!

You can analyze one of the datasets we have used in the class, as long as they contain social science data (e.g., cars, diamonds, flowers, or other teaching-related datasets won't be appropriate) and as long as we have not used them for past homework assignments. For example, you could use:

* `gapminder` in `library(gapminder)`
* `gun_deaths`
    * In `library(rcis)`
    * [Raw data for `gun_deaths` from FiveThirtyEight](https://github.com/fivethirtyeight/guns-data)
* `scorecard`
    * In `library(rcis)`
    * Use the [`rscorecard`](https://github.com/btskinner/rscorecard) library to download your own subset of the Department of Education's College Scorecard data
* Check out [this archive of datasets](https://docs.google.com/spreadsheets/d/1wZhPLMCHKJvwOkP4juclhjFgqIY8fQFMemwKL2c64vk/edit#gid=0) from the Data Is Plural Newsletter
* Check out #TidyTuesday, a weekly data analysis challenge for individuals to practice and develop their data analysis skills in R. They publish [a complete archive of all of their past challenges and source data](https://github.com/rfordatascience/tidytuesday).


### How can I download the data?

There are functions in R and programs for the [shell](/setup/shell/) that allow you to do automatically download data. If you are using one of the data sets already provided to you in `library(rcis)`, you do not need to download them again. But you can. For example, to download `gapminder` from the [original GitHub repo](https://github.com/jennybc/gapminder), there are three options:

+ Option 1: via an R script using [downloader::download](https://cran.r-project.org/web/packages/downloader/downloader.pdf) or [RCurl::getURL](http://www.omegahat.net/RCurl/installed/RCurl/html/getURL.html).

    ```r
    downloader::download("https://raw.githubusercontent.com/fivethirtyeight/guns-data/master/full_data.csv", "gun_deaths.csv")
    cat(file = "gun_deaths.csv",
    RCurl::getURL("https://raw.githubusercontent.com/fivethirtyeight/guns-data/master/full_data.csv"))
    ```

+ Option 2: in a [shell](/setup/shell/) script using `curl` or `wget`.

    ```bash
    curl -O https://raw.githubusercontent.com/fivethirtyeight/guns-data/master/full_data.csv
    wget https://raw.githubusercontent.com/fivethirtyeight/guns-data/master/full_data.csv
    ```

+ Option 3: manually download and save a copy of the data file(s) in your repo. Make sure to commit and push them to GitHub.


### What if my data file is large?

Because of how Git tracks changes in files, GitHub will not allow you to commit and push a file larger than 100mb. If you try to do so, you will get an error message and the commit will not push. Worse yet, you now have to find a way to strip all trace of the data file from the Git repo (including previous commits) before you can sync up your fork. This is a pain. Avoid it as much as possible. 

If you follow options 1 and 2 above, then you do not need to store the data file in the repo because it is automatically downloaded by your script/Rmd document.

If you have to store a large data file in your repo, use [**Git Large File Storage**](https://git-lfs.github.com/). It is a separate program you need to install via the shell, but the instructions are straight-forward. It integrates smoothly into GitHub, and makes version tracking of large files far easier. If you include it in a course-related repo (i.e. a fork of the homework repos), then there is no cost. If you want to use Git LFS for your own work, [there are separate fees charged by GitHub for storage and bandwidth usage.](https://help.github.com/articles/about-storage-and-bandwidth-usage/)


<!--
   * To emulate RStudio's "render" button from a [shell](/setup/shell/):
        `Rscript -e "quarto::quarto_render('input = myAwesomeAnalysis.qmd')"`
    * To emulate RStudio's "Knit" button within an R script:
        `quarto::quarto_render('input = myAwesomeAnalysis.qmd')`
-->


# Submit the assignment

Your repo should include everything you have used to collect the data and produce your analyses (R Markdown files, R scripts, graphs, data files, etc.). Submit also the data you collected.

Your code should be put in a `Rmd` file and knitted as `md`. Make sure to stage-commit-push your original `.Rmd` file, knit it as `.md` (e.g., `github_document`) and submit both the `.Rmd` and `.md`

When you are ready to submit, copy your repository URL (e.g. https://github.com/css-fall23/hw7-brinasab) and submit it on Canvas under HW07 before the deadline. Do not submit files on Canvas, we only need the link to your repository 

As part of your submission:
  * write 1-2 paragraphs of reflections about the homework
  * list the first and last name of eventual collaborators with whom you worked with to complete this assignment
  * list all the resources you consulted
  

# Assessment

All homework assignments are evaluated using [this general rubric](/faq/homework-evaluations/). Make sure to check it. 

Below are further guidelines for this specific homework to help you assess your work before submitting it.

*Needs improvement:* Scripts require interactive coding to fix. Markdown documents are not generated and/or `README.md` is insufficient or absent. Minimal code. Graphs and tables are too basic and/or don't have appropriate labels or formatting. There is no consistency to code's style. Research question not answered. No clear evidence that show the students understanding of R programming skills and course's topic.

*Good:* Solid effort. Hits all the elements. Finished all components of the assignment with only minor deficiencies. Easy to follow (both the code and the output). 

*Excellent:* Repository contains a detailed `README.md` explaining how the files in the repo should be executed. Displays solid understanding of course materials including data analysis or coding skills. Code is complex and efficient. Graphs and tables are well labeled. Excellent implementation of a consistent style guide. Analysis and write up are detailed and insightful.

