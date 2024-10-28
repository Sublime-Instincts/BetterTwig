# Twig

![LICENSE](https://img.shields.io/badge/LICENSE-MIT-green?style=for-the-badge) ![Sublime Text](https://img.shields.io/badge/ST-Build%204142+-orange?style=for-the-badge&logo=sublime-text) ![Tag](https://img.shields.io/github/v/tag/Sublime-Instincts/BetterTwig?style=for-the-badge&logo=github&sort=semver) ![Downloads](https://img.shields.io/packagecontrol/dt/Twig?style=for-the-badge)
![Syntax tests](https://img.shields.io/github/actions/workflow/status/Sublime-Instincts/BetterTwig/syntax_test.yml?color=green&label=Syntax%20Tests&logo=github&logoColor=white&style=for-the-badge)

A Sublime Text package that offers enhanced syntax highlighting, snippets, completions and much more for PHP [Twig](https://twig.symfony.com/) templates. Read more for the full documentation.

## Features

- Indentation for code blocks.
- Snippets for common code blocks.
- Key bindings to make your life easier.
- Enhanced syntax highlighting for Twig templates.
- Autocompletions for built in tags, filters, functions, tests & loop variables.

## Installation

### Package Control
Install Twig via [Package Control](https://packagecontrol.io/). Once you have Package Control setup in Sublime Text, open the command palette and search for `Package Control: Install Package`. Search for `Twig`. There should be a package with the URL as https://github.com/Sublime-Instincts/BetterTwig. Install it. 

Package Control will take care for of automatically updating the package for you if there are new releases.

### Manual installation
In Sublime Text open the Preferences > Browse Packages menu item. In the Packages directory you should now see, clone this repository in a new directory called "Twig".

## Documentation

### How to use this package ?

By default, this package supports the following Twig extensions,

1. `.twig`
2. `.htm.twig`
3. `.html.twig`

Since a user can have more than one templating language package installed, this package doesn't support `.html` directly. To get highlighting for `.html` files with Twig code and all the other features this package provides, you can follow any of the two approaches given below 

1. Go to the bottom right status bar item that displays information on current syntax and click on that when the currently open file is any `.html` file. From there go to `Open all with current extensions as ...` and scroll to select `HTML (Twig)`. You should now be good to go.

2. When the currently open file is a `.twig` file, from the main menu, go to `Preferences -> Settings -- Syntax Specific`. This should open a 2 column new window, with the default settings on the right and a user settings on the left. In the user settings, add the following, save & close.

```json
{
    "extensions": [
        ".html"
    ]
}
```

### Key bindings

- The key bindings are configured so that pressing <kbd>shift + {</kbd> **twice** will automatically add spaces on both sides for the inner brace expression block & place the cursor in the center, like so `{{ | }}`.
- Similarly, pressing <kbd>shift + %</kbd> within `{}` will add spaces on both sides of the inner `%` like so `{% | %}`
- Use <kbd>ctrl + /</kbd> or <kbd>ctrl + shift + /</kbd> for Twig comments (`{# This is a Twig comment #}`)
- Use <kbd>#</kbd> within strings, to get the interpolation expression, like so `#{|}`.

### Snippets

Basic snippets for each keyword are provided to create expressions without bothering with `{%  %}`.

|  **Tab Trigger**  | **Twig Tag**
|-------------------|-----------------------
| `autoescape`      |  `{% autoescape %}`
| `endautoescape`   | `{% endautoescape %}`
|       ...         |          ...

Prefixed with `b` basic snippets for most common control structures are provided.

|  **Tab Trigger**  |         **Twig Code Block**
|-------------------|--------------------------------------
| `bautoescape`     | `{% autoescape %}{% endautoescape %}`
| `bblock`          |      `{% block %}{% endblock %}`
| `bembed`          |      `{% embed %}{% endembed %}`
| `bextends`        |           `{% extends %}`
| `bfor`            |        `{% for %}{% endfor %}`
| `bif`             |         `{% if %}{% endif %}`
| `bifelse`         |    `{% if %}{% else %}{% endif %}`
| `bmacro`          |      `{% macro %}{% endmacro %}`
| `bsandbox`        |    `{% sandbox %}{% endsandbox %}`
| `bverbatim`       |   `{% verbatim %}{% endverbatim %}`
| `bwith`           |       `{% with %}{% endwith %}`

For more, please follow the official documentation on [snippets](https://www.sublimetext.com/docs/completions.html#snippets) to create your own.

Or use [SnippetMaker](https://packagecontrol.io/packages/SnippetMaker) for convenience.

If you want to ignore the snippets that are provided by default, you can use the `ignored_snippets` setting.

| ignored snippets | values
|------------------|--------------------------------------
| all              | `"Twig/Snippets/*"`
| blocks           | `"Twig/Snippets/blocks"`
| expressions      | `"Twig/Snippets/expressions"`
| tags             | `"Twig/Snippets/tags"`

#### Example

To only keep tag snippets...

```json
{
    "ignored_snippets": [
        "Twig/Snippets/blocks",
        "Twig/Snippets/expressions",
    ],
}
```

## Reporting issues.

There is always scope for improvements, so please do report any bug(s) that you encounter.

Please follow the issue template that has been setup while reporting any bug(s) (So as to stay as organised as possible).

Use the [Twig playground](https://twigfiddle.com/) if you want to share a particular snippet of template while creating a specific issue.
