---
title: "HW03: Wrangling and visualizing data"
date: 2024-06-19T13:30:00-06:00  # Schedule page publish date
type: book
toc: true
draft: true
aliases: ["/hw03-wrangle-data.html"]
categories: []
weight: 30
---



# Overview

**Due Tuesday, June 25th (11:59 PM).**

The goal of this assignment is to practice cleaning, wrangling, and exploring social science data in a research context (e.g., dealing with messy and large datasets). This assignment offers an opportunity to further develop your `dplyr` and `ggplot2` skills.


# Accessing and cloning your `hw03` repository

* Go [at this link](https://classroom.github.com/a/fXA4cWSB) to accept the invitation and create your private `hw03` repository on GitHub. Once you do so, your repo will be built in a few seconds. It follows the naming convention `hw03-<USERNAME>`
* Once your repository has been created, click on the provided link to access it. 
* Finally, follow the [same steps you completed for `hw01`](/homework/edit-readme/) to clone the repository to your R Workbench.


# General workflow

See Homework 1


# Assignment description

## Explore the Data

The [Supreme Court Database](http://scdb.wustl.edu/) contains detailed information of every published decision of the U.S. Supreme Court since its creation in 1791. It is perhaps the most utilized database in the study of judicial politics.

In the `hw03` repository, you will find two data files:

1. `scdb-case.csv`
1. `scdb-vote.csv`

These contain the exact same data you would obtain if you downloaded the files from the original website, but reformatted to be stored as relational data files. That is, `scdb-case.csv` contains all *case-level* variables, whereas `scdb-vote.csv` contains all *vote-level* variables.

The data is structured in as follows:

* `scdb-case.csv` contains one row for every case and one column for every variable
* `scdb-vote.csv` contains one row for every vote by a justice in every case and one column for every variable

The current data contain information on every case decided from the 1791-2020 terms.[^terms] There are several variables, but for our purposes, these are the variables you will want to familiarize yourself:

* `caseIssuesId`
* `chief`
* `dateDecision`
* `decisionDirection`
* `decisionType`
* `declarationUncon`
* `direction`
* `issueArea`
* `justice`
* `justiceName`
* `majority`
* `majVotes`
* `minVotes`
* `term`

{{% callout note %}}
Read the [documentation](http://scdb.wustl.edu/documentation.php) to see how these variables are coded and familiarize yourself with the data.
{{% /callout %}}


## Answer the questions

Your repository for this assignment includes an `.Rmd` file with three tasks, each containing a set of questions, some specific and others more open-ended. Please, answer all of them.

* Task 1: Recode variables
* Task 2: Answer specific questions
* Task 3: Answer more open-ended questions, and formulate (and answer) a question according to your interests 


## Formatting Guide

Refer to HW2 guidelines for formatting tables and graphs. Ensure you follow proper R coding style and make appropriate use of comments in your code (refer to the readings and lecture on this topic).


# Submit the assignment

To submit the assignment, follow these steps:

* First push to your repository the last version of your assignment before the deadline. Make sure to stage-commit-push the following files:

  - `scouts.Rmd`: main file you will add your code to
  - `scotus.md`: you will generate this file from the .Rmd by knitting it
  - the folders with all the graphs you generated in your `.Rmd`

* When you are ready to submit, copy your repository URL (e.g. `https://github.com/css-summer24/hw3-brinasab`) and submit it on Canvas under HW03 before the deadline. Do not submit files on Canvas, we only need the link to your repository 

* As part of your submission, at the end of the `.Rmd` for this homework write a few reflections about your experience with this homework, as specified in the instructions


# Assessment

All homework assignments are evaluated using a rubric: see [here](/faq/homework-evaluations/) and [here](https://docs.google.com/spreadsheets/d/1h7_TmhUr5k7BGT3h-F4VJMUEEUtvvhqw/edit?usp=sharing&ouid=112534119211880791899&rtpof=true&sd=true) (this file is also accessible from the top of the "Lectures" page from our website).

Further guidelines for this specific homework to help you assess your work before submitting it.
In the past, "Excellent" or "Very good" work included submissions that completed all components of the assignment accurately, with well-written, efficient, and well-documented code (both self-documented and with additional comments as necessary). Variables are correctly re-coded, possibly with the use of different approaches. Graphs and tables were properly labeled, well-executed, and carefully chosen, ensuring a match between variable type and graph type, using appropriate colors, and improving the default settings. Answers demonstrated a strong command of the necessary packages for the assignment. Responses went beyond expectations, showcasing exceptional mastery of the materials. The repository exhibited a history of multiple informative commits, demonstrating a clear progression in the work.

[^terms]: Terms run from October through June, so the 2020 term contains cases decided from October 2020 - June 2021.


# Acknowledgments

* This page has been developed starting from Benjamin Soltoff’s “Computing for the Social Sciences” course materials, licensed under the CC BY-NC 4.0 Creative Commons License.
