# js-doc
Insert JSDoc style comment easily in Emacs

## Installation
1. Put `js-doc.el` somewhere in your emacs load path.
2. Add a line below to your .emacs file:

```scheme
(require 'js-doc)
```

## Example
Paste the codes below into your configuration file and you:

1. insert function document by pressing `Ctrl + c, i`
2. insert `@tag` easily by pressing `@` in the JSDoc style comment

 If you want to see the tag description, just input the next command
   M-x js-doc-describe-tag

## Configuration
```scheme
(setq js-doc-mail-address "your email address"
      js-doc-author (format "your name <%s>" js-doc-mail-address)
      js-doc-url "url of your website"
      js-doc-license "license name")

 (add-hook 'js2-mode-hook
           (lambda ()
             (define-key js2-mode-map "\C-ci" 'js-doc-insert-function-doc)
             (define-key js2-mode-map "@" 'js-doc-insert-tag)))
```
