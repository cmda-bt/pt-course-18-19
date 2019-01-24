# Week 2: Registering & Functionalities

## Table of Contents

*   [Comic](#comic)
*   [Slides](#slides)
*   [Assignments](#assignments)
*   [Homework](#homework)


## Comic

[![][comic-cover]][comic-link]

> DFS by [**@xkcd**][comic-author].

## Slides

*   [**Slides**][slides-lab]

## Assignments

### Run the Command Line

In this assignment you’ll learn the basics of the command line.

#### Synopsis

*   **Practice**
*   **Time**: 0:30h
*   **Goals**: subgoal 1
*   **Due**: before lab 3 [w3lab]

#### Step A

Create a directory on your computer, `run`.  In it, create a file `tutorial.sh`
and copy-paste the code from the Gist into it: 

[**`tutorial.sh gist`**](https://gist.github.com/dandevri/9568a8dff8f572a0ea67627445aca5b2)

> ⚠️ If you are on Windows, make sure the select LF line endings (Unix) instead
> of CRLF (Windows) while saving the file.  In Atom, you can click on CRLF in
> the status bar and switch to LF.  In SublimeText, go to the View menu, and
> click Line Endings.


* * *

In your terminal, go to the `run` directory and enter it (**hint**: use the
`cd` command to “change directories”).

If you now run `ls` (to print out files) in the directory, you should see the
tutorial:

```sh
$ ls
# tutorial.sh
```

Now, run the tutorial with `bash tutorial.sh`:

```sh
$ bash tutorial.sh
# Hi! 👋
# Follow this tutorial by running `bash tutorial.sh`.  Stuck?  Use `man` (such
# as `man ls`) in another tab for help!
#
# Results (0/14)
# …
```

This tutorial is interactive.  Answer any questions it asks you, until it sends
you back here.

#### Step B

Sweet!  Welcome back!  If you completed the tutorial, you were given a code.
Now we’re going to hand in that code to mark your assignment as complete.
Create an issue on our [GitHub issue tracker][issues].
In it, include the **code** you were given.

#### Tips

*   [Terminal Cheat Sheet for Mac](https://github.com/0nn0/terminal-mac-cheatsheet)
    (**cheat sheet**)
    — List of my most used commands and shortcuts in the terminal for Mac
*   Stuck?  See the [Bugs][] section of the course readme to find a list of
    troubleshooting tips

#### Extra resources

*   [Learn Enough Command Line to Be Dangerous](https://www.learnenough.com/command-line-tutorial)
*   [tldr](https://github.com/tldr-pages/tldr)
*   [thefuck](https://github.com/nvbn/thefuck#readme)

---

### Homework

### I. Profile (optional)

> **Optional**: This is a very cool assignment but it can be pretty hard /vague and isn't necessary to get further in the course. Only do this if you feel comfortable and want to do some advanced CLI things. 

#### Synopsis

*   **Homework**
*   **Time**: 3:45h
*   **Goals**: [subgoal 1][s1], [subgoal 2][s2], [subgoal 3][s3], and
    [subgoal 4][s4]
*   **Due**: 3 a.m. the day of [lab 2][w2lab]

#### Tips

*   [The Perfect Web Development Setup for OS X](https://github.com/jonathanong/osx-webdev-setup)
    (**article**)
*   [Introduction to Useful Bash Aliases and Functions](https://www.digitalocean.com/community/tutorials/an-introduction-to-useful-bash-aliases-and-functions)
    (**article**)
*   [dotfiles](https://dotfiles.github.io)
    (**article**)
    — Unofficial guide to dotfiles on GitHub
*   [Awesome dotfiles](https://github.com/webpro/awesome-dotfiles)
    (**article**)
    — Curated list of dotfiles resources
*   Stuck?  See the [Bugs][] section of the course readme to find a list of
    troubleshooting tips

#### Description

> **Warning**: Don’t blindly use someones code.  Copy-paste code only if you
> know what it does.  Dotfiles are often very personal: they are often not what
> _you_ want but they can serve as inspiration.

In this course, you’ll find yourself staring at that black screen with green
letters a lot.
You’ll type the same commands over and over again.
As you’ll spend so much time there, it makes sense to make the command line
more useful, and prettier.

In this assignment you’ll customise your command line by changing a config file.
The file in question, called your profile, is often named `.bash_profile`,
`.profile`, or `.bashrc`, depending on your operating system.
To find the file you need to edit, go to your root directory (`cd ~`) and print
out hidden files there (`ls -a`).
If one of the previously mentioned files exists, you’re supposed to edit that.
If none of the them do, you can create a `.bash_profile` in your home directory
and use that.
If multiple files exist, open each and inspect them to find out which one you
should edit.

For this assignment:

*   Add aliases (for example, I have `alias ..="cd .."` set up)
*   Modify your prompt (for example, I have `PS1="🚀 \$(basename \$(pwd))"` set
    up)
*   Add a welcome message, such as the weather with `curl wttr.in/Amsterdam?0q`
    (see `curl wttr.in/:help` for more info) or [cowsay][]
*   And add other configuration you see fit

…in your profile.

See the aforementioned extra resources for tips to get started.
You’re expected to review a lot of existing examples, and do a lot of searching
online.
You can change other files, such as `.gitconfig`, `.curlrc` or `.vimrc`, if you
feel like it.
Make sure to document anything you add with comments (`#` starts a line comment
in Bash).

Hand in your project by creating a new repository on GitHub:
`username/dotfiles` (in my case `dandevri/dotfiles`).

In your repository, include the changed and added files.
Also include a `readme.md`, documenting how to install your config files, what
they do, and who you are.
For example, something like [this one by **@holman**](https://github.com/holman/dotfiles#readme).

### II. Branding Research

*   Registering 
*   Functionalities
*   Job Stories

#### Methods
*   [Competitive Analyses](http://cmdmethods.nl/cards/library/competitive-analysis)

### Hand in

1. **Pages:**  
Create a [page](https://guides.github.com/features/wikis/#adding-pages) for this week or section of your research on your [GitHub Wiki](https://guides.github.com/features/wikis/#creating-your-wiki). 

1. **Push your changes:**  
Hand in your research in your repository on GitHub under your username.

[bugs]: readme.md#bugs

[inspiration-cover]: images/hackertyper.png

[inspiration-link]: http://hackertyper.net

[inspiration-author]: https://github.com/duiker101

[comic-cover]: https://imgs.xkcd.com/comics/dfs.png

[comic-link]: https://xkcd.com/761/

[comic-author]: https://xkcd.com

[refresh]: readme.md#resources-to-refresh-your-memory

[slides-lecture]: https://docs.google.com/presentation/d/1iozO2yIjCPoMztV8td0h1MEoM2O0VjmLzzMI0xfSTDg/edit?usp=sharing

[slides-lab]: https://docs.google.com/presentation/d/1FQrPU-T4j4xChCuUekXQPxs0DPYw-TRRTbV7IPJ9Tbk/edit?usp=sharing

[w2lab]: week-2.md#lab

[markup-cover]: images/note.jpg

[markup-cover-source]: https://unsplash.com/photos/Hb6uWq0i4MI

[markup-cover-author]: https://unsplash.com/@climatereality

[md-tutorial]: https://www.markdowntutorial.com

[markup-issue]: https://github.com/cmda-be/course-17-18/issues/new?title=Markup%20assignment&labels=week-1%2Cweek-1%3Amarkup

[run-cover]: images/run.jpg

[run-cover-source]: https://unsplash.com/photos/Zp-wTck-3Zw

[run-cover-author]: https://unsplash.com/@anniespratt

[run-issue]: https://github.com/cmda-be/course-17-18/issues/new?title=Run%20assignment&labels=week-1%2Cweek-1%3Arun

[try-git-cover]: images/try.jpg

[try-git-cover-source]: https://unsplash.com/photos/xceMsVvxcd4

[try-git-cover-author]: https://unsplash.com/@martinceralde

[try-git]: https://try.github.io

[try-git-issue]: https://github.com/cmda-be/course-17-18/issues/new?title=Try%20Git%20assignment&labels=week-1%2Cweek-1%3Atry-git

[octocat-cover]: images/octocat.jpg

[octocat-cover-source]: https://unsplash.com/photos/Bb_X4JgSqIM

[octocat-cover-author]: https://unsplash.com/@brina_blum

[octocat-intro-to-github]: https://services.github.com/on-demand/intro-to-github/

[octocat-github-cli]: https://services.github.com/on-demand/github-cli/

[octocat-issue]: https://github.com/cmda-be/course-17-18/issues/new?title=Octocat%20assignment&labels=week-1%2Cweek-1%3Aoctocat

[profile-cover]: images/profile.jpg

[profile-cover-source]: https://unsplash.com/photos/HFkTGu30w5E

[profile-cover-author]: https://unsplash.com/@oliver_photographer

[profile-issue]: https://github.com/cmda-be/course-17-18/issues/new?title=Profile%20assignment&labels=week-1%2Cweek-1%3Aprofile

[s1]: readme.md#subgoal-1

[s2]: readme.md#subgoal-2

[s3]: readme.md#subgoal-3

[s4]: readme.md#subgoal-4

[moodle-be]: https://moodle.cmd.hva.nl/course/view.php?id=431

[cowsay]: https://github.com/piuccio/cowsay

[issues]: https://github.com/cmda-bt/pt-course-18-19/issues/new/choose