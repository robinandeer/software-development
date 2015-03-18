---
layout: page
title: Version Control &rsaquo; Versioning
permalink: /version-control/versioning/
---

## Semantic Versioning
There really is no reason to look any futher than :gem: [Semantic Versioning 2.0.0][semver].

In broad terms, SEMVER advocates dividing the version tag into three parts: ``MAJOR.MINOR.PATCH``. The scope of an update to the production code should be reflected in the delta between the previous and new version. E.g. a bug fix will generally correspond to a software patch and would be indicated with ``X.X.X -> X.X.X+1``.


## Helpful tools
:gift_heart: [Bumpversion][bumpversion] is a nice tool to automate the process of updating the version of your software. It's written in Python but is otherwise language agnostic.

For a general Python project the basic configuration file would reside in the root of the project and look something like this:

{% highlight INI %}
[bumpversion]
current_version = 0.0.1
commit = True
tag = True

[bumpversion:file:my_package/__init__.py]

[bumpversion:file:setup.py]
{% endhighlight %}

[bumpversion]: https://github.com/peritus/bumpversion
[semver]: http://semver.org/
