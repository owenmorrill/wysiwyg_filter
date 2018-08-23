WYSIWYG Filter
======================

The WYSIWYG Filter module provides an input filter that allows site 
administrators configure which HTML elements, attributes and style properties
are allowed. It also may add rel="nofollow" to posted links based on filter 
options. It can do so with no additional parsing on user input. That is, it may
apply nofollow rules while parsing HTML elements and attributes.

The filter is based on whitelists that can be defined from the filter settings 
panel. Rules for HTML element and attributes are defined using the same syntax 
of the TinyMCE valid_elements option. Note that the module does work with 
CKEditor and any other editor too, as it only filters formatted text.

HTML attributes related to DOM events (on*) are not allowed for security 
reasons (to prevent XSS, etc.).

The following elements cannot be whitelisted due to security reasons, to 
prevent users from breaking site layout and/or to avoid posting invalid HTML. 
Forbidden elements: applet, area, base, basefont, body, button, embed, form, 
frame, frameset, head, html, iframe, input, isindex, label, link, map, meta, 
noframes, noscript, object, optgroup, option, param, script, select, style, 
textarea, title.

The section used to whitelist style properties is pretty simple. You just check
the properties you need from a list where almost all style properties are 
organized into logical groups (Color and Background properties, Font, Text, 
Box, Table, List, ...). The WYSIWYG Filter will strip out style properties not 
explicitly enabled. On the other hand, for allowed style properties the WYSIWYG
 Filter will check their values for strict CSS syntax (based on regular 
 expressions) and strip out those that do not match. Additional matching rules 
 are explicitly required for properties that may contain URLs in their values 
 ("background", "background-image", "list-style" and "list-style-image"). If 
 rules don't match, these style properties will be ignored from user input.

When the "id" and "class" attributes have been whitelisted, it is also required
to specify explicit rules that will be used to validate user input, and again, 
those that don't match will be stripped out.

As a measure to reduce the effectiveness of spam links, it is often recommended
to add rel="nofollow" to posted links leading to external sites. The WYSIWYG 
Filter can easily do this for you while HTML is being processed with almost no 
additional performance impact. There is a section in the filter settings panel 
where a white/back list policy can be defined per domain name (the host part in
 the URLs).

This module has been ported from version 7.x-1.x.

Installation
------------

- Install this module using the official Backdrop CMS instructions at
  https://backdropcms.org/guide/modules.

- Navigate to admin/config/content/formats and choose the menu you want to 
  customize.

- Click on "Configure" on the text editor you'd like to add the WYSIWYG filter.

- Check the box for "WYSIWYG Filter" to add the option below in the 
  "Filter settings" section.
  
- Click on the tab titled "WYSIWYG Filter" in the "Filter settings" section.

- Fill in, check, or enter the information in the fields provided.

- Enter content into nodes as usual, output will follow the filter settings you
  established.

Documentation
-------------

Additional documentation is located in the Wiki:
N/A

Issues
------

Bugs and Feature requests should be reported in the Issue Queue: 
https://github.com/backdrop-contrib/wysiwyg_filter/issues

Current Maintainers
-------------------

- Owen Morrill (https://github.com/owenmorrill).

Credits
-------

- Ported to Backdrop CMS by Owen Morrill (https://github.com/owenmorrill).
- Originally written for Drupal by Marc Ferran (https://www.drupal.org/u/markus_petrux).

License
-------

This project is GPL v2 software. See the LICENSE.txt file in this directory for
complete text.
