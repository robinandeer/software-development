# software-development
General guidelines and style guide for software developed at SciLifeLab.

I think we'll start with software development and see if we branch out enough to discuss if we should switch the name of the repository.

> Reason for forking: I started this project at SciLifeLab but I think I'm still the only contributor so this is really more of my own collection of best practices :sweat_smile:


## Idea
The guide should clearly separate between 1) *conventions* :green_apple:, 2) *best practices* :gem:, and 3) *helpful tools* :gift_heart:. Try to mark each paragraph or suggestion with it's corresponding emoji (before the reference).

1. **Conventions** are agreed upon standards that consolidate projects so that any developer can quickly get up an running with any project. They don't nessesarily need to be motivated or back by evidence.

  A good example is whether to use 2 or 4 spaces per indentation. No choice is nessesarily better but as long as everyone agrees on one of them, it makes it easier to work across projects.

2. **Best practices** are standards backed by evidence or significant experience. Breaking a best practice should require an explanation.

  An example is to use spaces instead of (hard) tabs for indentation. In this case, the motivation is that spaces are supported across all editors and work more consistently than tabs.

3. **Helpful tools** can be provided at the end of a page or section. They can help to enforce certain conventions or best practices.

  An example relating to our indentation example is [EditorConfig](http://editorconfig.org/). It's a cross editor configuration file that can be places inside a project and commited to source control. This means that project level standards will be easily shared and enforced for anyone working on the project.


## Motivation
A lot of companies produce [various][material-style] [style][numpy-style] [guides][ios-style] to ensure consistently high quality and side effects that come from subscribing to common conventions.

It will also be a great entry point and reference for new employees and people getting into a new programming language.


## Considerations
One important point to make is that there are already a lot of projects like the [Python Guide][python-guide] that cover a lot of convetions and best practices. When ever possible, try to clearly reference and point people to already existing resources of high quality. It might, however, be a good idea to provide a short summary on this site as well.


## Development
This is intended to be a living document that is continously updated and refined. If you want to add or update something, create a branch on this repository (no need to fork) with a name that clearly conveys it's intended purpose. Don't hold off on pushing your branch to the central repository.

This way it will be easy for other developers to get a quick grasp of what is being worked on by looking into the lists of active branches.

You are encouraged to open a pull request for your branch *early*, for example if you have questions for other developers. When you feel ready and have gotten at least two :thumbsup: or :shipit: you can go ahead and merge the branch into "master".


## Examples for inspiration

* [Python Code Style Guidelines](http://www.cs.swarthmore.edu/~richardw/cs21-s09/python_codestyle.php)
* [PyStyleGuide](http://wiki.ros.org/PyStyleGuide)
* [Python Style Guide](https://github.com/numenta/nupic/wiki/Python-Style-Guide)
* [Code Like a Pythonista: Idiomatic Python](http://python.net/~goodger/projects/pycon/2007/idiomatic/handout.html)
* [Chromium: Python Style Guidelines](http://www.chromium.org/chromium-os/python-style-guidelines)
* [Python Guide: Code Style](http://docs.python-guide.org/en/latest/writing/style/)



[material-style]: http://www.google.com/design/spec/material-design/introduction.html
[numpy-style]: https://github.com/numpy/numpy/blob/master/doc/HOWTO_DOCUMENT.rst.txt
[ios-style]: https://developer.apple.com/library/iOS/documentation/UserExperience/Conceptual/MobileHIG/index.html#//apple_ref/doc/uid/TP40006556
[python-guide]: http://docs.python-guide.org/en/latest/
