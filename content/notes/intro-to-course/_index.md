---
title: "Introduction to the course"
date: 2022-09-25T12:25:00-05:00
type: book
toc: true
draft: false
aliases: ["/intro.html", "/notes/intro-to-course/"]
categories: []

weight: 10
---



## The data workflow

{{< figure src="data-science.png" caption="Data science workflow. Source: [R for Data Science](http://r4ds.had.co.nz/) by Garrett Grolemund and Hadley Wickham." >}}

Computationally driven research follows a specific workflow. This is the ideal - in this course, I want to illustrate and explain to you why each stage is important and how to do it.

### Import

First you need to get your data into whatever software package you will use to analyze it. Most of us are familiar with data stored in flat files (e.g. spreadsheets). However a lot of interesting data cannot be obtained in a single specific and simple format. Information you need could be stored in a database, or a web API, or even (gasp!) **printed books**. You need to know how to convert/extract information into your software package of choice.

### Tidy

Tidying your data means to store it in a standardized form that enables the use of a standard library of functions to analyze the data. When your data is tidy, each column is a variable, and each row is an observation. By storing data in a consistent structure, you can focus your efforts on questions about the data and not constantly wrangling the data into different forms. Contrary to what you might expect, much of a researcher's time is spent wrangling and cleaning data into a tidy format for analysis. While not glamorous, tidying is an important stage.

### Transform

Transforming data can take on different tasks. Typically these include subsetting the data to focus on one specific set of observations, creating new variables that are functions of existing variables, or calculating summary statistics for the data.

### Visualize

Humans love to visualize information, as it reduces the complexity of the data into an easily interpretable format. There are many different ways to visualize data - knowing how to create specific graphs is important, but even more so is the ability to determine what visualizations are appropriate given the variables you wish to analyze.

### Model

Models complement visualizations. While visualizations are intuitive, they do not scale well to complex relationships. Visualizing two (or even three) variables is a straightforward exercise, but once you are dealing with four or more variables visualizations become pointless. Models are fundamentally mathemetical, so they scale well to many variables. However all models make assumptions about the form of relationships, so if you choose an inappropriate functional form the model will not tell you that you are wrong.

### Communicate

All of the above work will be for naught if you fail to communicate your project to a larger audience. You need to not only understand your data, but also communicate your results to others so that the community can learn from your knowledge.

### Programming

Programming is the tool that encompasses all of the previous stages. You can use programming in all facets of your project. You do not need to be an expert programmer to be a computational social scientist, but learning to program will make your life **much easier**.

## Basic principles of programming

A **program** is a series of instructions that specifies how to perform a computation.[^downey]

Much of computer programming involves translating what you wish to do into a set of instructions. 

Think of human languages: languages conform to specific sets of grammatical and syntax rules which define how to interpret elements of speech such as nouns, verbs, and adjectives. Some languages have simple rules and are (relatively) easy to learn; others follow more complex rules that require greater effort in order to gain fluency. Some languages derive from a common source and therefore share many similarities that make it easier to learn a second language within the same family of languages. So a native Spanish speaker will find it easier to learn French rather than Chinese, because French and Spanish share many grammatical rules and root derivations of words whereas Chinese and Spanish do not. Regardless, these are all perfectly usable languages humans use to communicate with one another. 

Major components to programs are:

* **Input** - what is being manipulated/utilized. Typically these are data files from your hard drive or the internet.
* **Output** - display data or analysis on the computer, include in a paper/report, publish on the internet, etc.
* **Math** - basic or complex mathematical and statistical operations. This could be as simple as addition or subtraction, or more complicated like estimating a linear regression or statistical learning model.
* **Conditional execution** - check for certain conditions and only perform operations when conditions are met.
* **Repetition** - perform some action repeatedly, usually with some variation.

Virtually all programs are built using these fundamental components. Obviously the more components you implement, the more complex the program will become. The skill is in breaking up a problem into smaller parts until each part is simple enough to be computed using these basic instructions.

## GUI software

A **graphical user interface (GUI)** is a visual way of interacting with a computer using elements such as a mouse, icons, and menus.

{{< figure src="windows_3.1.png" caption="Windows 3.1" >}}

{{< figure src="mac_os_x.png" caption="Mac OSX" >}}

{{< figure src="android_phones.jpg" caption="Android operating system" >}}

GUI software runs using all the basic programming elements, but the end user is not aware of any of this. Instructions in GUI software are **implicit** to the user, whereas programming requires the user to make instructions **explicit**.

<!--
{{< figure src="shell.png" caption="Programming in [the shell](/setup/shell/)" >}}
-->

## Benefits to programming vs. GUI software

Let's demonstrate why you should want to learn to program.[^stata] What are the advantages over GUI software, such as Stata?

{{< figure src="stata14.png" caption="Stata" >}}

Here is a hypothetical assignment:

> Write a report analyzing the relationship between ice cream consumption and crime rates in New York City.

Let's see how two students (Jane and Sally) would complete this. Jane will use strictly GUI software, whereas Sally will use programming and the data science workflow we outlined above.

#### Jane: Typical workflow of an undergraduate writing a research paper

1. Jane finds data files online with total annual ice cream sales in the 50 largest U.S. cities from 2001-2010 and total numbers of crimes (by type) for the 50 largest U.S. cities from 2001-2010. She gets them as spreadsheets and downloads them to her computer, saving them in her main `Downloads` folder which includes everything she's downloaded over the past three years. 

1. Jane opens the files in Excel.
    * Ice cream sales - frozen yogurt is not ice cream. She deletes the column for frozen yogurt sales.
    * Crime data - Jane is only interested in violent crime. She deletes all rows pertaining to non-violent offenses.
    * Jane saves these modified spreadsheets in a new folder created for this paper.
1. Jane opens Stata.
    * First she imports the ice cream data file using the drop-down menu.
    * Next she merges this with the crime data using the drop-down menu. There are some settings she tweaks when she does this, but Jane doesn't bother to write them down anywhere.
    * Then she creates new variables for per capita ice cream sales and per capita crime rates.
    * After that, she estimates a linear regression model for the relationship between the two per capita variables.
    * Finally she creates a graph plotting the relationship between these two variables.
1. Jane writes her report in Google Docs.
    * Huzzah! She finds a correlation between the two variables. Jane writes up her awesome findings and prepares for her A+.
    * The professor wants her results in the paper itself? Darn it. Okay, she copies and pastes her regression results and graph into the paper.
1. Jane prints her report and turns it in to the professor. Done!

#### Sally: Using a computational data science workflow

1. Sally creates a folder specifically for this project and divides it into subfolders (e.g. `data`, `graphics`, `output`).
1. Next she finds data files online with total annual ice cream sales in the 50 largest U.S. cities from 2001-2010 and total numbers of crimes (by type) for the 50 largest U.S. cities from 2001-2010. She writes a program to download these files to the `data` subfolder.
1. Then Sally writes a program in R that opens each data file and filters/cleans the data to get the necessary variables. She saves the cleaned data as new files in the `data` folder.
1. Sally writes a separate program which imports the cleaned data files, estimates a regression model, generates a graph, and saves the regression results and graph to the `output` subfolder.
1. Sally creates an [R Markdown](http://rmarkdown.rstudio.com) document for her report and analysis. Because R Markdown combines both code and text, the results from step 3 are automatically added into the final report.
1. Sally submits the report to the professor. Done!

## The value of automation

The professor is impressed with Jane and Sally's findings, but wants them to verify the results using new data files for ice cream **and frozen yogurt** sales and crime rates for 2011-2020 before he will determine their grade.

At this point, Jane is greatly hampered by her GUI workflow. She now has to repeat steps 1-5 all over again, but she forgot how she defined violent vs. non-violent crimes. She also no longer has the original frozen yogurt sales data and has to find the original file again somewhere on her computer or online. She has to remember precisely all the menus she entered and all the settings she changed in order to reproduce her findings.

Sally's computational workflow is much better suited to the professor's request because it is **automated**. All Sally needs to do is add the updated data files to the `data` subfolder, then rewrite her program in step 2 to combine the old and new data files. Next she can simply re-run the programs in steps 3 and 4 with no modifications. The analysis program accepts the new data files without issue and generates the updated regression model estimates and graph. The R Markdown document automatically includes these revised results without any need to modify the code in underlying document.

By automating her workflow, Sally can quickly update her results. Jane has to do all the same work again. Data cleaning alone is a non-trivial challenge for Jane. And the more data files in a project, the more work that has to be done. Sally's program makes cleaning the data files trivial - if she wants to clean the data again, she simply runs the program again.

## Reproducibility

Previously researchers focused on **replication** - can the results be duplicated in a new study with different data? In science it is difficult to replicate articles and research, in part because authors don't provide enough information to easily replicate experiments and studies. Institutional biases also exist against replication - no one wants to publish it, and authors don't like to have their results challenged.

**Reproducibility** is "the idea that data analyses, and more generally, scientific claims, are published with their data and software code so that others may verify the findings and build upon them."[^coursera] Scholars who implement reproducibility in their projects can quickly and easily reproduce the original results and trace back to determine how they were derived. This easily enables verification and replication, and allows the researcher to precisely replicate his or her analysis. This is extremely important when writing a paper, submiting it to a journal, then coming back months later for a revise and resubmit because you won't remember how all the code/analysis works together when completing your revisions.

Because Jane forgot how she initially filtered the data files, she cannot replicate her original results, much less update them with the new data. There is no way to definitively prove how she got her initial results. And even if Jane does remember, she still has to do the work of cleaning the data all over again. Sally's work is reproducible because she still has all the original data files. Any changes to the files, as well as analysis, are created in the programs she wrote. To reproduce her results, all she needs to do is run the programs again. Anyone who wishes to verify her results can implement her code to reproduce them.

## Version control

Research projects involve lots of edits and revisions, and not just in the final paper. Researchers make lots of individual decisions when writing programs and conducting analysis. Why filter this set of rows and not this other set? Do I compute traditional or robust standard errors?

To keep track of all of these decisions and modifications, you could save multiple copies of the same file. But this is bad for two reasons.

1. When do you decide to create a new version of the file? What do we name this file?
2. Why did you create this new version? How can we include this information in a short file name?

Many of you are probably familiar with cloud storage systems like Dropbox or Google Drive. Why not use those to track files in research projects? For one, multiple authors cannot simultaneously edit these files - how do you combine the changes? There is also no record of who made what changes, and you cannot keep annotations describing the changes and why you made them.

**Version control software** (VCS) allows us to track all these changes in a detailed and comprehensive manner without resorting to 50 different copies of a file floating around. VCS works by creating a **repository** on a computer or server which contains all files relevant to a project. Any time you want to modify a file or directory, you check it out. When you are finished, you check it back in. The VCS tracks all changes, when the changes were made, and who made the changes.

If you make a change and realize you don't want to keep it, you can rollback to a previous version of the repository - or even an individual file - without hassle because the VCS already contains a log of every change. VCS can be implemented locally on a single computer:

{{< figure src="https://git-scm.com/book/en/v2/book/01-introduction/images/local.png" caption="VCS on a local computer" >}}

Or in conjunction with remote servers to store backups of your repository:

{{< figure src="https://git-scm.com/book/en/v2/book/01-introduction/images/distributed.png" caption="VCS with a server" >}}

If Jane wanted to rollback to an earlier implementation of her linear regression model, she'd have to remember exactly what her settings were. However all Sally needs to do is use VCS when she revises her programs. Then to rollback to an earlier model formulation she just needs to find the earlier version of her program which generates that model.

## Documentation

Programs include **comments** which are ignored by the computer but are intended for humans reading the code to understand what it does. So if you decide to ignore frozen yogurt sales, you can include this comment in your code to explain why the program drops that column from the data.

{{% callout note %}}
Comments are the **what** - what is the program doing? Code is the **how** - how is the program going to do this?
{{% /callout %}}

Computer code should also be **self-documenting**. That is, the code should be comprehensible whenever possible. For example, if you are creating a scatterplot of the relationship between ice cream sales and crime, don't store it in your code as `graph`. Instead, give it an intelligible name that intuitively means something, such as `icecream_crime_scatterplot` or even `ic_crime_plot`. These records are included directly in the code and should be updated whenever the code is updated.

Comments are not just for other people reading your code, but also for yourself. The goal here is to future-proof your code. That is, future you should be able to open a program and understand what the code does. If you do not include comments and/or write the code in an interpretable way, you will forget how it works.


### Badly documented code

This is an example of badly documented code.


```r
library(tidyverse)
library(rtweet)
tml1 <- get_timeline("MeCookieMonster", 3000)
tml2 <- get_timeline("Grover", 3000)
tml3 <- get_timeline("elmo", 3000)
tml4 <- get_timeline("CountVonCount", 3000)
ts_plot(group_by(bind_rows(select(tml1, created_at), select(tml2, created_at), select(tml3, created_at), select(tml4, created_at), .id = "screen_name"), screen_name), by = "months")
```

* What does this program do?
* What are we using with the `ts_plot()` function?
* What does `3000` refer to?

This program, although it works, is entirely indecipherable unless you are the original author (and even then you may not fully understand it).

### Good code

This is a rewritten version of the previous program. Note that it does the exact same thing, but is much more comprehensible.[^ben]




```r
# get_to_sesame_street.R
# Program to retrieve recent tweets from Sesame Street characters

# load packages for data management and Twitter API
library(tidyverse)
library(rtweet)

# retrieve most recent 3000 tweets of best Sesame Street residents
cookie <- get_timeline(
  user = "MeCookieMonster",
  n = 3000
)

grover <- get_timeline(
  user = "Grover",
  n = 3000
)

elmo <- get_timeline(
  user = "elmo",
  n = 3000
)

count_von_count <- get_timeline(
  user = "CountVonCount",
  n = 3000
)

# combine, group by character, and plot weekly tweet frequency
bind_rows(
  `Cookie Monster` = cookie %>% select(created_at),
  Grover = grover %>% select(created_at),
  Elmo = elmo %>% select(created_at),
  `Count von Count` = count_von_count %>% select(created_at),
  .id = "screen_name"
) %>%
  group_by(screen_name) %>%
  ts_plot(by = "months")
```




<!--## Session Info


-->

[^rachel]: Hat tip to [Rachel Thomas](https://twitter.com/math_rachel/status/764931533383749632).
[^downey]: Downey, Allen. 2012. Think Python. 2nd ed.
[^stata]: Example drawn from [*Code and Data for the Social Sciences: A Practitioner's Guide*](https://people.stanford.edu/gentzkow/sites/default/files/codeanddata.pdf).
[^coursera]: [Coursera: Reproducible Research](https://www.coursera.org/learn/reproducible-research).
[^ben]: Credits: The content of this page is derived from the most part from Benjamin Soltoff's "Computing for the Social Sciences" course materials, licensed under the CC BY NC 4.0 Creative Commons License.
