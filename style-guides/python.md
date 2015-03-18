---
layout: page
title: Style Guides &rsaquo; Python
permalink: /style-guides/python/
---

> Code is read much more often than it is written. - A Wise Pythonista

:gem: [PEP8][pep8] and :gem: [PEP20][pep20] (``import this``) should be considered as the starting points. Unless specified otherwise, we follow the guidelines laid out there. For a brief overview, read the [Python Guide][python-guide#style]'s entry on the subject.


## PEP8 clarifications and tips
The official guide has some very nice tips on [code layout][code-layout]. This can be a nice reference when you are unsure about how to e.g. style your hanging indents.

### Indentation
:green_apple: Use 4 *spaces* to indent code. Never use hard tabs. Spaces are preferred over tabs for the following reason: spaces are spaces on every editor on every operating system. Tabs can be configured to act as 2, 4, 8 "spaces" and this can make code unreadable when being shared.

### Maximum line length
Limit all lines to a maximum of 79 characters. Break down the line if it exceeds the maximum length. For example:

{% highlight python %}
# Python automatically concatenates consecutive strings
a_long_string = ("I am a very long string that can be split across"
                 "multiple lines by automatic string concatenation.")

# multi conditional if-statements can be split into multiple statements
# notice how the code reads a lot like regular English!
first_condition = 'genius' in 'Paul Thomas Anderson'
second_condition = 'genius' in 'Daniel Day-Lewis'

if first_condition and second_condition:
  print('And the Oscar goes to... There Will Be Blood!')
{% endhighlight %}

### Imports
I like to split up imports into three seprate groups: 1. standard library imports, 2. third party imports, 3. intra-package imports.

{% highlight python %}
import os
import re

import numpy as np
from path import path

from .utils import read_config

{% endhighlight %}

There are also another category of imports known as "future imports". They exist to bridge the gap between Python 2 and 3. It's important to realize that they only effect the current module they are present in. Future imports must be at the top of your Python module file. I make it a habit of putting the following lines at the top of every module I write:

{% highlight python %}
# -*- coding: utf-8 -*-
from __future__ import absolute_import, unicode_literals, division
{% endhighlight %}


## Installation
All packages should be installable through pip by running (inside project root):

{% highlight console %}
$ pip install [-e] .
{% endhighlight %}

This means that the package needs a ``setup.py`` file which is used by ``setuptools`` during installation. To expose console scripts [it's preferred][setuptools-entrypoints] to use :gem: [entry points][entry-points] over explicit Python scripts.

## Starting point
:thought_balloon: *To easily get set up with a base project structure we should provide a central skeleton repository to base future Python projects on. We might like to consider something like :gift_heart: [Cookiecutter][cookiecutter].*

## <a name="python2vs3"></a> Python 2 vs. 3 support
Code should be written to take advantage of straight forward ways to accomplish universal Python support. This means:

1. Sticking to pure Python code whenever possible.
2. Making liberal use of :gem: ``from __future__ import <e.g. print_function>`` on any page where nessesary. This includes but is not limited to:
  - print_function
  - unicode_literals
  - absolute_import
  - division
3. The Python 3 version of the ``open`` functions should be used through :gem: ``from codecs import open``.
4. Use Python 3 style :gem: relative imports: ``from .subpackage import func``

## Command line utilities/scripts
If you are building anything remotely complex, the command line framework of choice is :green_apple: [Click][click]. It's an elegant and flexible package with a great syntax.

## Imperative vs. functional programming
Is writing unit tests for your code a piece of cake? If "yes", then you need not worry - you are probably writing good quality already. However, if you are struggling with your tests it might help to consider more of a *functional* (rather than imperative) approach. Read [an introduction to functional programming][functional] or take away some of the key points:

1. Each function should do *only* one thing.
2. Write *stateless* functions that perform tasks without knowledge of what's going on beyond it's scope.
3. Treat all data structures as immutable.
4. Think hard before adding for/while loops, there's usually a cleaner way to do it.
5. Compose small, discrete components into larger once.

## Docstrings
Functions, methods and classes should be annotated using :green_apple: [Google Style Docstrings][google-doc]. They look a little something like this:

{% highlight python %}
def find(some_id):
  """Returns a single item defined by it's unique id. Returns
  ``None`` if it can't find the requested item.

  Args:
    some_id (str): unique item id

  Returns:
    dict or None: item from the data store or ``None``

  Examples:

    >>> find('1')
    {'id': 1, 'director': 'P.T. Anderson', ...}

  """
  pass
{% endhighlight %}

## Helpful tools
We encourage using a :gift_heart: *linter* to continously check the syntax of your code. The Python community maintains a number of linters such as pep8, and [PyFlakes][pyflakes].

Another resource that can greatly ease collaboration is :gift_heart: [EditorConfig][editor-config]. It's an effort to provide a cross editor configuration format and in placed in your project and commited to source control. You also need to install a plugin for your favorite editor, e.g. [Sublime][sublime-config].

[pep8]: http://legacy.python.org/dev/peps/pep-0008/
[pep20]: http://legacy.python.org/dev/peps/pep-0020/
[code-layout]: http://legacy.python.org/dev/peps/pep-0008/#code-lay-out
[pyflakes]: https://pypi.python.org/pypi/pyflakes
[flake8]: https://pypi.python.org/pypi/flake8
[entry-points]: http://pythonhosted.org/setuptools/pkg_resources.html#entry-points
[click]: http://click.pocoo.org/
[python-guide#style]: http://docs.python-guide.org/en/latest/writing/style/
[google-doc]: http://sphinxcontrib-napoleon.readthedocs.org/en/latest/example_google.html
[functional]: http://www.smashingmagazine.com/2014/07/02/dont-be-scared-of-functional-programming/
[editor-config]: http://editorconfig.org/
[sublime-config]: https://github.com/sindresorhus/editorconfig-sublime
[setuptools-entrypoints]: https://pythonhosted.org/setuptools/setuptools.html#automatic-script-creation
[cookiecutter]: https://github.com/audreyr/cookiecutter
