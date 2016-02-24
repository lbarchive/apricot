=================
Key design points
=================


.. contents:: **Contents**
   :local:


Simplicity
==========

Layout
------

1044px width, fixed and centered
''''''''''''''''''''''''''''''''

Apricot has a fixed with at 1044 pixels for default view, 1024px of which are
for the main content, the rest 40 pixels are the margins for the both sides.

The choice of 1024 is for images, and that's based on the embedding image
options from image hosting services. Personally, I like 800px, but really only
a few provide that size; However, 1024 is virtually all available, and that's
why I went for 1024px.

20px on either side is a compromise I have to accept. If I set the width to
1024px and the actual screen is at the same size, then text likely would stick
to the edge and that'd not be easy to read.

As far as I know, there is many mobile devices is at 1024px width, which would
be in turn served with `responsive design`_.

And since it's a fixed width, that would only be natural to go with centered
layout.

Responsive design
'''''''''''''''''

For screen sizes which are smaller than 1044 pixels in width, they will be
served with a fixed width that is with 10px margins and the rest of width goes
to the main content.

The base font size goes down to 20px from 24px.

Decluttered
'''''''''''

In these days, many websites are cluttered with tons of links, the amount of
the links are more than the links in the main article by ten fold easily.
Social media, stuff in sidebar, confusing links in header, no-so-related
related and recommended content on sidebar #2, and many more in the footer.
Right, almost forgot the share buttons.

Are they really necessary?

There is no any sidebar, but a footer and hovering header. Yes, this theme does
have a header, see those dots on top edge, hover over and you will see.

Style
-----

I tried to use as less CSS as possible, only using for readability, such as the
background color for the hovering blog header and for table cells.

Monochrome color
''''''''''''''''

I don't like reading a blog that is as if being painted by three years old, or
having various styles.

Basically, colors are all based on a base apricot color, all used colors are:

* ``#A85206``
* ``#D67113``
* ``#F0923B``
* ``#FFAD61``
* ``#FFC38B``

Of course, there is the default black text color, it's also part of monochrome
colors.

There is also the syntax highlighting, Apricot uses colors from
`Solarized Pygments Style`_, I don't count those colors as part of the theme.

.. _Solarized Pygments Style: https://github.com/john2x/solarized-pygment

Limited fonts and styles
''''''''''''''''''''''''

Fonts are limited to three:

1. One sans for headings or titles;

   Palatino, Georgia, Times, Times New Roman, and serif

2. One serif for content; and

   Verdana, Tahoma, Arial, and sans

3. One monospaced for code-like things.

   Courier, Courier New, monospace

There is no web fonts used, the list of candidate fonts should be available on
most of systems.

There is only one base font size set, a couple of ``font-weight`` uses, nearly
everything defaults to browser's shipped styles.

No social media and links
-------------------------

There is no spaces for them, you should put them in About page.

I don't use them, so I didn't add them, if you really need them, open a feature
request.

No images and just plain ASCII
------------------------------

Do we actually need images to tell what the thing is?

I decided to go with plain old ASCII, not even any Unicode symbols. With
Apricot, you only need one HTML and an extra CSS if not inlined.


Templating
==========

Jinja2 is a powerful templating library, however, if you want to do something
even more, you may need to enable some extensions, or even write additional
extensions, which I decided not to go for.

A few examples are:

1. Looping to filter out duplicate item for pagination,
2. Extra ``if`` block for not enabling ``continue`` of *Loop Controls*
   extension, or
3. Appending item without using ``do`` of *Expression Statement* extension.

I prefer theme users don't have to change any of their ``pelicanconf.py``
settings.


Schema.org
==========

Apricot has incorporated some schema.org.
