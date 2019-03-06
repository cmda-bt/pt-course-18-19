<!--lint disable no-html-->

# Week 4: Configs & Requirements

## Table of Contents

*   [Comic](#comic)
*   [Slides](#slides)
*   [Assignments](#assignments)
*   [Homework](#homework)

## Comic

[![][comic-cover]][comic-link]

> GeoIP by [**@xkcd**][comic-author].

## Slides

*   [**Slides**][slides-lab]

## Assignments

### Linting (research)

*   **Research**
*   **Time**: 0:45h
*   **Goals**: subgoal 5

Take about 0:45h to investigate what 'linting' is: what is it used for, why is it useful and try to look for examples. 

* Linting is commonly used to enforce consistent 'code quality', what do we mean by that?
* What are common tools for 'linting'?
* How can you implement these tools in your own project?
* What are the difference between syntax and stylistic errors?

## Homework

### Linting (implementation)

*   **Homework**
*   **Time**: 3h
*   **Goals**: subgoal 5

Based on the research you conducted setup a (or multiple) linters in your own project. Ask yourself which tools are useful for your own project. If you're not sure which one to pick, the ones below are solid choices:

* [`eslint`](https://eslint.org/) - pluggable linting utility for JavaScript
* [`stylelint`](https://stylelint.io/) - modern linter that helps you avoid errors and enforce conventions in your styles
* [`prettier`](https://prettier.io/) - opinionated code formatter
* And so much [more](https://github.com/caramelomartins/awesome-linters#)

Think about what rules you are going to enforce. Most linters requires you to configure those on your own. You can use linters most linters as script in your `package.json` or as an `extension` in your editor.

> If you've configured a linter and want to use it in your editor, make sure you also install the corresponding extension!

### Extensions

*   **Homework**
*   **Time**: 2h
*   **Goals**: subgoal 5

Previously you've customized the look and feel of your command line. We are going to do the same thing with your code editor. Since you spend quite some time in there it's good to customize it to your own liking. If you are still using Brackets, this might be a good assignment to broaden your horizon or even switch to another code editor such as [`Atom`](https://atom.io/) or [`VS Code`](https://code.visualstudio.com/).

* Try a different color theme! Each editor come with some default options but you can also [browse through](http://color-themes.com/?view=index) lots of other community made ones.
    * In VS Code these are called [color themes](https://code.visualstudio.com/docs/getstarted/themes).
    * [Here](https://atom.io/themes) is a list for Atom, they are usually split between UI and syntax themes.
* Install some extensions to enhance functionality of your editor.
    * [VS Code marketplace](https://marketplace.visualstudio.com/vscode) and Atom [Packages](https://atom.io/packages) are the corresponding pages for extensions for both editors.
* Get the most out of your edidtor by tweaking your settings and getting to know the shorcuts. Take some time to tweak some settings and learn some keyboard shortcuts. You can read the [Flight Manual](https://flight-manual.atom.io/) for Atom or read the [docs](https://code.visualstudio.com/docs) for VS Code

> Wes and Scott (you might have taken one of their courses) have a good podcast called Syntax where they detail their setups. You can listen to [these episodes](https://syntax.fm/show/012/why-is-everyone-switching-to-vs-code) or look in the show notes for inspiration.

### Usability Test

*   **Homework**
*   **Time**: 1h
*   **Goals**: subgoal 5

You already started working on your interface. You might already have some sketches or written some views, partials or components with a templating engine. Collect feedback on your interface and Static HTML. Let other students test your interface and give you feedback.

[bugs]: readme.md#bugs

[comic-cover]: https://imgs.xkcd.com/comics/geoip.png

[comic-link]: https://xkcd.com/713/

[comic-author]: https://xkcd.com

[slides-lab]: https://docs.google.com/presentation/d/1Jaq86Wo5qQkVzeJX2ZY1JoL8T5Lvfq4A7hC01sLNjUM/edit?usp=sharing
