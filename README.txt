;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;
;; WYSIWYG Filter module for Drupal
;; $Id$
;;
;; Original author: markus_petrux at drupal.org (October 2008)
;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;

OVERVIEW
========

The WYSIWYG Filter module provides an input filter that allows site
administrators configure which HTML elements, attributes and style properties
are allowed. It also may add rel="nofollow" to posted links based on filter
options. Benefit is it does so with no additional parsing on user input. That
is, it may apply nofollow rules while parsing HTML elements and attributes.



INSTALLATION
============

- Copy all contents of this package to your modules directory preserving
  subdirectory structure.

- Goto admin/build/modules to install the module.

- Goto admin/settings/filters and create a new input format as follows:

  - Input format name: WYSIWYG Filter (or something similar of your choice).
  - Check the filters: WYSIWYG Filter and HTML Corrector. Save.
  - Goto Rearrange tab.
  - Drag the WYSIWYG Filter on top of the HTML Corrector. Save.
  - Goto the Configure tab of your newly created WYSIWYG Filter and setup the
    options to suit your needs.
