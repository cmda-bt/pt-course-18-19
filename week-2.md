<!--lint disable no-html-->

# Week 2: Registering & Functionalities

## Table of Contents

*   [Lab](#lab)
*   [Assignments](#assignments)

---

# Lab

#### Synopsis

*   **Date**: 05-02
*   [**Slides**][slides-lecture]
*   **Date**: 08-02 (BT 1) or 06-02 (BT 2 and BT 3)
*   [**Slides**][slides-lab]

#### Schedule

*   Recap
*   Huisstijl & persona
*   Registering ([**subgoal ..**][s..])
*   Functionalities ([**subgoal 1**][s1])
*   Job Stories

---

## Assignments

[![][comic-cover]][comic-link]

> DFS by [**@xkcd**][comic-author].

You’re expected to spend about 6 hours on assignments outside of class.
Submit your assignments by 3 a.m. the day of [lab 2][w2lab].

### Assignments Registering & Functionalities

---

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

### II. Run the Command Line

In this assignment you’ll learn the basics of the command line.

#### Synopsis

*   **Practice**
*   **Time**: 0:30h
*   **Goals**: [subgoal 1][s1]
*   **Due**: 3 a.m. the day of [lab 2][w2lab]

#### Tips

*   [Terminal Cheat Sheet for Mac](https://github.com/0nn0/terminal-mac-cheatsheet)
    (**cheat sheet**)
    — List of my most used commands and shortcuts in the terminal for Mac
*   Stuck?  See the [Bugs][] section of the course readme to find a list of
    troubleshooting tips

#### Step A

Create a directory on your computer, `run`.  In it, create a file `tutorial.sh`
and copy-paste the complete following document into it.

> ⚠️ If you are on Windows, make sure the select LF line endings (Unix) instead
> of CRLF (Windows) while saving the file.  In Atom, you can click on CRLF in
> the status bar and switch to LF.  In SublimeText, go to the View menu, and
> click Line Endings.

<details>
<summary><code>tutorial.sh</code> (click the arrow to expand)</summary>

```sh
#!/bin/bash

###
### Hi students! Please don’t change this file,
### run it with `bash tutorial.sh` instead.
###

function bold {
  printf "\\033[1m%s\\033[22m" "$1"
}

function green {
  printf "\\033[32m%s\\033[0m" "$1"
}

function red {
  printf "\\033[31m%s\\033[0m" "$1"
}

function yellow {
  printf "\\033[33m%s\\033[0m" "$1"
}

function intro {
  clear
  if [ -n "$username" ]; then
    echo "$(bold "Hi, $username! 👋")"
  else
    echo "$(bold "Hi! 👋")"
  fi
  echo "Follow this tutorial by running \`sh $currentScript\`.  $(yellow "Stuck")?  Use \`man\` (such"
  echo "as \`man ls\`) for help!"
  echo
  echo "$(bold "Results") ($(yellow "$ok")/14)"
  echo

  for index in $(seq 0 $ok); do
    case $index in
    0)
      echo "$(green "✓") $question0"
      ;;
    1)
      echo "$(green "✓") $question1"
      ;;
    2)
      echo "$(green "✓") $question2"
      ;;
    3)
      echo "$(green "✓") $question3:" $answer3
      ;;
    4)
      echo "$(green "✓") $question4:" $answer4
      ;;
    5)
      echo "$(green "✓") $question5"
      ;;
    6)
      echo "$(green "✓") $question6"
      ;;
    7)
      echo "$(green "✓") $question7:" $answer7
      ;;
    8)
      echo "$(green "✓") $question8:" $answer8
      ;;
    9)
      echo "$(green "✓") $question9"
      ;;
    10)
      echo "$(green "✓") $question10"
      ;;
    11)
      echo "$(green "✓") $question11:" $answer11
      ;;
    12)
      echo "$(green "✓") $question12"
      ;;
    13)
      echo "$(green "✓") $question13"
      ;;
    14)
      echo "$(green "✓") $question14"
      ;;
    esac
  done
}

###
### Questions
###

currentScript="$(basename "$0")"

typeset -i ok=0

question0="Directory"
question1="Username"
question2="Hello World"
question3="Where are we"
question4="Files"
question5="Add a file"
question6="Add a directory"
question7="Enter a directory"
question8="Exit a directory"
question9="Remove a file"
question10="Redirect"
question11="Print a file"
question12="Move a file"
question13="Copy a file"
question14="Append to file"

answer3=""
answer4=""
answer7=""
answer8=""
answer11=""

###
### Question 0: make a directory named `run`.
###

if [[ "$(basename "$(pwd)")" != "run" ]]; then
  intro
  echo "$(red "𐄂") Create a directory named \`run\`"
  echo
  echo "  $(bold "$(yellow "Make sure to change the current directory to \`run\` as well")")"
  exit 1
fi

###
### Question 1: Type your GitHub username.
###

intro
echo "○ $(yellow "$question1")"
echo

while true; do
  printf "Could you give us your GitHub username? Type here: "
  read -e username

  if [ -n "$username" ]; then
    code="$(base64 <<<"$username")"
    (( ok++ ))
    intro
    break
  fi

  echo
  echo "$(bold "$(yellow "Please try again")")"
  echo
done

###
### Question 2: print `hello world`.
###

echo "○ $(yellow "$question2")"
echo
echo "The next step is to print out something."

while true; do
  printf "Type the code needed to print out 'Hello World!': "
  read -e cmd

  if [[ "$cmd" == echo* ]]; then
    if [[ "$(eval "$cmd")" == "Hello World!" ]]; then
      (( ok++ ))
      intro
      break
    fi
  fi

  echo
  echo "$(bold "$(yellow "Hmm, that doesn’t seem right.  Make sure to use the proper casing and")")"
  echo "$(bold "$(yellow "don’t forget the exclamation mark!  Try again.")")"
  echo
done

###
### Question 3: Current working directory.
###

echo "○ $(yellow "$question3")"
echo
echo "The next step is to print where we are."

while true; do
  printf "Type the code needed to print out the current working directory: "
  read -e cmd

  if [[ "$cmd" == pwd* ]]; then
    answer3="$(eval "$cmd")"
    if [[ "$answer3" == "$(pwd)" ]]; then
      (( ok++ ))
      intro
      break
    fi
  fi

  echo
  echo "$(bold "$(yellow "Hmm, that doesn’t seem right. Try again.")")"
  echo
done

###
### Question 4: Files
###

echo "○ $(yellow "$question4")"
echo
echo "The next step is to print files."

while true; do
  printf "Type the code needed to print all files where we are: "
  read -e cmd

  if [[ "$cmd" == ls* ]]; then
    answer4="$(eval "$cmd")"
    if [[ "$answer4" == "$(ls)" ]]; then
      (( ok++ ))
      intro
      break
    fi
  fi

  echo
  echo "$(bold "$(yellow "Hmm, that doesn’t seem right. Try again.")")"
  echo "$(bold "$(yellow "Print out files *just* where we are.")")"
  echo
done

###
### Question 5: Create a file
###

echo "○ $(yellow "$question5")"
echo
echo "Now, add a file."

while true; do
  printf "Type the code needed to add a file \`index.txt\`: "
  read -e cmd

  if [[ "$cmd" == touch* ]]; then
    eval "$cmd"

    if [ -f "index.txt" ]; then
      (( ok++ ))
      intro
      break
    fi
  fi

  echo
  echo "$(bold "$(yellow "Hmm, that doesn’t seem right. Try again.")")"
  echo "$(bold "$(yellow "Hint: create \`index.txt\`, not another file.")")"
  echo
done

###
### Question 6: Create a directory
###

echo "○ $(yellow "$question6")"
echo
echo "Next up, add a directory."

while true; do
  printf "Type the code needed to add a directory \`doc\`: "
  read -e cmd

  if [[ "$cmd" == mkdir* ]]; then
    eval "$cmd"

    if [ -d "doc" ]; then
      (( ok++ ))
      intro
      break
    fi
  fi

  echo
  echo "$(bold "$(yellow "Hmm, that doesn’t seem right. Try again.")")"
  echo "$(bold "$(yellow "Hint: create \`doc\`, not another directory.")")"
  echo
done

###
### Question 7: Change directories
###

currentDirectory="$(pwd)"

echo "○ $(yellow "$question7")"
echo
echo "And now, change directories."

while true; do
  printf "Type the code needed to enter \`doc\`: "
  read -e cmd

  if [[ "$cmd" == cd* ]]; then
    eval "$cmd"

    if [[ "$(basename "$(pwd)")" == "doc" ]]; then
      answer7="$(pwd)"
      (( ok++ ))
      intro
      break
    fi
  fi

  # Restore place we were at, for people that cd to a wrong place.
  cd "$currentDirectory" || exit
  echo
  echo "$(bold "$(yellow "Hmm, that doesn’t seem right. Try again.")")"
  echo "$(bold "$(yellow "Hint: Change directories.")")"
  echo
done

###
### Question 8: Exit directories
###

docDirectory="$(pwd)"

echo "○ $(yellow "$question8")"
echo
echo "Next, exit that directory."

while true; do
  printf "Type the code needed to exit \`doc\`: "
  read -e cmd

  if [[ "$cmd" == cd* ]]; then
    eval "$cmd"

    if [[ "$(basename "$(pwd)")" == "run" ]]; then
      answer8="$(pwd)"
      (( ok++ ))
      intro
      break
    fi
  fi

  # Restore place we were at, for people that cd to a wrong place.
  cd "$docDirectory" || exit
  echo
  echo "$(bold "$(yellow "Hmm, that doesn’t seem right. Try again.")")"
  echo "$(bold "$(yellow "Hint: . refers to this directory, and .. to it’s parent.")")"
  echo
done

###
### Question 9: Remove a file
###

echo "○ $(yellow "$question9")"
echo
echo "Now, we’re going to remove the files and directories we just created."

while true; do
  echo "There are currently some files in this directory, here’s what \`ls\` produces:"
  echo
  echo "$(ls | sed "/^$currentScript$/d")"
  echo
  printf "Type the code needed to remove one of the files until everything is gone: "
  read -e cmd

  if [[ "$cmd" == rm* ]]; then
    eval "$cmd"

    if [[ "$(ls)" == "$currentScript" ]]; then
      (( ok++ ))
      intro
      break
    fi
  fi

  echo
  echo "$(bold "$(yellow "Not yet done! (note: use \`-r\` to remove directories)")")"
  echo
done

###
### Question 10: Redirect to a file
###

echo "○ $(yellow "$question10")"
echo
echo "Now, create a file with some content in it."
echo

while true; do
  echo "Could you add the text 'Alpha' to a file \`foo.txt\` using the \`>\` operator?"
  echo
  printf "Type the code needed to echo 'Alpha' into \`foo.txt\`: "
  read -e cmd

  if [[ "$cmd" == echo* ]]; then
    eval "$cmd"
    value="$(cat foo.txt)"

    if [ "$value" == "Alpha" ]; then
      (( ok++ ))
      intro
      break
    fi
  fi

  echo
  echo "$(bold "$(yellow "Don’t forget to use echo and >.")")"
  echo
done

###
### Question 11: Print a file
###

echo "○ $(yellow "$question11")"
echo
echo "Next, print a file."
echo

while true; do
  printf "Type code needed to $(bold "print") out \`foo.txt\`: "
  read -e cmd

  if [[ "$cmd" == cat* ]]; then
    answer11="$(eval "$cmd")"

    if [ "$answer11" == "Alpha" ]; then
      (( ok++ ))
      intro
      break
    fi
  fi

  echo
  echo "$(bold "$(yellow "Tip: you actually want to concatenate the file.")")"
  echo
done

###
### Question 12: Move a file
###

echo "○ $(yellow "$question12")"
echo
echo "Now, rename \`foo.txt\` to \`bar.txt\` (aka $(bold "move"))?"
echo

while true; do
  echo "Here’s what \`ls\` currently produces:"
  echo
  echo "$(ls | sed "/^$currentScript$/d")"
  echo
  printf "Type the code needed to $(bold "move") \`foo.txt\` to \`bar.txt\`: "
  read -e cmd

  if [[ "$cmd" == mv* ]]; then
    eval "$cmd"

    if [ -f "bar.txt" ]; then
      (( ok++ ))
      intro
      break
    fi
  fi

  echo
  echo "$(bold "$(yellow "Tip: Moving a file is the same as renaming it.")")"
  echo
done

###
### Question 13: Copy a file
###

echo "○ $(yellow "$question13")"
echo
echo "Next, could you $(bold "copy") \`bar.txt\` to \`baz.txt\`?"
echo

while true; do
  echo "Here’s what \`ls\` currently produces:"
  echo
  echo "$(ls | sed "/^$currentScript$/d")"
  echo
  printf "Type the code needed to $(bold "copy") \`bar.txt\` to \`baz.txt\`: "
  read -e cmd

  if [[ "$cmd" == cp* ]]; then
    eval "$cmd"

    if [ -f "baz.txt" ]; then
      (( ok++ ))
      intro
      break
    fi
  fi

  echo
  echo "$(bold "$(yellow "Not yet done!")")"
  echo
done

###
### Question 14: Append to a file
###

echo "○ $(yellow "$question14")"
echo
echo "Previously, we added 'Alpha' to \`foo.txt\`, but then renamed it to \`bar.txt\`."
echo "Then we copied \`bar.txt\` to \`baz.txt\`.  We now have two files, with the same contents."
echo
echo "For the final question, could you append 'Bravo' to \`baz.txt\`?"

while true; do
  echo "Here’s what \`cat baz.txt\` currently produces:"
  echo
  echo "$(cat baz.txt)"
  echo
  printf "Type the code needed to $(bold "append") 'Bravo' to \`baz.txt\`: "
  read -e cmd

  if [[ "$cmd" == echo* ]]; then
    eval "$cmd"
    value="$(cat baz.txt | tail -n 1)"
    echo "Value: .$value."

    if [ "$value" == "Bravo" ]; then
      (( ok++ ))
      break
    fi
  fi

  echo
  echo "$(bold "$(yellow "Don’t forget to use echo and >>.")")"
  echo
done

###
### Done!
###

clear
echo "$(bold "Hi, $username! 👋")"
echo "All done!  You’re now ready to continue with the steps found on GitHub."
echo
echo "You'll need this code:"
echo
echo "  $(bold "$code")"
```

</details>

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
Create an issue on our [GitHub issue tracker][run-issue].
In it, include the **code** you were given.

#### Extra resources

*   [Learn Enough Command Line to Be Dangerous](https://www.learnenough.com/command-line-tutorial)
*   [tldr](https://github.com/tldr-pages/tldr)
*   [thefuck](https://github.com/nvbn/thefuck#readme)

---


### V. Profile

In this assignment you’ll apply your newfound command line, Git, GitHub, and
Markdown skills.

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
    
---

#### Description

> **Warning**: Don’t blindly use someones code.  Copy-paste code only if you
> know what it does.  Dotfiles are often very personal: they are often not what
> _you_ want but they can serve as inspiration.

In this course, you’ll find yourself staring at that black screen with green
letters a lot.
You’ll type the same commands over and over again.
As you’ll spend so much time there, it makes sense to make the command line
more useful, and prettier.

---