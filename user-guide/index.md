---
layout: page
title: User Guide
permalink: /user-guide/
---

## User guide for shared users
On login your environment will be setup to configure the ``$PATH`` variable, aliases etc.


### Python
The ``production`` [conda environment][conda] is loaded automatically as default. If you are doing development, make sure to switch virtual environment by running:

{% highlight bash %}
$ source activate [develop]
{% endhighlight %}

Here's a [very nice reference][format]/mini tutorial on the format mini-language used for string formatting in Python.

[conda]: /software-development/environment/#installing-python
[format]: http://pyformat.info/
