---
title: "HW05: Debugging and practice working with functions and tidy data"
date: 2023-11-1T13:30:00-06:00  # Schedule page publish date
type: book
toc: true
draft: false
categories: []
weight: 50
---



# Overview

**Due Thursday, November 9th (11:59 PM).**

In previous assignments, you practiced applying tidy data principles and working with functions using toy datasets. The goal of this assignment is twofold: practice debugging common errors in code and practice working with functions and applying tidy data principles with a real social science dataset.


# Accessing the `hw05` repository

* Go [at this link](https://classroom.github.com/a/Y_PGoY5Y) to accept and create your private `hw05` repository on GitHub. Once you do so, your repository will be built in a few seconds. It follows the naming convention `hw05-<USERNAME>`  
* Once the your repository has been created, click on the link you see, which will take you to your repository. 
* Finally, clone the repository to your R Workbench (or your computer if you have installed R there) following the process below.


# Cloning your `hw05` repository

After you have accessed the `hw05` repository (see above), follow the [same steps you completed for `hw01`](/homework/edit-readme/) to clone the repository.


# General workflow

See Homework 1


# Assignment description

This assignment has two parts. The first asks you to debug some code, the second asks you to work with the world bank data.


# PART 1: Debug code

The repository contains a file called `fix-errors.Rmd`, which includes code to conduct research of baby name popularity in the United States using the [`babynames`](http://hadley.github.io/babynames/) package. 

Its author made some mistakes and the script currently does not work. Your task is to fix the errors/warnings in the script to generate the desired output.


# PART 2: Working with the world bank data

The World Bank publishes extensive socioeconomic data on countries and economies worldwide. In the `data_world_bank` folder included in this assignment, there are all the World Bank’s `csv` data files with economic indicators for each country (https://data.worldbank.org/indicator). Each `csv` file contains data on a given country economy's data.

Edit the `world-bank.Rmd` file and complete the following tasks (detailed instructions are provided in `world-bank.Rmd`):

1. Write  a function that imports a data file (one single data file) and renames some of the columns in each data file. Remember to document your function. Then call the function to import all files. Finally, show how to call the function both with a for loop and with map

2. Tidy the imported data

<!--
Once you have the data imported, write a brief report exploring and analyzing at least [two variables in the data](http://data.worldbank.org/indicator). Use a combination of descriptive statistics, tables, and figures, and present your results and analysis in a coherent and interpretable manner. The main point is that your report should not just be code and output from R - you also need to include your own written analysis. Submitting the report as an [Quarto document](http://rmarkdown.rstudio.com/) will make this much easier (and is in fact mandatory).
-->


# Submit the assignment

To submit the assignment, follow these steps:

* First push to your repository the last version of your assignment before the deadline. Make sure to stage-commit-push the following files:
    
    - `fix-errors.Rmd` and its knitted `md`
    - `world-bank.Rmd` and its knitted `md`

* When you are ready to submit, copy your repository URL (e.g. https://github.com/css-fall23/hw5-brinasab) and submit it on Canvas under HW05 before the deadline. Do not submit files on Canvas, we only need the link to your repository 

* As part of your submission, in the `world-bank.Rmd` for this homework:
  * write 1-2 paragraphs of reflections about the homework
  * list the first and last name of eventual collaborators with whom you worked with to complete this assignment
  
  
# Assessment

All homework assignments are evaluated using [this general rubric](/faq/homework-evaluations/). Make sure to check it. 

Below are further guidelines for this specific homework to help you assess your work before submitting it.

*Needs improvement:* The errors script has not been successfully fixed or has only partially been fixed. The functions to import the data has not been fully set up, and/or is used incorrectly. Data are not tidy. The code does not run and/or partially runs. Partial or insufficient attention to standards of reproducible research.

*Good:* Solid effort. Hits all the elements. Finished all components of the assignment with no or only minor deficiencies. Easy to follow (both the code and the output). Submitted work shows sufficient understanding of the packages needed for the assignment.

*Excellent:* Finished all assignment components correctly and used efficient code to complete the exercises. The solutions adopted went beyond what strictly required. The code is well-documented. The function is written succinctly/comprehensibly and used correctly. Data are tidy. Use multiple commits to back up, with meaningul messages, and show a progression in work.


# Acknowledgments

* This page has been developed starting from Benjamin Soltoff’s “Computing for the Social Sciences” course materials, licensed under the CC BY-NC 4.0 Creative Commons License.
