---
layout: page
title: Version Control &rsaquo; GitHub
permalink: /version-control/github/
---

## Introduction
First of all; GitHub is pretty simple. This 5 minute [interactive introduction][intro] will guide you through the basics. It won't take long, but it will set you up with some very powerful concepts that will take you farther than you think.

![GitHub Flow Introduction]({{ site.baseurl }}/img/github-flow.png)


## GitHub Flow
:green_apple: [GitHub Flow][original] is how [GitHub uses GitHub to build GitHub][video]. It works especially well for projects that are continously developed and deployed. Imagine that you and your team make constant and small iterative changes to the code base, updating the production code multiple times a day.

Something more complex like [GitFlow][gitflow] could be a better fit for a project that makes less frequent, larger updates. In GitHub Flow, a "hotfix" can essentially be handled just the same way as a regular push to master in.

To learn more, read the [original article][original], watch the rather entertaining [extended brief][video], or skim the [summary][summary] on the official GitHub blog. And remember the [introduction to GitHub][intro] mentioned above? That's in fact a pretty spot on description of the workflow in under 5 minutes. That simple.


## When and how to rebase
According to good practice *GitHub Flow*, opening pull requests early is encouraged. When multiple people are working on the same repo, this will cause some pull requests to go stale as others are merged into ``master``. Before merging stale branches, they should be rebased onto the remote ``upstream/master`` branch.

Perform the rebase according to this [excellent guide][rebase] by [edX][edx]. It also does a great job of explaining why rebasing is prefferable to a merge.



[edx]: https://open.edx.org/
[rebase]: https://github.com/edx/edx-platform/wiki/How-to-Rebase-a-Pull-Request
[intro]: https://guides.github.com/introduction/flow/index.html
[original]: http://scottchacon.com/2011/08/31/github-flow.html
[video]: http://zachholman.com/talk/how-github-uses-github-to-build-github/
[gitflow]: http://nvie.com/posts/a-successful-git-branching-model/
[summary]: https://github.com/blog/1557-github-flow-in-the-browser
