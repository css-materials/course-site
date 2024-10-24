---
title: "HW02: Exploring data"
date: 2024-10-09T13:30:00-06:00  # Schedule page publish date
type: book
toc: true
draft: false
aliases: ["/hw02-explore-data.html"]
categories: []
weight: 20
---



# Overview

**Due Thursday, October 17th (11:59 PM).**

In HW01 you have demonstrated knowledge of your software setup, Git/GitHub via RStudio, and Markdown. The goal of this second assignment is to practice transforming and visually exploring data with `dplyr` and `ggplot2`.


# Accessing and cloning your `hw02` repository

* Go [at this link](https://classroom.github.com/a/z9Lc54LU) to accept the invitation and create your private `hw02` repository on GitHub. Once you do so, your repo will be built in a few seconds. It follows the naming convention `hw02-<USERNAME>`
* Once your repository has been created, click on the provided link to access it. 
* Finally, follow the [same steps you completed for `hw01`](/homework/edit-readme/) to clone the repository to your R Workbench.


# General workflow

See Homework 1 for details.

<!--
Please notice for this assignment we expect you to do some more work in terms of formatting and reproducibility: submit a homework that fully complies with the [Homework Guidelines](/faq/homework-guidelines/#homework-workflow).
--> 


# Assignment description

Your goal for this assignment is to apply what you have learned so far by answering a set of questions using a cleaned dataset that we provide: **the "mass shooting" dataset.**

The United States experiences far more mass shooting events than any other developed country in the world. Policymakers, politicians, the media, activists, and the general public acknowledge the widespread prevalence of these tragic events. However, effective policies to prevent such incidents should be grounded in empirical data

In July 2012, in the aftermath of a mass shooting in a movie theater in Aurora, Colorado,
[Mother Jones](https://www.motherjones.com/politics/2012/07/mass-shootings-map/) published a report on mass shootings in the United States since 1982. Importantly, they provided the underlying data set as [an open-source database](https://www.motherjones.com/politics/2012/12/mass-shootings-mother-jones-full-data/) for anyone interested in studying and understanding this criminal behavior.


## Obtain the data

This dataset in included in the [`rcis`](https://github.com/css-materials/rcis) library on GitHub. 

* If you are working on Workbench, you should have everything already installed. Simply load the library by typing in your console `library(rcis)`, then load the dataset by typing `data("mass_shootings")`. Type `?mass_shootings` for detailed information on the variables and other coding information. I'd suggest to work with R version 4.2 on Workbench

* If you are using R on your local computer, you first need to install the `rcis` by typing in your console `remotes::install_github("css-materials/rcis")`. If you don't already have the `remotes` library installed, you will get an error. Go back and install it first using `install.packages()`, then install `rcis`. Finally, the mass shootings dataset can be loaded using `data("mass_shootings")`. Use the help function in R `?mass_shootings` for detailed information on the variables and other coding information.


## Answer the questions

Your repository for this assignment includes a set of questions, some very specific and others more open-ended. Answer all of them.

Please note:
* The questions, especially the open-ended ones, are designed to help you think and plan before diving into coding, similar to challenges you might face in real-world research settings. They won’t lay out exact step-by-step instructions, as they encourage you to apply and expand on the code you've learned so far. One of the main goals of this assignment (and future ones) is for you to tackle these challenges independently. We know you can do it!
* All assignments are designed to be completed in multiple coding sessions. Start early, and save, stage, commit, and push often!
* You are not allowed to use AI tools to generate R code to complete this and future assignments. The only acceptable uses of AI tools are the following two: debugging (but only after you have made an attempt on your own) and generating examples of how to use a specific function (but also check the function documentation, and the course materials). While AI tools can be helpful outside of class, this is a coding course, and it's all about learning to code in R, not learning to use AI!
* Do not submit code that you cannot fully explain to yourself and someone else.


## Formatting Guide

#### Formatting graphs

While you are practicing Exploratory Data Analysis, your final graphs should be appropriate for sharing with outsiders. That means your graphs should have:

* [A title](http://r4ds.had.co.nz/graphics-for-communication.html#label)
* Labels on the axes (type `?labs` in your Console for details)

Consider adopting your own color scales, [taking control of your legends (if any)](http://www.cookbook-r.com/Graphs/Legends_(ggplot2)/), playing around with [themes](https://ggplot2.tidyverse.org/reference/index.html#section-themes), and generally customizing your graphs to improve their visual appeal and clarity.


#### Formatting tables

When presenting tabular data (using `dplyr::summarize()`), use the `kable()` function from the `knitr` package to format the table for the final document.  Keep reading for an example on how to use this function.

The code below displays a basic table summarizing where gun deaths occurred:




```r
# calculate total gun deaths by location
count(mass_shootings, location_type)
```

```
## # A tibble: 6 × 2
##   location_type     n
##   <chr>         <int>
## 1 Airport           1
## 2 Military          6
## 3 Other            49
## 4 Religious         6
## 5 School           18
## 6 Workplace        45
```

Instead, use `kable()` to format the table, add a caption, and label the columns:


```r
count(mass_shootings, location_type) %>%
  kable(
    caption = "Mass shootings in the United States by location",
    col.names = c("Location", "Number of incidents")
  )
```



Table: <span id="tab:table-good"></span>Table 1: Mass shootings in the United States by location

|Location  | Number of incidents|
|:---------|-------------------:|
|Airport   |                   1|
|Military  |                   6|
|Other     |                  49|
|Religious |                   6|
|School    |                  18|
|Workplace |                  45|

Run `?kable` in the console for additional options. We expect you to use this function for formatting tabular data in this and future assigments.


# Submit the assignment

To submit the assignment, follow these steps:

* First push to your repository the last version of your assignment before the deadline. Make sure to stage-commit-push the following files:
  * `mass-shootings.Rmd`: you will add your code to this file
  * `mass-shootings.md`: you will generate this file from the .Rmd by simply knitting it, like you did for HW01 (we need this file to be able to see your graphs and grade your homework, if you do not submit it, we will mark down on reproducibility)
  * `mass-shootings_files/`: this folder contains all the graphs that you generated in your `.Rmd`

* When you are ready to submit, copy your repository URL (e.g. `https://github.com/css-fall24/hw2-brinasab`) and submit it on Canvas under HW02 before the deadline. Do not submit files on Canvas, we only need the link to your repository. 

* As part of your submission, at the end of the `.Rmd` for this homework, include a few reflections on your experience with this assignment, list any help you might have received (from both humans and AI), as specified in the instructions.


# Assessment

All homework assignments are evaluated using a rubric: see [here](/faq/homework-evaluations/).

Below are further guidelines for this specific homework to help you assess your work before submitting it. 

In the past, "Excellent" or "Very Good" work included submissions that completed all components of the assignment correctly and accurately. Code ran correctly, followed proper style, and was well-documented without excessive comments. The code was appropriately complex and aligned with the prompt and course material (e.g., demonstrating a nuanced understanding of concepts and using them effectively throughout the assignment). Graphs and tables were well-executed and carefully chosen (e.g., matching variable types with graph types), with appropriate labels, colors, and enhanced default settings. The analysis was clear and easy to follow, with graphs properly interpreted. There was a strong understanding of required packages, extending beyond the basics. Additionally, the repository showed a history of multiple informative commits, reflecting the progression and backup of work. Command of R Markdown syntax was evident, with no errors.

<!--
*Needs improvement:* Doesn't complete all components. Code is too minimal, poorly written, and/or not documented. Plots are not correct and/or too minimal (e.g., same type of plot for each graph, or doesn't use plots appropriate for the variables being analyzed, or missing labels/titles, or leave default without experimenting). Does not follow or follows incorrectly the provided formatting guide. Shows partial or incomplete understanding of the packages needed for the assignment. Interpretation is lacking or incomplete. No record of commits other than the final push to GitHub (we expect students to commit often).

*Good:* Solid effort. Hits all the elements. Minor omissions but no clear mistakes. Easy to follow (both the code and the output). Shows sufficient understanding of the packages needed for the assignment.

*Excellent:* Finished all components of the assignment correctly. Code is well-documented (both self-documented and with additional comments as necessary). Graphs and tables are properly labeled, well-executed, and carefully chosen. Analysis is clear and easy to follow (e.g., graphs are labeled clearly and/or additional text to describe how you interpret the output). Shows solid understanding of the packages needed for the assignment. Repo shows history of multiple commits to back up and show a progression in the work.
-->

# Acknowledgments

The initial version of this homework was developed by Benjamin Soltoff  (“Computing for the Social Sciences” licensed under the CC BY-NC 4.0 Creative Commons License). Further implementations have been developed by Sabrina Nardin.

<!-- {r child = here::here("R", "_ack_ben.Rmd")} -->

<!--
[^clean]: For the purposes of this assignment, some data cleaning of the underlying raw data have been performed. You can view the data cleaning code [here](https://github.com/cis-ds/rcis/blob/master/data-raw/mass-shootings.R).
-->
