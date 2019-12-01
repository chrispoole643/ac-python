# Simple Python Completion Source for Auto-Complete

(This is old, but kept here in case it's of use later. Better to use
[lsp-mode][lsp] or similar now.)


## Installation

Setup [Auto-Complete](https://www.emacswiki.org/emacs/AutoComplete) in
the usual fashion, and make sure it gets loaded for python
buffers. Then, place [ac-python.el](./ac-python.el) in your load-path,
and add

```lisp
(require 'ac-python)
```

to your .emacs file (after loading Auto-Complete).


## Usage

Python symbols will be completed by Auto-Complete, once Emacs learns
about these symbols. This is the short-coming of the plugin, but it's
a small price to pay.

To teach Emacs about symbols in imported modules, Emacs needs to
execute the Python source. This can be accomplished with
`python-send-buffer` for example, often bound to `C-c C-c`. If a
python process is already running, this is essentially instantaneous.

See [this blog post][more] for more information.


[more]: https://chrispoole.com/project/ac-python
[lsp]: https://github.com/emacs-lsp/lsp-mode
