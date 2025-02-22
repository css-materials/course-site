---
date: "2022-09-26T00:00:00-05:00"
draft: false
weight: 20
title: "Access RStudio Workbench"
toc: true
type: book
aliases: ["/setup_server.html", "/setup/r-server/"]
---



This page provides a few definitions (R, RStudio, RStudio Workbench) and instructions to access RStudio Workbench (Option 1).

## R and RStudio

[R](https://www.r-project.org/) is an open-source programming. When people mention R, they might refer to the base R distribution or to its most popular IDE (Integrated Development Environment): RStudio. Most people do not use R in its bare distribution but through a IDE, which makes it easier to interact with R and write code. There are different IDEs that can be used with R, but the most popular is [RStudio](https://www.rstudio.com/products/RStudio/) and in this course we will use it. RStudio is open-source, expandable, and provides many useful tools and enhancements over the base R environment.

## RStudio Workbench

We will use “RStudio Workbench” throughout the course, which is the exact same thing as the regular R/RStudio but instead of being on your machine, it is online! 
In practice, rather than installing your own copy of R and RStudio, you can access R and RStudio remotely hosted on a server: the [Social Sciences Computing Services](https://sscs.uchicago.edu/) hosts RStudio Workbench for us. To use it, you will open RStudio in your web browser. All the processing and computation is done on a remote server. This means that all of the software is pre-configured for you and the setup is minimal.

The downside is that you only have access to this server for the duration of the class. If you intend to use R and RStudio in future classes/research projects, you will need to install and configure everything on your own computer after the course is completed.

## Accessing RStudio Workbench

1. Go to https://macss-r.uchicago.edu/ to login to the server. Save the link somewhere since you will be using it frequently
2. Use your [CNetID](https://uchicago.service-now.com/it?id=kb_article&kb=KB06000393) and password to login (this is the same username/password you use for other UChicago online services).
3. You're done. You should see a fresh RStudio window in your browser.

{{% callout note %}}

Only students in this course who have been approved by SSCS can access this server. If you cannot log on to the server, chances are that you have not yet been added to the server. Please, email me at nardin@uchicago.edu and we will get this fixed.

If you have problems with cVPN or the network, contact [ITS](https://its.uchicago.edu/)

{{% /callout %}}

## Testing RStudio Workbench

You should see something that looks like this:

{{< figure src="rstudio-server.png" caption="" >}}

The RStudio IDE is divided into 4 separate panes (one of which is hidden for now) which all serve specific functions. To make sure R and RStudio are setup correctly, type `x <- 5 + 2` into the *console* pane (the one on the left side of your screen) and execute it by pressing Enter/Return. You just created an object in R called `x`. Type `print(x)` into the console and press enter again. Your console should now contain the following output:


```r
x <- 5 + 2
print(x)
```

```
## [1] 7
```

## Acknowledgments


* This page is derived in part from ["UBC STAT 545A and 547M"](http://stat545.com), licensed under the [CC BY-NC 3.0 Creative Commons License](https://creativecommons.org/licenses/by-nc/3.0/).

* This page has been developed starting from Benjamin Soltoff’s “Computing for the Social Sciences” course materials, licensed under the CC BY-NC 4.0 Creative Commons License.
