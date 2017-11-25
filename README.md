# mkdocs-rtd-lightbox
Readthedocs theme for mkdocs with Lightbox support

This is a fork of the [mkdocs](http://www.mkdocs.org) builtin Readthedocs theme which adds support for 
[Lightbox](http://lokeshdhakar.com/projects/lightbox2/). Lightbox is small javascript library used to 
overlay images on top of the current page.

# Usage with markdown-lightbox addon

The markdown-lightbox addon wraps all images in a lightbox link. The syntax is the same as to insert
a normal image:

    ![Description](http://image/link.jpg)
    
See documentation of the [markdown-lightbox](https://github.com/MrLeeh/markdown-lightbox) addon for details.

## Installation

1. Create a new mkdocs project

    $ mkdocs new foodoc
    
2. Clone this repositiory in your project directory

    $ cd foodoc
    $ git clone https://github.com/MrLeeh/mkdocs-rtd-lightbox
