flymake-haskell-multi.el
========================

*Note: you probably want to use [flycheck](https://github.com/lunaryorn/flycheck) instead.*

An Emacs flymake handler for checking Haskell source code with both
`ghc` and [hlint][hlint]. If `ghc -Wall -fno-code` returns no errors,
`hlint` is run (if available). Warnings and errors output by both programs
will be displayed via flymake overlays in the source code.

This works via a small shell script, `haskell_multi`, which is bundled.

For a demonstration, see [this screencast](http://www.youtube.com/watch?v=aj7WF_Zm9zY).

Installation
=============

If you choose not to use one of the convenient packages in
[Melpa][melpa] and [Marmalade][marmalade], you'll need to add the
directory containing `flymake-haskell-multi.el` and the
`haskell_multi` script to your `load-path`, and then `(require
'flymake-haskell-multi)`. You'll also need to install
[flymake-easy](https://github.com/purcell/flymake-easy).

You should also install [hlint][hlint] and ensure it is on your `exec-path`.

Usage
=====

Add the following to your emacs init file:

    (require 'flymake-haskell-multi) ;; not needed if installed via package
    (add-hook 'haskell-mode-hook 'flymake-haskell-multi-load)


[marmalade]: http://marmalade-repo.org
[melpa]: http://melpa.org
[hlint]: http://community.haskell.org/~ndm/hlint/

<hr>

[💝 Support this project and my other Open Source work](https://www.patreon.com/sanityinc)

[💼 LinkedIn profile](https://uk.linkedin.com/in/stevepurcell)

[✍ sanityinc.com](http://www.sanityinc.com/)
