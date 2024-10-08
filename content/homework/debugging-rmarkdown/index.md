---
title: "HW05: Debugging & practice working with functions"
date: 2024-07-02T13:30:00-06:00  # Schedule page publish date
type: book
toc: true
draft: true
categories: []
weight: 50
---



# Overview

**Due Tuesday, July 9th (11:59 PM).**

In the previous homework assignment, you practiced applying tidy data principles and using R programming techniques with toy data. This assignment builds on that foundation by offering an opportunity to further practice these skills, as well as the new skills you have acquired this week, using real social science datasets.


# Accessing and cloning your `hw05` repository

* Go [at this link](https://classroom.github.com/a/hgBx2KXX) to accept the invitation and create your private `hw05` repository on GitHub. Once you do so, your repo will be built in a few seconds. It follows the naming convention `hw05-<USERNAME>`
* Once your repository has been created, click on the provided link to access it. 
* Finally, follow the [same steps you completed for `hw01`](/homework/edit-readme/) to clone the repository to your R Workbench.


# General workflow

See Homework 1


# Assignment description

This assignment is divided in two parts:

* Part 1 offers an opportunity to solidify your understanding of functions in R and to improve your skills in spotting and fixing common sources of errors in code using the `babynames` package (with multiple datasets). 

* Part 2 simulates a real data analysis scenario and asks you to apply functions and previous course contents (loops, tidyr, data manipulation and visualization, etc.) to manipulate `wordbank` data.


## PART 1: Debug code

The repository contains a file called `fix-errors.Rmd`, which includes code to conduct research of baby name popularity in the United States using the [`babynames`](http://hadley.github.io/babynames/) package and two specific data sets in it `babynames` and `applicants`. 

Its author made some mistakes and the script currently does not work. Your task is to fix the errors/warnings in the script to generate the desired output.


## PART 2: Working with the world bank data

The World Bank publishes extensive socioeconomic data on countries and economies worldwide. In the `data_world_bank` folder included in this assignment, there are all the World Bank’s `csv` data files with economic indicators for each country (https://data.worldbank.org/indicator). Each `csv` file contains data on a given country economy's data.

Edit the `world-bank.Rmd` file and complete the following tasks (detailed instructions for each task are provided in the file `world-bank.Rmd` located in in your repo):

1. Write a well-documented function that imports a single data file and renames some of the columns. Then call the function to import all files.

2. Tidy the imported data

3. Compute simple statistics and visualize the data

<!--
Once you have the data imported, write a brief report exploring and analyzing at least [two variables in the data](http://data.worldbank.org/indicator). Use a combination of descriptive statistics, tables, and figures, and present your results and analysis in a coherent and interpretable manner. The main point is that your report should not just be code and output from R - you also need to include your own written analysis. Submitting the report as an [Quarto document](http://rmarkdown.rstudio.com/) will make this much easier (and is in fact mandatory).
-->


# Submit the assignment

To submit the assignment, follow these steps:

* First push to your repository the last version of your assignment before the deadline. Make sure to stage-commit-push the following files (and the plots you generate):
    
    - `fix-errors.Rmd` and its knitted `md`
    - `world-bank.Rmd` and its knitted `md`

* When you are ready to submit, copy your repository URL (e.g. https://github.com/css-summer24/hw5-brinasab) and submit it on Canvas under HW05 before the deadline. Do not submit files on Canvas, we only need the link to your repository 

* As part of your submission, at the end of the `world-bank.Rmd` file write 1-2 paragraphs of reflections about the homework, as specified in the instructions

  
# Assessment

All homework assignments are evaluated using a rubric: see [here](/faq/homework-evaluations/) and [here](https://docs.google.com/spreadsheets/d/1h7_TmhUr5k7BGT3h-F4VJMUEEUtvvhqw/edit?usp=sharing&ouid=112534119211880791899&rtpof=true&sd=true) (this file is also accessible from the top of the "Lectures" page from our website).

Further guidelines for this specific homework to help you assess your work before submitting it:
In the past, "Excellent" or "Very good" work included submissions that finished all components of the assignment correctly and used efficient code to complete them. The solutions adopted went beyond what strictly required. The code is well-documented. The function is written succinctly/comprehensibly and used correctly. Data are tidy. Task 3 is completed creatively and in-depth, showing student's interests and research abilities. Use multiple commits to back up, with meaningful messages, and show a progression in work.

