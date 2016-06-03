============
 dmacro.el
============

dmacro is a suport macro tools.

Install
========

Download from GitHub::

  $ git clone https://github.com/masui/DynamicMacro.git ~/.emacs.d/site-lisp/dmacro

Add belon in your emacs config file (``~/.emacs`` or ``~/.emacs.d/init.el``)::

  (add-to-list 'load-path "~/.emacs.d/site-lisp/dmacro")
  (defconst *dmacro-key* "\C-t" "repeat key")
  (load "~/.emacs.d/private/site-lisp/dmacro.el")
  (global-set-key *dmacro-key* 'dmacro-exec)
  (autoload 'dmacro-exec "dmacro" nil t)
  (require 'dmacro)

Usage
=====

For example, if you type

.. code-block::

   abcabc

and press "\C-t"(dmacro-key), the result is

.. code-block::

   abcabcabc
