---
layout: page
title: Documentation
permalink: /documentation/
---

Your project documentation will inevitably be **[the most][rdd] [important part][most-important-doc]** of your project going forward. It's important to use any and all means at your disposal to document your code.

:gem: Include a lot of usage examples and keep it concise and clearly structured.

> There's even entire development strategies with their starting points in the project documentation. The simplest and most attrative of them is [README Driven Development][rdd-summary].


## Dedicated documentation
This is likely the main entry point for new users. The dedicated documentation should first and foremost provide a higher level description of the software. It's important to give a gentle introduction but still get to the point the point quickly.

It should be available online, either as part a README file for small projects or more likely a full web site. Liberally include code examples and if possible a short demo tutorial where the user can follow along.


## Inline documentation
Worry more about not documenting enough than documenting too much.

Always document classes, methods, and functions. It should be clear what input arguments are expected and what output it is transformed into. A function documentation should also describe under which condition it raises exceptions.

A welcome addition is to provide consice usage examples along with the e.g. function documentations.

{% highlight python %}
@curry
def grep(pattern, line):
  """Match a simple pattern substring in a given string.

  Note that the function would also work to check for an item in a list,
  a key in a dictionary etc.

  Args:
    pattern (str): substring to match with
    line (str): string to match against

  Returns:
    bool: if ``pattern`` was a substring in ``string``

  Examples:

  .. code-block:: python

    >>> directors = ['Quentin Tarantino', 'PT Anderson']
    >>> list(filter(grep('Anderson'), directors))
    ['PT Anderson']
  """
  return pattern in line
{% endhighlight %}

Find out [how to document functions][google-docstrings] in your language and stick to accepted conventions.


## Change log
Follow this [opinionated standard][keepachangelog] dubbed "Keep a CHANGELOG". Basically it should be written in Markdown, mark each release with a version and date, and clearly separate between different categories of changes.


## Flowcharts
:green_apple: Flowcharts can convey overview in ways that is impossible to put into words. It can be a great way to organize e.g. a pipeline of functions that will help you in the design of your project.

A great, dedicated flow chart creation tool is :gift_heart: [Delineato][delineato], $6.99 on the *Mac App Store*. Another option that works surprisingly well is :gift_heart: [Apple Keynote][keynote] making use of the ``Insert > Line > [Straight] Connection Line``.


[google-docstrings]: http://sphinxcontrib-napoleon.readthedocs.org/en/latest/example_google.html
[rdd]: http://tom.preston-werner.com/2010/08/23/readme-driven-development.html
[rdd-summary]: {{ site.baseurl }}/documentation/readme-driven-development/
[most-important-doc]: http://zachholman.com/posts/documentation/
[delineato]: http://www.delineato.com/
[keynote]: https://www.apple.com/mac/keynote/
[keepachangelog]: http://keepachangelog.com/
