---
title: "HW05: Debugging & working with functions"
date: 2024-11-06T13:30:00-06:00  # Schedule page publish date
type: book
toc: true
draft: false
categories: []
weight: 50
---



# Overview

<!-- NOTE FROM FALL 2024
rename this hw from course site and in part 1 add one exercise on taking code from previous hw and rewrite using function, like Iris did on ED, add a few sentences to explain what changed and why
-->

**Due Thursday, November 14th (11:59 PM).**

In the previous homework assignment, you practiced applying tidy data principles and using R programming techniques with simple datasets. 

This assignment builds on that foundation by offering an opportunity to further practice these skills, and the new skills you have acquired this week, using real social science datasets.


# Accessing and cloning your `hw05` repository

* Go [at this link](https://classroom.github.com/a/yRu7pE7C) to accept the invitation and create your private `hw05` repository on GitHub. Once you do so, your repo will be built in a few seconds. It follows the naming convention `hw05-<USERNAME>`
* Once your repository has been created, click on the provided link to access it. 
* Finally, follow the [same steps you completed for `hw01`](/homework/edit-readme/) to clone the repository to your R Workbench.


# General workflow

See Homework 1 for details.


# Assignment description

This assignment is divided in two parts:

* PART 1 `fix-errors.Rmd` offers an opportunity to solidify your understanding of functions in R and to improve your skills in spotting and fixing common sources of errors in code using the `babynames` package with mutiple datasets. 

* PART 2 `world-bank.Rmd` simulates a real-world data analysis scenario and asks you to apply functions and various course contents (loops, tidyr, data manipulation and visualization, etc.) to work with the `wordbank` social science dataset.


## PART 1

The repository contains a file called `fix-errors.Rmd`, which includes code to conduct research of baby name popularity in the United States using the [`babynames`](http://hadley.github.io/babynames/) package and two specific data sets in it `babynames` and `applicants`. 

Its author made some mistakes and the script currently does not work. Your task is to fix the errors/warnings in the script to generate the desired output.


## PART 2

The World Bank publishes extensive socioeconomic data on countries and economies worldwide. In the `data_world_bank` folder included in this assignment, there are all the World Bank’s `csv` data files with economic indicators for each country (https://data.worldbank.org/indicator). Each `csv` file contains data on a given country economy's data.

Edit the `world-bank.Rmd` file and complete the following tasks (detailed instructions for each task are provided in the file `world-bank.Rmd` located in in your repo):

1. Write a well-documented function that imports a single data file and renames some of the columns. Then call the function to import all files.

2. Tidy the imported data.

3. Compute simple statistics, visualize, and interpret the data.

<!--
Once you have the data imported, write a brief report exploring and analyzing at least [two variables in the data](http://data.worldbank.org/indicator). Use a combination of descriptive statistics, tables, and figures, and present your results and analysis in a coherent and interpretable manner. The main point is that your report should not just be code and output from R - you also need to include your own written analysis. Submitting the report as an [Quarto document](http://rmarkdown.rstudio.com/) will make this much easier (and is in fact mandatory).
-->

**Please note:**

* The questions are designed to help you think and plan before diving into coding, similar to challenges you might face in real-world research settings. They won’t lay out exact step-by-step instructions, as they encourage you to apply and expand on the code you've learned so far. One of the main goals of this assignment (and future ones) is for you to tackle these challenges independently. We know you can do it!
* All assignments are designed to be completed in multiple coding sessions. Start early, and save, stage, commit, and push often!
* You are not allowed to use AI tools to generate R code to complete this and future assignments. The only acceptable uses of AI tools are the following two: debugging (but only after you have made an attempt on your own) and generating examples of how to use a specific function (but also check the function documentation, and the course materials -- if there are many ways to code something, you are expected prioritize what we have learned vs. what we have not). While AI tools can be helpful outside of class, this is a coding course, and it's all about learning to code in R, not learning to use AI!
* Do not submit code that you cannot fully explain to yourself and someone else.

Refer to HW2 guidelines for formatting tables and graphs. Ensure you follow proper R coding style and make appropriate use of comments in your code (refer to the readings and lecture on this topic).


# Submit the assignment

To submit the assignment, follow these steps:

* First push to your repository the last version of your assignment before the deadline. Make sure to stage-commit-push the following files (and the plots you generate):
    
    - `fix-errors.Rmd` and its knitted `md`
    - `world-bank.Rmd` and its knitted `md`

* When you are ready to submit, copy your repository URL (e.g. https://github.com/css-fall24/hw5-brinasab) and submit it on Canvas under HW05 before the deadline. Do not submit files on Canvas, we only need the link to your repository 

* As part of your submission, at the end of the `world-bank.Rmd` include a few reflections on your experience with this assignment, list any help you might have received (from both humans and AI), as specified in the instructions.

  
# Assessment

All homework assignments are evaluated using a rubric which you can access from the assignment submission folder on Canvas. See also [here](/faq/homework-evaluations/) for more. 

Further guidelines for this specific homework to help you assess your work before submitting it.

In the past, "Excellent" or "Very Good" work included submissions that completed all components of the assignment correctly and accurately. Code ran correctly, followed proper style, and was well-documented without excessive comments. The code and answers demonstrated strong grasp of class materials and were aligned with the prompt and course materials, demonstrating a nuanced understanding of concepts and using them effectively throughout the assignment.
Bugs in code are correctly identified and well-explained. Functions are written succinctly/comprehensibly and used correctly. Data are tidy. The open question(s) are completed creatively and in-depth, showing student's interests and research abilities. Use multiple commits to back up, with meaningful messages, and show a progression in work.
The repository showed a history of multiple informative commits, reflecting the progression and backup of work. Command of R Markdown syntax was evident, with no errors.


# Acknowledgments

<!--

* This page has been developed starting from Benjamin Soltoff’s “Computing for the Social Sciences” course materials, licensed under the CC BY-NC 4.0 Creative Commons License.
-->

The initial version of this homework was developed by Benjamin Soltoff  (“Computing for the Social Sciences” licensed under the CC BY-NC 4.0 Creative Commons License). Further implementations have been developed by Sabrina Nardin.
