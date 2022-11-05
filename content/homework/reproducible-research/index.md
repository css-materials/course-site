---
title: "HW06: Generating reproducible research"
date: 2022-11-04T13:30:00-06:00  # Schedule page publish date
publishdate: 2019-04-01

draft: true
aliases: ["/hw05-reproducible-research.html"]

summary: "Synthesize everything we have learned thus far."
---



# Overview

**Due by 11:59 pm on Friday, November 11th.**

The goal of this assignment is to practice and further consolidate what we have been learning so far, by applying these tools to a social science research context.


# Accessing the `hw06` repository

* Go [at this link](ADD LINK) to accept and create your private `hw5` repository on GitHub. Once you do so, your repository will be built in a few seconds. It follows the naming convention `hw5-<USERNAME>`  
* Once the your repository has been created, click on the link you see, which will take you to your repository. 
* Finally, clone the repository to your computer (or R workbench) following the process below.

Notice the repo you clone for this assignment is empty: **you will have to fill it with your data and code (in R Markdown document), and push your data and code to your github repo**.


# Cloning your `hw06` repository

After you have accessed the `hw6` repository (see above), follow the [same steps you completed for `hw1`](/homework/edit-readme/) to clone the repository.


# General workflow

Your general workflow will be:

* Accept the repo and clone it (see above)
* Make changes locally to the files in RStudio
* Save your changes
* Stage-Commit-Push: stage and commit your changes to your local Git repo; then push them online to GitHub. You can complete these steps using the Git GUI integrated into RStudio. In general, you do not want to directly modify your online GitHub repo (if you do so, remember to pull first); instead modify your local Git repo, then stage-commit-push your changes up to your online GitHub repo. 


# Assignment description

At this mid-way point in the term, I want to check and make sure everyone is up to speed on the major skills learned so far:

* Importing and tidying data
* Transforming, visualizing, and exploring data
* Interpreting and communicating results
* Basic programming principles (conditional statements, functions, data structures)
* Debugging and defensive programming
* Reproducible Workflow
* Generating R Markdown documents

I ask you to demonstrate the value of these skills for research **that interests you**. Therefore in this assignment, I want you to write a short report on a research question of your own interest. 

State your research question (or questions) clearly and frame your report as you would if you were submitting it for a substantive seminar in your research field, though much shorter and comprehensive then a term paper. It should be approximately 750-1000 words in length and showcase the major skills identified above. It does not need to be an advanced statistical analysis involving complex statistical modeling and skills we have not learned. The actual analysis can be relative simple - think exploratory. Analyzing the distribution of variables and how they are related to one another at a bivariate level is more than adequate.

Your code should do the following:

* Import the data
* Tidy it as necessary to get it into a tidy data structure
* Generate some descriptive statistics and plots of the data
* Summarize the relationships you discover with a written summary. Conjecture as to why they occur and/or why they may be [spurious](https://en.wikipedia.org/wiki/Spurious_relationship).

Your code should contain the following:
* ...
* 


The final output should be a `md` or alternatively a `pdf_document`, but it must be something you can view directly on GitHub - no `html_document`s).


# What data should I use?

Whatever you want! The important thing is that the entire analysis is **reproducible**. That is, we will clone your repository on our computers and attempt to reproduce your results. This means you should provide an informative `README.md` file that:

* Explains the purpose of the repository
* Identifies how to execute the script(s) to produce the same results as you
* Lists any additional packages a user should be expected to install prior to executing the files (you don't need to specify basic packages like `dplyr`, `tidyverse`, `rmarkdown`, etc.)


### I can't think of anything to analyze!

Okay, then analyze one of the datasets we have used before.

* `gapminder` in `library(gapminder)`
* `gun_deaths`
    * In `library(rcis)`
    * [Raw data for `gun_deaths` from FiveThirtyEight](https://github.com/fivethirtyeight/guns-data)
* `scorecard`
    * In `library(rcis)`
    * Use the [`rscorecard`](https://github.com/btskinner/rscorecard) library to download your own subset of the Department of Education's College Scorecard data
* Check out [this archive of datasets](https://docs.google.com/spreadsheets/d/1wZhPLMCHKJvwOkP4juclhjFgqIY8fQFMemwKL2c64vk/edit#gid=0) from the Data Is Plural Newsletter
* Likewise, #TidyTuesday is a weekly data analysis challenge for individuals to practice and develop their data analysis skills in R. They post a new challenge every Tuesday, and publish [a complete archive of all of their past challenges and source data](https://github.com/rfordatascience/tidytuesday).


### How can I automatically download the data

There are functions in R and programs for the [shell](/setup/shell/) that allow you to do this. For example, if I wanted to download `gapminder` from the [original GitHub repo](https://github.com/jennybc/gapminder):

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

+ Option 3: manually download and save a copy of the data file(s) in your repo. **Make sure to commit and push them to GitHub**.


### What if my data file is large?

Because of how Git tracks changes in files, GitHub will not allow you to commit and push a file larger than 100mb. If you try to do so, you will get an error message and the commit will not push. Worse yet, you know have to find a way to strip all trace of the data file from the Git repo (including previous commits) before you can sync up your fork. This is a pain in the ass. Avoid it as much as possible. If you follow option 1 and 2, then you do not need to store the data file in the repo because it is automatically downloaded by your script/Quarto document.

If you have to store a large data file in your repo, use [**Git Large File Storage**](https://git-lfs.github.com/). It is a separate program you need to install via the shell, but the instructions are straight-forward. It integrates smoothly into GitHub, and makes version tracking of large files far easier. If you include it in a course-related repo (i.e. a fork of the homework repos), then there is no cost. If you want to use Git LFS for your own work, [there are separate fees charged by GitHub for storage and bandwidth usage.](https://help.github.com/articles/about-storage-and-bandwidth-usage/)


# Aim higher!

* Use a completely unique dataset - preferably something related to your own research interests
    * You will probably need to spend time data cleaning and tidying. Could be done in the main Rmd document or in a separate R script. If done in the Rmd document, consider whether it is necessary to include the code and output in the final document.
* Render an R Markdown document with your final analysis.
    * You do not need to stuff everything into the final document. Think of this like a traditional report. You might describe how you obtained and prepared the data, but you won't include all the code and output from that process in the final document. But because it is stored in a separate R script and is part of the repo, everything is still completely reproducible.
    * To emulate RStudio's "render" button from a [shell](/setup/shell/):
        `Rscript -e "quarto::quarto_render('input = myAwesomeAnalysis.qmd')"`
    * To emulate RStudio's "Knit" button within an R script:
        `quarto::quarto_render('input = myAwesomeAnalysis.qmd')`
* Make use of code chunk and YAML options to customize the appearance of your final document
* Use your skills on [project management](/notes/saving-source/) to ensure reproducibility
* Writing your own functions? Implement [defensive](/notes/style-guide/) [programming](/notes/condition-handling/) to minimize errors (or at least provide informative error messages).
* Use a consistent style when writing your code


# Submit the assignment

Your repo should be include everything you have used to produce your analyses (R scripts, R Markdown documents, data files, figures, etc.)

Make sure to stage-commit-push your original `.Rmd` file (or files if you used more than one), and the report you generate from it (as a `md` or a `pdf`).

To submit the assignment, simply push to your repository the last version of your assignment before the deadline. Then copy your repository URL (e.g., `https://github.com/css-fall22/hw5-brinasab`) and submit it to Canvas under HW05 before the deadline.



# Rubric

Needs improvement: Cannot reproduce your results. Scripts require interactive coding to fix. Markdown documents are not generated. Graphs and tables are unclear and/or don't have appropriate labels or formatting. There is no consistency to your code's style.

Satisfactory: Solid effort. Hits all the elements. Finished all components of the assignment with only minor deficiencies. Easy to follow (both the code and the output). 

Excellent: Finished all assignment components correctly and used efficient code to complete the exercises. The solutions adopted went beyond what strictly required. The code is well-documented (both self-documented and with additional comments as necessary). The function is written succinctly/comprehensibly and used correctly. Use multiple commits to back up and show a progression in work.


Excellent: Repository contains a detailed `README.md` explaining how the files in the repo should be executed. Displays innovative data analysis or coding skills. Graphs and tables are well labeled. Excellent implementation of a consistent style guide. Analysis is insightful. I walk away feeling I learned something.

## Acknowledgments


* This page is derived in part from ["UBC STAT 545A and 547M"](http://stat545.com), licensed under the [CC BY-NC 3.0 Creative Commons License](https://creativecommons.org/licenses/by-nc/3.0/).


* This page has been developed starting from Benjamin Soltoff’s “Computing for the Social Sciences” course materials, licensed under the CC BY-NC 4.0 Creative Commons License.
