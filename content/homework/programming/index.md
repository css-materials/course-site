---
title: "HW04: Tidying data & programming in R"
date: 2024-06-26T13:30:00-06:00  # Schedule page publish date
type: book
toc: true
draft: true
aliases: ["/hw04-programming.html"]
categories: []
weight: 40
---




# Overview

**Due Tuesday, July 2nd (11:59 PM).**

The goals of this homework assignment are to (1) practice manipulating tidy data, and (2) demonstrate competency in R programming skills, especially control structures.


# Accessing and cloning your `hw04` repository

* Go [at this link](https://classroom.github.com/a/MADvhEM7) to accept the invitation and create your private `hw04` repository on GitHub. Once you do so, your repo will be built in a few seconds. It follows the naming convention `hw04-<USERNAME>`
* Once your repository has been created, click on the provided link to access it. 
* Finally, follow the [same steps you completed for `hw01`](/homework/edit-readme/) to clone the repository to your R Workbench.


# General workflow

See Homework 1


# Assignment description

This homework assignment consists of two parts: 
* Part 1: practicing tidying data with `tidyr`
* Part 2: practicing programming in R by applying the programming techniques we have been learning so far 

In the repo for this assignment you will find a `.Rmd` file with the questions for each part.

For part 1, your main task is to tidy a data frame called `dadmom`, which is in the `rcis` package. The final product should look like this:


| famid|parent |name |   inc|
|-----:|:------|:----|-----:|
|     1|d      |Bill | 30000|
|     1|m      |Bess | 15000|
|     2|d      |Art  | 22000|
|     2|m      |Amy  | 18000|
|     3|d      |Paul | 25000|
|     3|m      |Pat  | 50000|



# Submit the assignment

To submit the assignment, follow these steps:

* First push to your repository the last version of your assignment before the deadline. Make sure to stage-commit-push the following files:

  - `programming_exercises.Rmd`: the main file you will add your code to
  - `programming_exercises.md`: you will generate this file from the `.Rmd` by knitting it 

* When you are ready to submit, copy your repository URL (e.g. `https://github.com/css-summer24/hw4-brinasab`) and submit it on Canvas under HW04 before the deadline. Do not submit files on Canvas, we only need the link to your repository 

* As part of your submission, at the end of the `.Rmd` for this homework write a few reflections about your experience with this homework, as specified in the instructions


# Assessment

All homework assignments are evaluated using a rubric: see [here](/faq/homework-evaluations/) and [here](https://docs.google.com/spreadsheets/d/1h7_TmhUr5k7BGT3h-F4VJMUEEUtvvhqw/edit?usp=sharing&ouid=112534119211880791899&rtpof=true&sd=true) (this file is also accessible from the top of the "Lectures" page from our website).

Further guidelines for this specific homework to help you assess your work before submitting it.
In the past, "Excellent" or "Very good" work included submissions that finished all components of the assignment correctly and used efficient code to complete them. Provide multiple options to answer the same question. Show solid command of basic R programming skills. Code is well-documented (both self-documented and with additional comments as necessary). Use multiple commits to back up and show a progression in the work. 
