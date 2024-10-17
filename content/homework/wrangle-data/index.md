---
title: "HW03: Wrangling data"
date: 2024-10-16T13:30:00-06:00  # Schedule page publish date
type: book
toc: true
draft: false
aliases: ["/hw03-wrangle-data.html"]
categories: []
weight: 30
---



# Overview

**Due Thursday, October 24th (11:59 PM).**

In the previous assignment you practiced working with `dplyr` and `ggplot2` on a clean and small-sized dataset. The goal of this assignment is to further develop your `dplyr` and `ggplot2` skills and practice cleaning, wrangling, and exploring social science data in a realistic research context (e.g., dealing with messy and larger datasets). 


# Accessing and cloning your `hw03` repository

* Go [at this link](https://classroom.github.com/a/hr2t-mDj) to accept the invitation and create your private `hw03` repository on GitHub. Once you do so, your repo will be built in a few seconds. It follows the naming convention `hw03-<USERNAME>`
* Once your repository has been created, click on the provided link to access it. 
* Finally, follow the [same steps you completed for `hw01`](/homework/edit-readme/) to clone the repository to your R Workbench.


# General workflow

See Homework 1 for details.


# Assignment description

## Explore the Data

The [Supreme Court Database](http://scdb.wustl.edu/) contains detailed information of every published decision of the U.S. Supreme Court since its creation in 1791. It is one the most utilized database in the study of judicial politics.

In the `hw03` repository, you will find two data files:

1. `scdb-case.csv`
1. `scdb-vote.csv`

These contain the exact same data you would obtain if you downloaded the files from the original website, but reformatted to be stored as relational data files. That is, `scdb-case.csv` contains all *case-level* variables, whereas `scdb-vote.csv` contains all *vote-level* variables.

The data is structured in as follows:

* `scdb-case.csv` contains one row for every case and one column for every variable
* `scdb-vote.csv` contains one row for every vote by a justice in every case and one column for every variable

The current data contain information on every case decided from the 1791-2020 terms.[^terms] There are several variables to explore, and I encourage you to do so, but these are the main ones you will need to answer most prompts:

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
* Task 2: Answer specific questions, and formulate (and answer) a question according to your interests 
* Task 3: Answer more open-ended questions, and formulate (and answer) a question according to your interests 

Please note:
* The questions, especially the open-ended ones, are designed to help you think and plan before diving into coding, similar to challenges you might face in real-world research settings. They won’t lay out exact step-by-step instructions, as they encourage you to apply and expand on the code you've learned so far. One of the main goals of this assignment (and future ones) is for you to tackle these challenges independently. We know you can do it!
* All assignments are designed to be completed in multiple coding sessions. Start early, and save, stage, commit, and push often!
* You are not allowed to use AI tools to generate R code to complete this and future assignments. The only acceptable uses of AI tools are the following two: debugging (but only after you have made an attempt on your own) and generating examples of how to use a specific function (but also check the function documentation, and the course materials -- if there are many ways to code something, you are expected prioritize what we have learned vs. what we have not). While AI tools can be helpful outside of class, this is a coding course, and it's all about learning to code in R, not learning to use AI!
* Do not submit code that you cannot fully explain to yourself and someone else.


## Formatting Guide

Refer to HW2 guidelines for formatting tables and graphs. Ensure you follow proper R coding style and make appropriate use of comments in your code (refer to the readings and lecture on this topic).


# Submit the assignment

To submit the assignment, follow these steps:

* First push to your repository the last version of your assignment before the deadline. Make sure to stage-commit-push the following files:

  - `scouts.Rmd`: main file you will add your code to
  - `scotus.md`: you will generate this file from the .Rmd by knitting it
  - the folders with all the graphs you generated in your `.Rmd` (we need this file to be able to see your graphs and grade your homework, if you do not submit it, we will mark down on reproducibility)

* When you are ready to submit, copy your repository URL (e.g. `https://github.com/css-fall24/hw3-brinasab`) and submit it on Canvas under HW03 before the deadline. Do not submit files on Canvas, we only need the link to your repository 

* As part of your submission, at the end of the `.Rmd` for this homework, include a few reflections on your experience with this assignment, list any help you might have received (from both humans and AI), as specified in the instructions.


# Assessment

All homework assignments are evaluated using a rubric which you can access from in the assignment submission folder on Canvas. See also [here](/faq/homework-evaluations/) for further info. 

Further guidelines for this specific homework to help you assess your work before submitting it.

In the past, "Excellent" or "Very Good" work included submissions that completed all components of the assignment correctly and accurately. Code ran correctly, followed proper style, and was well-documented without excessive comments. The code was appropriately complex and aligned with the prompt and course material (e.g., demonstrating a nuanced understanding of concepts and using them effectively throughout the assignment). Variables are correctly re-coded, possibly with the use of different approaches that we have learned in the course. Graphs and tables were well-executed and carefully chosen (e.g., matching variable types with graph types), with appropriate labels, colors, and enhanced default settings. The analysis was clear and easy to follow, with graphs properly interpreted. Explanation of the student's logic to solve a task, when required, was clear and on-point. There was a strong understanding of required packages, extending beyond the basics. Additionally, the repository showed a history of multiple informative commits, reflecting the progression and backup of work. Command of R Markdown syntax was evident, with no errors.

[^terms]: Terms run from October through June, so the 2020 term contains cases decided from October 2020 - June 2021.


# Acknowledgments

<!--

* This page has been developed starting from Benjamin Soltoff’s “Computing for the Social Sciences” course materials, licensed under the CC BY-NC 4.0 Creative Commons License.
-->

The initial version of this homework was developed by Benjamin Soltoff  (“Computing for the Social Sciences” licensed under the CC BY-NC 4.0 Creative Commons License). Further implementations have been developed by Sabrina Nardin.
