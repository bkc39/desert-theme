# desert-theme

[![CI](https://github.com/bkc39/desert-theme/actions/workflows/ci.yml/badge.svg)](https://github.com/bkc39/desert-theme/actions/workflows/ci.yml)

A warm, earthy Emacs port of the classic **desert** colorscheme from Vim.

It aims to preserve the feel of the original:

- dark warm-gray background
- golden/yellow comments
- soft greens for strings
- sandy/orange accents for variables and constants
- gentle blue for function names and types

## Screenshot

<!-- Add a screenshot here, e.g.: -->
<!-- ![desert-theme screenshot](screenshot.png) -->

_Screenshot coming soon._

## Installation

### MELPA

Once available on [MELPA](https://melpa.org/), install with:

```
M-x package-install RET desert-theme RET
```

Then load it:

```elisp
(load-theme 'desert t)
```

### use-package

```elisp
(use-package desert-theme
  :config
  (load-theme 'desert t))
```

### straight.el / use-package

```elisp
(use-package desert-theme
  :straight (desert-theme
             :type git
             :host github
             :repo "bkc39/desert-theme")
  :config
  (load-theme 'desert t))
```

### Manual

Clone the repo and put it on your `custom-theme-load-path`:

```elisp
(add-to-list 'custom-theme-load-path "/path/to/desert-theme")
(load-theme 'desert t)
```

## Requirements

Emacs 27.1 or newer (the theme uses the `:extend` face attribute).

## Development

This package uses [Eask](https://emacs-eask.github.io/) for building and
linting. CI verifies that the theme byte-compiles and passes `checkdoc` and
`package-lint` on Emacs 27.1 through 30.1.

```sh
eask install-deps
eask compile        # byte-compile (warnings are errors)
eask lint checkdoc
eask lint package   # package-lint
```

## License

Released into the public domain under
[CC0 1.0 Universal](LICENSE).
