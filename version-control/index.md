---
layout: page
title: Version Control
permalink: /version-control/
---
## Table of Contents
1. [Versioning][versioning]
2. [GitHub][github]


## Rebase vs. merge
According to good practice [GitHub Flow][github] it's a good idea to open pull requests early. When multiple people are working on the same repo, this will cause some pull requests to go stale as others are merged into ``master``. Before merging stale branches, they should be rebased onto the remote ``upstream/master`` branch.

Perform the rebase according to this [excellent guide][rebase] by [edX][edx]. It also does a great job of explaining why rebasing is prefferable to a merge.


## Helpful tools
:gift_heart: [SourceTree][source-tree] is a truly fully featured and *free* Git client that plays nicely with GitHub. It's great if care to devote your spare brain cells to something other than remembering obscure Git commands.



[edx]: https://open.edx.org/
[github]: {{ site.baseurl }}/version-control/github/
[rebase]: https://github.com/edx/edx-platform/wiki/How-to-Rebase-a-Pull-Request
[source-tree]: https://www.atlassian.com/software/sourcetree/overview
[versioning]: {{ site.baseurl }}/version-control/versioning/
