---
date: "2022-09-25T00:00:00-05:00"
draft: false
weight: 50
title: "How to ask for help"
toc: true
type: book
aliases: "/hw00_asking_questions.html"
---



You will stumble in this class, you will get confused, not understand how to perform a task, not understand why your code is generating an error. But as Alfred so helpfully points out to Bruce Wayne, do not fall to pieces when you fail. Instead, learn to pick yourself up, recover, and learn from the experience. Consider this a lesson not only for this class, but graduate school in general.

We will follow the **15 minute rule** in this class.[^rachel] If you encounter a problem in your assignments, spend 15 minutes troubleshooting the problem on your own. Make use of [Google](https://www.google.com) and [StackOverflow](http://stackoverflow.com/) to resolve the error. However, if after 15 minutes you still cannot solve the problem, ask for help to the instructional staff and your peers.

Asking questions is an important part of this class. Questions should be posted to [Ed Discussion](https://edstem.org/us/courses/29905/discussion/) in the appropriate category. Here are some **tips** you should always follow when posting questions.

## Introduce the problem with an informative title

* Bad title: "I need help!"
* Good title: "Getting a 'file not found error' when importing scotus.csv"

Be specific with your title. It should be brief, but also informative so that when others are looking at it (and they have a similar error and/or solution), they can easily find it.

## Summarize the problem

Introduce the problem you are having. Include what task you are trying to perform, pertinent error messages, and any solutions you've already attempted. This helps us narrow down and troubleshoot your problem.

## Include a reproducible example

Including a minimal, complete, and verifiable example (see [here](http://stackoverflow.com/help/mcve)) of the code you are using greatly helps us resolve your problem. You don't need to copy all the code from your program into the comment, but include enough code that we can run it successfully **until the point at which the error occurs**.

Make sure you have pushed your recent commits to the GitHub repo. If it is up-to-date, we can look in or clone your repo to our machines to replicate the problem.

## Format your code snippets with `reprex` (optional but encouraged)

The [`reprex`](http://reprex.tidyverse.org/) package allows you to generate reproducible examples that are easily shared on GitHub with all the proper formatting and syntax. Install it by running the following command from the console:

```r
install.packages("reprex")
```

To use it, copy your code onto your clipboard (e.g. select the code and **Ctrl + C** or **⌘ + C**). For example, copy this demonstration code to your clipboard:






```
library(tidyverse)
count(diamonds, colour)
```

Then run `reprex()` from the console, where the default target venue is GitHub:


```r
reprex()
```

A nicely rendered HTML preview will display in RStudio's Viewer (if you're in RStudio) or your default browser otherwise.

{{< figure src="reprex-output.png" caption="Output of `reprex()`" >}}

The relevant bit of GitHub-flavored Markdown is ready to be pasted from your clipboard:


````
``` r
library(tidyverse)
count(diamonds, colour)
#> Error in `group_by()`:
#> ! Must group by variables found in `.data`.
#> x Column `colour` is not found.

#> Backtrace:
#>     x
#>  1. +-dplyr::count(diamonds, colour)
#>  2. \-dplyr:::count.data.frame(diamonds, colour)
#>  3.   +-dplyr::group_by(x, ..., .add = TRUE, .drop = .drop)
#>  4.   \-dplyr:::group_by.data.frame(x, ..., .add = TRUE, .drop = .drop)
#>  5.     \-dplyr::group_by_prepare(.data, ..., .add = .add, caller_env = caller_env())
#>  6.       \-rlang::abort(bullets, call = error_call)
```

<sup>Created on 2023-09-21 with [reprex v2.0.2](https://reprex.tidyverse.org)</sup>
````

Here's what that Markdown would look like rendered in a GitHub issue:


``` r
library(tidyverse)
count(diamonds, colour)
#> Error in `group_by()`:
#> ! Must group by variables found in `.data`.
#> x Column `colour` is not found.

#> Backtrace:
#>     x
#>  1. +-dplyr::count(diamonds, colour)
#>  2. \-dplyr:::count.data.frame(diamonds, colour)
#>  3.   +-dplyr::group_by(x, ..., .add = TRUE, .drop = .drop)
#>  4.   \-dplyr:::group_by.data.frame(x, ..., .add = TRUE, .drop = .drop)
#>  5.     \-dplyr::group_by_prepare(.data, ..., .add = .add, caller_env = caller_env())
#>  6.       \-rlang::abort(bullets, call = error_call)
```

<sup>Created on 2023-09-21 with [reprex v2.0.2](https://reprex.tidyverse.org)</sup>

Anyone else can copy, paste, and run this immediately. The nice thing is that if your script also produces images or graphs (probably using `ggplot()`) these images are automatically uploaded and included in the issue.

Note: to ensure your example is a reproducible example, you need to make sure to load all necessary packages and data objects at the top of your copied code. This may involve opening a new tab in the editor panel and writing a short version of the script that only includes the essentials, then copying that script to the clipboard and `reprex()` it.




## Include your `session_info()`

Sometimes problems are caused by using older or incompatible versions of packages. The `session_info()` function in the `sessioninfo` library will print a list of all active packages and their respective versions. Include this in your post so we know which versions of packages you are using by setting `si = TRUE` in the `reprex()` function, like this: `reprex(si = TRUE)`.

## Post your solution

Once you have solved the problem (either by yourself or with the help of an instructor/classmate), **post the solution**. This let's us know that you have fixed the issue AND if anyone else encounters a similar error, they can refer to your solution to fix their problem.

## Acknowledgments

* ["How do I ask a good question?" StackOverflow.com](http://stackoverflow.com/help/how-to-ask)
* ["How to Ask Programming Questions," ProPublica.com](https://www.propublica.org/nerds/item/how-to-ask-programming-questions)

* This page has been developed starting from Benjamin Soltoff’s “Computing for the Social Sciences” course materials, licensed under the CC BY-NC 4.0 Creative Commons License.
