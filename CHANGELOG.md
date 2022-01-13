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

## [1.0.4] - 2021-05-12
### Fixed
- Cleaned up the syntax definition a bit and added more tests.
- Ternary operators not highlighting.
- Import statements not getting highlighted.
- More specific language constant scopes.
- Quoted string escapes not highlighting.
- Better scoping of builtin tests.

### Added
- Additional keybindings for interpolation & to come out of empty statements/expression blocks.

## [1.0.5] - 2021-05-24
### Removed
- Keybindings to come out of empty statements/expression blocks.

## [1.0.6] - 2021-10-29
### Removed
- Regex highlighting in strings.

## [2.0.0] - 2022-01-
### Added
- Syntax now uses inheritance to provide HTML highlighting. As an end user, there should be no difference
at all, but using inheritance should significantly reduce syntax & regex cache size on disk, offerring
improved performance.
- Better test coverage for indentation using indentation tests.
- All of the completion files are now updated to use kind, annotation & details.
- Added support for highlighting `cache` tags.
- Added command palette entries for opening documentation and keybindings.
- Added CI for running syntax tests via GitHub Actions.
