---
layout: page
title: Code Review
permalink: /code-review/
---

Code reviews exist to spot mistakes that were overlooked during inital development. They are also an excellent opportunity for spreading knowledge and best practises among your team members.

I've basically stolen all of this from Thoughbot's guide on [Code Review][thoughtbot].

- Establish the idea that *everybody* gets reviewed. No one stands above the rest. Every patch gets reviewed. However small, there is no valid argument to not review it.
- As far as possible, code should be reviewed before it gets merged.
- Make liberal use of GitHub and pull requests; use line-specific comments for example.
- For bigger patches, don't be afraid to ask to separate them into smaller units.
- Document code review practises.


## Role: Reviewer
The reviewer should focus on things in this order:

1. Intent (why)
2. Design (how)
3. Implementation
4. Grammar

Collect the suggested changes in TODO lists, questions for the code author, and suggested follow-ups for later patches.


## Automate the automatable
Aim to discover mistakes as early as possible. This includes running lints, checking for conformance to style guide, etc. Encourage team members to run these tools locally as well as considering them as part of your [continous integration][ci] flow. It can also be worth mentioning that it's often easier to take critisim from computers rather than your peers.



[thoughtbot]: https://github.com/thoughtbot/guides/tree/master/code-review
[ci]: {{ site.baseurl }}/testing/
