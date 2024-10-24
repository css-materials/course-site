---
title: "HW07: Final Project"
date: 2024-06-27T13:30:00-06:00  # Schedule page publish date
type: book
toc: true
draft: true
categories: []
weight: 70
---



**Due ~~Sunday, July 14th (11:59 PM)~~ Friday, July 19th (11:59 PM)**

This final assignment provides an opportunity further consolidate the skills and tools acquired throughout this course by applying them to a research context that interest you.


# Accessing and cloning the `hw07` repository

* Go [at this link](https://classroom.github.com/a/dmneOOq6) to accept the invitation and create your private `hw07` repository on GitHub. Once you do so, your repo will be built in a few seconds. It follows the naming convention `hw07-<USERNAME>`
* Once your repository has been created, click on the provided link to access it. 
* Finally, follow the [same steps you completed for `hw01`](/homework/edit-readme/) to clone the repository to your R Workbench. Refer to the same link also for the general workflow of using Git/GitHub. 

Notice that, unlike previous assignments, the repo you clone for this assignment is almost empty: **you will have to add your data and code** to your local Git repo, and then push them to your online Github repo.


# Assignment description

In this course, you have developed a range of skills, ranging from working with Git/GitHub and creating R Markdown documents to processing and visualizing data (see the homepage for the course learning objectives). This final homework provides you with an opportunity to showcase and further practice these skills by applying them to a research topic that interests you!

**GOAL:** For this assignment, formulate a research question that interests you and answer it using code and data. Your final product should be a report that includes the code used for the analysis, graphs and tables displaying your findings, and your interpretation of the them. 

The following sections provide detailed guidelines to help you complete the assignment successfully... *keep reading to learn more!*


### Guidelines for your report

Your report should be an `Rmd` file and must include written text, code, and outputs from the code (such as graphs, tables, and descriptive statistics). If you prefer not to include all of your code in the report, you can place the extra code in a separate file, either as an R script or another `Rmd` document.

Frame your report as if you were submitting it for a substantive seminar in your research field or preparing it for a company. The written parts of your report should explain your project, including its purpose and research questions, and should be approximately 700-750 words in length (this total includes your project explanation, interpretation of findings and explanations of graphs and tables). While it is acceptable for the report to be longer (up to 1000 words), it should not be shorter than 700 words. 
 
Specifically, your report should include the following elements. They should be *easily identifiable*, i.e., come up with titles and subtitles, and use Rmd syntax to render them as such:

<!-- * A title and table of content (add the latter using Rmd syntax) -->

* Research Question(s): state your research question(s), ideally it should have social science relevance

* Project Description: provide a narrative that offers context and explains what you are working on and why

* Data Description: describe the data (total observations, time period, variables, etc.), including how you obtained it and any relevant links and information. Place the data in your repository (if the data is too large, refer to the instructions below to avoid issues)

* Descriptive Statistics and Data Plots: include tables (use `kable()`), plots, and your interpretation of the data:
  * While the exact number of graphs depends on your project, we expect that you generate several exploratory charts and include in your report only 4 or 5 well designed plots; these should be of different types
  * You are not expected nor required to include statistical modeling (unless you want to) beyond what we have learned in the course. Excellent projects can have simple analyses: think about descriptive statistics, Exploratory Data Analysis (EDA), and the graphs you generated for HW2 and HW3. 
  * We want to hear your explanation and interpretation of the analyses: explain the significance of each graph, hypothesize about relationships between variables, discuss potential spurious relationships, and propose further hypotheses or research directions

<!-- ADD THIS AS FOOTNOTE NEXT TIME: Please note, if you decide to include statistical models that we have not covered in the course (e.g., linear regression, logistic regression, ML models, etc.) make sure to do it accurately. It is best not to include these models than including them poorly (example: a linear regression model that does not check the distribution of the data, residuals, outlines, etc.); if in doubt, please ask, we are happy to provide advice!

You do not have to, but you are welcome to work with textual data and produce analyses such as word frequencies, correlations, tm, sentiment analysis, etc.
-->

### Guidelines for your code

This is class with a strong coding component, so the quality of your code is an important part of the project.

* Library Loading and Data Import: Include code to load the required libraries and import the data at the top of the document only. Avoid loading libraries or importing data in other parts of the script. If you are scraping data, place your scraper in a separate script (see the last point).

* Data Cleaning and Tidying: Provide code to clean the data (e.g., renaming variables, recoding variables) and/or tidy the data as necessary. The amount of this code will vary from project to project.

* Descriptive Statistics and Plots: Include code to generate descriptive statistics (tables, summaries) and plots (roughly 4-5 well-designed, more if your data requires minimal cleaning/tidying; see above for details about the plots).

* Programming Techniques: Incorporate programming techniques such as loops (or R alternatives), conditional statements, and user-defined functions. Aim to include at least one of each, but consult with me if you struggle with this part, as feasibility can vary by project: we can discuss how to adapt these techniques for your project!

* Code Organization: 
  *  Include relevant output but omit lengthy, irrelevant, and hard-to-read output (e.g., include the head of the data but not the full print, use RMarkdown options to suppress irrelevant messages, etc.).
  * Ensure your code reflects the topics we have covered in the course, including coding style, reproducible workflow, and the use of Markdown syntax (customize your final document using Markdown options, see the last lecture on this).
  * You can, but don't need to include all code and output in the final report. Think of it like a traditional report. For instance, if  you write extensive data cleaning and tidying code, write that code in a separate `Rmd` or R script, and load only the cleaned data into the final `Rmd`; or, if you create multiple plots, select a few for the report, and store the rest of the code separately. As long as all your code is stored in the repo, you ensure reproducibility and we will access and grade everything in the repo (refer to the extra code in the `README.md` to make us aware of its presence).


### Guidelines for your repository and `README.md`

Your repository must include a `README.md` with the following information:

* Purpose of the Repository: Write a few sentences explaining the purpose of the repository. For example, "This repo includes the data (with sample size and data source) and code for a project that investigates x and y."

* List of Scripts: Provide a list of all the R scripts and `.Rmd` files contained in the repository with a one-sentence description of each

* Required Packages: List any additional packages a user needs to install before executing the files. There is no need to specify basic packages like dplyr, tidyverse, rmarkdown, etc.

* Additional Information: Include any other relevant information the user needs to know to use your repository and replicate your results.

<!-- add example README here -->

# FAQs

### How do I know if I have "done enough"?

* Make sure you have followed the instructions (e.g., make sure that the requirements for the report, code, and `README.md` are met).
* While it is difficult to provide a precise estimate of the time needed for this assignment (people and interests vary!), you can use the average time you spent on each previous assignment as a reference: this final homework should take at least as long as the average time you spent on other assignments. Another element to consider is that this final assignment is worth 20 points, while regular assignments are worth 15 points.
* As you complete the assignment, aim to review what you have learned in the course and try to push a bit beyond your comfort zone. If you have any doubts, check in with us: we can help you assess if your plan is appropriate!
* Please note, the goal of this homework is to demonstrate and reinforce what you have learned in the course. You are expected to complete it independently (you can rely on classmates or resources for advice, but the homework itself needs to be completed alone). We expect you to submit your own original code, adopt coding strategies that make sense to you, and code that you fully understand and can debug on your own.

### What data should I use?

You can use any data you want! We encourage you to find data in the social sciences, but if you have something else in mind, please check with us to ensure it’s a good fit. The most important thing is that your assignment demonstrates the skills you have learned in class and is useful for you. You don't have to choose something directly related to your own research: feel free to explore a topic for fun or one that will help you consolidate and expand your knowledge.

### I can't think of anything to analyze!

You can analyze one of the datasets we have used in the class, as long as it is not teaching-related data (e.g., penguins, cars, flowers, or other teaching-related datasets won't be appropriate) and as long as we have not used them for past homework assignments. 

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


### What if my data file is large?

Due to the way Git tracks changes in files, GitHub will not allow you to commit and push a file larger than 100MB. If you try to do so, you will receive an error message, and the commit will not push. Worse yet, you will have to find a way to strip all traces of the data file from the Git repository (including previous commits) before you can sync up your fork. This is a pain, so it's best to avoid it as much as possible.
 
If you follow options 1 and 2 above, you do not need to store the data file in the repo, as it will be automatically downloaded by your script or `Rmd` document.

For the purpose of this course, you can store the data outside GitHub and submit the link to the data in the repo. If you want store a large data file in your repo, use [**Git Large File Storage**](https://git-lfs.github.com/). It is a separate program you need to install via the shell, but the instructions are straightforward. It integrates smoothly into GitHub, and makes version tracking of large files much easier. If you want to use Git LFS for your own work, there are separate fees charged by GitHub for storage and bandwidth usage.

<!--
   * To emulate RStudio's "render" button from a [shell](/setup/shell/):
        `Rscript -e "quarto::quarto_render('input = myAwesomeAnalysis.qmd')"`
    * To emulate RStudio's "Knit" button within an R script:
        `quarto::quarto_render('input = myAwesomeAnalysis.qmd')`
-->


# Submit the assignment

* First push to your repository the last version of your assignment before the deadline. Make sure to stage-commit-push:

  - everything you have done to collect the data and produce your analyses, e.g., R Markdown files or R scripts, graphs, data (unless they are too large, see above for details)
  - your report should integrate code and written text and should be generated using a `Rmd` file, knitted as `md` or `github_document`; submit both the `Rmd` and `md` (you are welcome to knit the file also as `pdf` or `world` if you'd like)

* When you are ready to submit, copy your repository URL (e.g. `https://github.com/css-summer24/hw7-brinasab`) and submit it on Canvas under HW07 before the deadline. Do not submit files on Canvas, we only need the link to your repository 

* As part of your submission, write a few reflections about your experience with this homework, as specified in the instructions; make sure to report all resources you consulted to complete it


# Assessment

All homework assignments are evaluated using a rubric: see [here](/faq/homework-evaluations/) and [here](https://docs.google.com/spreadsheets/d/1h7_TmhUr5k7BGT3h-F4VJMUEEUtvvhqw/edit?usp=sharing&ouid=112534119211880791899&rtpof=true&sd=true) (this file is also accessible from the top of the "Lectures" page from our website).

Here are further guidelines to help you assess your homework; use these benchmarks to evaluate your work before submitting it:

In the past, "Excellent" or "Very Good" work has included submissions that met all requirements proficiently (e.g. the listed requirements regarding written text, plots, code, README files, etc.). Such work demonstrated a solid understanding of course materials, including data analysis and coding skills. The code was clean and efficient, and tables were clear and well-formatted, often using tools like kable, removing irrelevant data, and aggregating data appropriately. The graphs were well-crafted and diverse, each appropriately matching the variable type and incorporating some data wrangling. High-quality submissions also used multiple commits to show progression and back up work, followed a consistent and correct coding style, and included a detailed and insightful analysis and write-up. 
