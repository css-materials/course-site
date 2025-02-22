---
date: "2024-09-29T00:00:00-05:00"
draft: false
weight: 40
title: "Configure Git"
toc: true
type: book
aliases: ["/git07.html", "/setup/git-configure/"]
---



To ensure minimal challenges using Git during the class, we want to configure Git now with some default settings: identify yourself and set up your cache credentials. **You only have to do this once per machine.**


{{% callout note %}}
If you are configuring Git on your own computer, before doing anything else run the following code in the R console to ensure you have the required packages installed (you do not need to do it if you use R Workbench):
```r
install.packages(c("usethis", "gitcreds", "gh"))
```
{{% /callout %}}

Follow the step-by-step written instructions in the tutorial below to set up Git. For a walkthrough of the setup process check out [this video demonstration](https://drive.google.com/file/d/1O_uiyzVHKJOfGxaEDZ3TWWwkUm2qZpl-/view?usp=sharing)


# Identify yourself

To track changes and attribute them to the correct user, we need to tell Git your name and email address. Go to the Console tab in R and run the code below by replacing `Sabrina Nardin` and `email@gmail.com` with **your name and email address**:
* Your name could be your GitHub username, or your actual first and last name
* Your email address must be the email address associated with your GitHub account

```r
library(usethis)
usethis::use_git_config(user.name = "Sabrina Nardin", user.email = "email@gmail.com")
```

To check that Git got your credentials, go to *Tools > Shell* and run the following command in the shell/terminal tab that opens up:

```r
git config --global --list
```


# Cache credentials

In order to push changes to GitHub, you need to authenticate yourself. That is, you need to prove you are the owner of your GitHub account. When you log in to GitHub.com from your browser, you provide your username and password to prove your identity. But when you want to push and pull from your computer, you cannot use this method. Instead, you will prove your identity using one of two methods:
1. Cache credentials for SSH (use this if you are using R Workbench)
2. Cache credentials for HTTPS


## 1. Cache credentials for SSH

{{% callout note %}}

If you are using the [RStudio Workbench](/setup/r-server/) for the class, you will need to use SSH. The server does not have the ability to cache your personal access token for HTTPS.

{{% /callout %}}

The Secure Shell Protocol (SSH) is a method for authenticating your identity when communicating with GitHub. While a password can eventually be cracked with a brute force attack, SSH keys are nearly impossible to decipher by brute force alone. Generating a key pair provides you with two long strings of characters: a public and a private key. You can place the public key on any server (like GitHub), and then unlock it by connecting to it with a client that already has the private key (your computer or RStudio Serve). When the two match up, the system unlocks without the need for a password.

On GitHub, the URL for SSH remotes looks like `git@github.com:<OWNER>/<REPO>.git`. Make sure you use this URL to create a project or clone a repository. If you accidentally use the HTTPS version, the operation will not work.

To create and store an SSH key pair, run the following code in the R Console:

```r
credentials::ssh_setup_github()
```

<!--
new line of command cis-ds
```r credentials::ssh_keygen() ```
-->

* It should say "No SSH key found. Generate one now?" Tell the computer yes
* You will see a long string of characters in the Console (that's your key!). You should be asked to open a browser now, tell the computer yes. Then go back to your Console: copy and paste the SSH key (the whole line of text, including the first words that should say "ssh-rsa") into the new browser window on GitHub. If you do not have a GitHub account, please register a free GitHub account before proceeding (see Lecture 1)
* Under "Title" give the key an informative title, something like `css-rstudio-server` or `css-rworkbench` to record the class and computer. Leave "Key type" as "Authentication Key" 
* Click the green button "Add SSH key". If you are prompted to clear the GitHub security procedures (e.g. authentication code, GitHub password, etc.) do so.
* You should now see your key saved on GitHub and you are done!


## 2. Cache credentials for HTTPS

{{% callout note %}}
If you are running R and Git on your personal computer, I recommend this method. However, if you are using R Workbench, please authenticate with the SSH method below
{{% /callout %}}

With this authentication method you will clone GitHub repositories using a regular HTTPS url like `https://github.com/<OWNER>/<REPO>.git`. You will need a *personal access token* (PAT) and use that as your credential for HTTPS operations.

To get a PAT, run this code from your R console:

```r
usethis::create_github_token(
  scopes = c("repo", "user", "gist", "workflow"),
  description = "RStudio Workbench"
)
```

This is a helper function that takes you to the web form to create a PAT.

- Give the PAT a description (e.g. "PAT for Computing for Information Science")
- Change the Expiration to 90 days. This ensures the PAT remains valid through the end of the course. You can also set the token to never expire, but GitHub will warn you this is not as secure as an expiring token.
- Leave the remaining options on the pre-filled form selected and click "Generate token". As the page says, you must *store this token somewhere*, because you'll never be able to see it again, once you leave that page or close the window. For now, you can copy it to your clipboard (we will save it in the next step).

If you lose or forget your PAT, just generate a new one.

In order to store your PAT so you don't have to reenter it every time you interact with Git, we need to run the following code:

```r
gitcreds::gitcreds_set()
```

When prompted, paste your PAT into the console and press return. Your credential should now be saved on your computer.

To confirm your PAT is saved, run the following code:

```r
gh::gh_whoami()

usethis::git_sitrep()
```

You should see output that provides information about your GitHub account.

Now that you have stored your PAT, you should not be asked to provide a username and password when you attempt to push to or pull from GitHub. It will just work! Hopefully.


# Acknowledgments


* This page is derived in part from ["UBC STAT 545A and 547M"](http://stat545.com), licensed under the [CC BY-NC 3.0 Creative Commons License](https://creativecommons.org/licenses/by-nc/3.0/).

* This page has been developed starting from Benjamin Soltoff’s “Computing for the Social Sciences” course materials, licensed under the CC BY-NC 4.0 Creative Commons License.
* [*Happy Git and GitHub for the useR*](https://happygitwithr.com/)


<!-- MORE ON CACHE CREDENTIALS 


## Why cache credentials?

As you have probably gathered by now, it will be annoying to enter your username and password each time you push changes to GitHub. It may even discourage you from pushing as frequently as you should. By storing your credentials on the computer, you won't have to authenticate yourself manually each time you push to GitHub, and your credentials will be stored in a secure manner.

{{% callout note %}}

As of January 2019, if you install Git using [these instructions](/setup/git/), it is possible that Git will use a credential helper provided by your operating system. That is, you may not need to do anything special in order to cache your GitHub username and password. Specifically, if you are on macOS or Windows, don’t do anything described here until you have actual proof that it’s necessary, i.e. that you have experienced repeated challenges for your username and password when attempting to push/pull to GitHub.

{{% /callout %}}

## Get a test repository

You need a functioning test Git repository. One that exists locally and remotely on GitHub, with the local repo tracking the remote. If you just setup [Git with GitHub](/setup/github/), you have a test repository. If you setup [Git to work within RStudio](/setup/git-with-rstudio/), you have a test repository. If you already deleted those repositories, set one of them back up again.

You may proceed when

* You have a test repo.
* You know where it lives on your local computer. Example:
    * `/home/benjamin/Github/myrepo`
* You know where it lives on GitHub. Example:
    * `https://github.com/bensoltoff/myrepo`
* You know local is tracking remote. In a [shell](/setup/shell/) with working directory set to the local Git repo, enter these commands:

```
benjamin-laptop:Github benjamin $ git remote -v
origin  https://github.com/bensoltoff/myrepo (fetch)
origin  https://github.com/bensoltoff/myrepo (push)

benjamin-laptop:Github benjamin $ git branch -vv
* main b8e03e3 [origin/main] line added locally
```

We want to see that fetch and push are set to remote URLs that point to your GitHub repo. We also want to see that your local main branch has your GitHub main branch as upstream remote. Gibberish? Just check that your output looks similar to this.

## Verify Git is up-to-date

In a shell, enter `git --version` and verify that you have 1.7.10 or newer. If you don't, update Git.

## Turn on the credential helper

### Windows

In the shell, enter `git config --global credential.helper wincred`

### Mac

Find out if the credential helper is already installed. In the shell, enter `git credential-osxkeychain`. You should see something like this: `Usage: git credential-osxkeychain <get|store|erase>`. If you do not, follow step 2 on the [GitHub help page](https://help.github.com/articles/caching-your-github-password-in-git/#platform-mac).

Once you’ve confirmed you have the credential helper, enter `git config --global credential.helper osxkeychain`.

### Linux

In the shell, enter `git config --global credential.helper 'cache --timeout=10000000'` to store your password for ten million seconds (that's roughly 16 weeks).

## Trigger a username/password challenge

Change a file in your local repo and commit it. Do that however you wish. Here are shell commands that will work:

```
echo "adding a line" >> README.md
git add -A
git commit -m "A commit from my local computer"
```

Now push!

```
git push -u origin main
```

One last time you will be asked for your username and password, which hopefully will be cached.

Now push AGAIN.

```
git push
```

You should NOT be asked for your username and password, instead you should see `Everything up-to-date`.

Rejoice and close the shell. From now on your "Push" button in RStudio will just work.

## More options: SSH

Secure Shell (SSH) is an alternative method for authenticating trusted computers without using a password. There are some benefits to this approach over HTTPS, however it is generally more complicated to initially set up. If you wish to use this approach, see [here](https://help.github.com/articles/generating-an-ssh-key/) for instructions on generating an SSH key and pairing it with your GitHub account.

## Acknowledgments


* This page is derived in part from ["UBC STAT 545A and 547M"](http://stat545.com), licensed under the [CC BY-NC 3.0 Creative Commons License](https://creativecommons.org/licenses/by-nc/3.0/).
* ["Chapter 10: Cache credentials for HTTPS" from Happy Git and GitHub for the useR](https://happygitwithr.com/credential-caching.html)

-->
