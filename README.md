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

```bash
$ mkdocs new foodoc
```
    
2. Clone this repositiory in your project directory

```bash
$ cd foodoc
$ git clone https://github.com/MrLeeh/mkdocs-rtd-lightbox
```

3. Set mkdocs-rtd-lightbox as your custom theme in the mkdocs.yml

```yaml
theme:
  name: null
  custom_dir: mkdocs-rtd-lightbox
```

4. Install markdown-lightbox addon

```bash
$ pip install -e git+https://github.com/MrLeeh/markdown-lightbox.git#egg=markdown-lightbox
```

5. Add markdown-lightbox plugin to your mkdocs.yml

The resulting mkdocs.yml should look like this:

```yaml
site_name: My Docs
theme:
  name: readthedocs
  custom_dir: mkdocs-rtd-lightbox
markdown_extensions:
  - lightbox
  - extra
```

## Usage

The basic syntax for creating a lightbox-linked image is:

```
![Description](path/to/image.jpg)
```

However you might want to scale the image down. You can do this with the following syntax:

```
![Description](path/to/image.jpg){size="width:200px;"}
``` 
This is possible because we added the [Extra extension package](https://pythonhosted.org/Markdown/extensions/extra.html) 
of [Python Markdown](https://pythonhosted.org/Markdown/index.html) which allows the use of attribute lists.
