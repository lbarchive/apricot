========
Settings
========


.. contents:: **Contents**
   :local:


``pelicanconf.py`` settings
===========================

Official settings
-----------------

``DISPLAY_PAGES_ON_MENU``
  You can disable pages listed on hovering header.

``DIRECT_TEMPLATES``
  If you don't need Authors, Tags, Categories, or Archives to be on hovering header,
  you need to remove them from ``DIRECT_TEMPLATES``, changing setting like
  ``AUTHORS_SAVE_AS`` won't affect.

  For Categories, you could set ``DISPLAY_CATEGORIES_ON_MENU`` to ``False``, if
  you still want the Categories page to be generated.


Apricot specifics
-----------------

``CSS_INLINE``
  You can tell Apricot to inline the ``CSS_FILE``, however, if it's not default
  ``main.css``, you will have to either symbolic link from or copy the file to
  the ``templates`` directory.

``SITE_DESCRIPTION``
  This is displayed below your blog name in the hovering header.

``ATTRIBUTION`` (integer or text)
  This controls how much attribution to Pelican, Python, and this theme you
  would like to show.

  \ -1
    Absolutely nothing.

  0 (default)
    All mentions in HTML comment.

  1
    Just Pelican.

  2
    Pelican and Python.

  3
    Pelican, Python, and the theme.

  4
    Pelican, Python, and the theme plus its author.

  text
    Custom attribution, it can be HTML.


Content metadata
================

``:thumbnail:`` (URL)
  It is the thumbnail image URL for the content, it will be displayed in pages
  like archive or any index style pages.

  It is also used for schema.org ``thumbnail`` property of ``Article``.
