.. _ch-intro:

************
Introduction
************

Creating a PhD thesis is typically done using LaTeX. This works really well for
producing a PDF, but a giant PDF file is not a great way to put documents on
the web. There are solutions that exist to turn latex source files into HTML,
but in my experience, they tend to produce poor HTML output.

The `Sphinx <http://sphinx.pocoo.org/>`_ project is a wonderful tool for
creating portable documents, allowing for output to many different formats.
Unfortunately, it has many shortcomings when trying to typeset something
so advanced as a PhD thesis. The aim of this project is to modify Sphinx to
support all of the needs of a thesis writer. Many of the patches are not
appropriate for contributing directly to the upstream Sphinx repository, so
this is instead a separate project.

This sphinxtr output is available in several formats at:
http://jterrace.github.com/sphinxtr.

The source code for sphinxtr can be found at:
https://github.com/jterrace/sphinxtr.

Installation
============

Install the required Python packages::

    pip install -r requirements.txt

I was unable to build a PDF using my regular TeXLive
installation (``apt-get install texlive-full`` in Ubuntu 12.04).
However, after setting up a clean, full `TeXLive 2012`_, everything went smoothly.

.. _TeXLive 2012: http://www.tug.org/texlive/doc/texlive-en/texlive-en.html#installation

Building
========

You need ``make``. The following targets are supported:

html
  Builds HTML format, separated into sections
singlehtml
  Builds HTML format on a single page
text
  Builds text files, separated into sections
singletext
  Builds a single text file
latexpdf
  Builds into latex source files and then compiles into a PDF. Requires latex.

Changes
=======

The following changes and additions have been made from vanilla Sphinx:

* A cross-format bibtex bibliography based on sphinx-natbib
* Tables that can go inside figures
* Changed table formatting to look pretty, like booktabs
* Improved alignment in table environment
* Added support for short captions that show up in the "list of figures" section
* Changed equation reference formatting from "(1)" to "1"
* Full customization of latex preamble and style file
* Numbered figures
* Numbered section references
* A singletext output that builds into a single text file, similar to singlehtml
* A subfigure environment

Documents Using sphinxtr
========================

* `Jeff Terrace's PhD Thesis <http://www.cs.princeton.edu/~jterrace/thesis/>`_
