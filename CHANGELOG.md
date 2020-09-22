# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2020-08-12
### Added
- Indentation for Twig code blocks.
- Snippets for commonly used Twig blocks.
- The main syntax file along with syntax tests for the scopes.
- Auto completions for builtin tags, filters, tests and functions. 
- Abiility to use <kbd>ctrl + /</kbd> for Twig line comments & <kbd>ctrl + shift + /</kbd> for block comments.

## [1.0.1] - 2020-08-17
### Changed
- Comments in Twig (`{# #}`) are now triggered by <kbd>ctrl + /</kbd> or <kbd>ctrl + shift + /</kbd>. Removed the erroneous behavior where <kbd>ctrl + /</kbd> would trigger adding `##` at the beginning of a line (Mistaken for a line comment).

### Removed
- <kbd>ctrl + /</kbd> no longer adds `##` to the beginning of a line.

## [1.0.2] - 2020-08-22
### Fixed
- The base scope is now changed from `text.twig` to `text.html.twig`.
- Fixed regex modifiers breaking the syntax highlighting.
- Fixed operators & language constants not being scoped in data structures.

## [1.0.3] - 2020-09-22
### Fixed
- Updated numeric literals to having the `meta.number` scopes.
- Fixed scoping for the `endif` & `endfor` tags
- Removed the non needed settings file.