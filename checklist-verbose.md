## Version control

- version control from the beginning of the project
- use git as version control system (vcs)
> Other VCS can be used if the project does not start in NLeSC and does not use git or when the prevailing VCS in particular community
> is not git. Even then changing VCS should be considered (especially if svn or other centralised system is used).

- choose one branching model, make the choice explicit in contribution guidelines, link to documentation on how to get started with it
> NLeSC default choice is [GitHub flow branching model](https://guides.github.com/introduction/flow/)
> (TL;DR: use feature branches and pull requests).
> GitHub flow is very simple and sane branching model. It supports collaboration and is based on pull requests, therefore relies
> heavily on GitHub. [Pro Git](https://git-scm.com/doc) book describes in detail the workflow of collaboration on the project
> with use of git branches,
> forks and github in [Contributing to a Project chapter](https://git-scm.com/book/en/v2/GitHub-Contributing-to-a-Project).
> Other more complicated models could be used if necessary, but we should strive for simplicity and uniformity
> in NLeSc since that will enhance collaboration between the engineers. Learning new branching model should not stand in the way
> of contributions. 
> You can learn more about those other models from [atlasian page](https://www.atlassian.com/git/tutorials/comparing-workflows).

- public vcs repository ([github](https://github.com/))
> Unless code cannot be open (usually commercial partners, or some competitiveness issues ) it should be in public online repository.
> In case the code uses data, that cannot be open, an engineer should try to keep sensitive parts outside of the main codebase.

- meaningful commit messages
> Commit messages are the way for other developers to understand changes in the codebase. In case of using GitHub flow model commit 
> messages can be very short but pull request comment should explain all the changes. It is very important is to explain the why
> behind implementation choices. To learn more about writing good commit messages read
> [tpope’s guide](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
> and [this post](http://who-t.blogspot.nl/2009/12/on-commit-messages.html)

## Release
> Those points by definition apply to software that is **released** tho the users. Where users can be researchers or other engineers.

* [semantic versioning](http://semver.org/)
> Semantic Versioning (semver) is the most accepted and used way to add numbers to software versions. It is a way of communicating impact of
> changes in the software on users. Very often package managers depend on `semver` and will not work
> as expected otherwise.

- tagged releases ([github releases](https://help.github.com/categories/releases/))
> Releases are a way to signify and point to particular milestone in software development.
> [Apache foundation](http://www.apache.org/) describes their [release policy](http://www.apache.org/dev/release.html).

- CHANGELOG.md ([Keep a CHANGELOG](http://keepachangelog.com/))
> Change log is a way to communicate notable changes in release to the users and contributors.
> Every release should have relevant entry in change log.

- one command install ([pip](https://pypi.python.org/pypi/pip), [npm](https://www.npmjs.com/package/npm) etc)
> This applies to software which is distributed as package or library that will be used by other software
> or from within other language. Should be
> implemented when there are (going to be) first users of the software, so that they can use
> default package managers.

- package in package manager ([pypi](https://pypi.python.org/pypi), [npm](https://www.npmjs.com/) etc)
> This is a way to publish the package.

- discuss release cycle with coordinator
> Release cycles will depend on the project specifics, but in general we encourage quick agile
> development and therefore frequent releases.

- release quick-scan by other engineer (is documentation understandable, can it be installed, etc)
> Think of it as a kind of code review but with focus on mechanics, not code. The reviewer should check if:
> (i) there is easily visible or findable documentation,
> (ii) download works, (iii) there are instructions on how to (iv) install and (v) start using software,
> some of the things in this *scan* could be automated with continuous integration.

- notify Lode for dissemination (news item on site / annual report, etc)
> News item should be made for at least first stable and subsequent major releases (the ones with major change in semantic versioning)

> Read more about releases [here](http://www.apache.org/dev/release.html)

## Licensing

- [Apache 2 license](http://www.apache.org/licenses/LICENSE-2.0)
> Apache 2.0 is the default choice for the NLeSC software license. Other license can be used in special cases, when software has
> already attached license or there are commercial partners that require different licensing.
- compatible license of all libraries
> All software used in the project **MUST HAVE** compatible licenses. Compatibility should be checked
> when new external code is added to the project.
- `NOTICE(.txt|.md)` listing licenses, request citation of paper if applicable
> Read more [here](http://www.apache.org/dev/licensing-howto.html)

## Communication

> Communication to the outside world is important for visibility of NLeSC projects and for building
> the user base.

> Communication to other developers is a way to build community and contributors. It also increases
> NLeSC visibility in development world.

- home page with all the necessary introduction information, links to documentation, source code (github) and latest release download (e.g. [github.io pages](https://pages.github.com/))
> The page should be created at the latest when the software is ready to be seen by the outside world. It is the place where people will learn about software, so it is important to describe its goals and functionality.
> It should be targeted towards non-programming users (unless software is meant for programers i.e library) but should have
> pointers for developers to more advanced resources (README.md)

- project discussion list (github issues, mailing list, not private email) for all project related
  discussions from the beginning of the project
> There should be no private discussions about the project. Therefore once discussions are started
> (in the email), either move them to github issues or if they don’t fit into issues format any more,
> create the mailing list.

- for services: a demo docker image in dockerhub (with Dockerfile)
> If software is the service Docker image should be created at the very early stage. This will allow for easier testing and platform
> independent use.

- for websites: an online demo
> Online demo should be available since first stable release. 
> When the website is the user interface for researchers, make sure there is a development version
> running somewhere so that they can *play around with it* and give usability feedback. 

- Pitch presentation (1 to 3 slides)
> Pitch presentation should be prepared when visible results of the software are available.
> It is important to keep those up to date and that other engineers have easy access to it.

- Few sentences about the project for [nlesc technology pages](https://www.esciencecenter.nl/technology)
> Short description of the project should be provided from the beginning of the project.
> Starting with requirements and should be updated along the way. There should be no major updates there
> since the goal of the project should not change.

## Testing

> Those points do not apply to prototype / throwaway phase.

- [unit tests](https://en.wikipedia.org/wiki/Unit_testing)

- [continuous integration](https://en.wikipedia.org/wiki/Continuous_integration) (CI), public on [Travis](https://travis-ci.org/)
> CI meaning: compile, unit test, integration test, quality analysis etc.
> Once there is some build process established and tests set up, CI should be configured too.
> It will save you a lot of time on debugging and allow for much quicker problem diagnosis.

- continuous code coverage and code quality metrics public, minimum 70% coverage required
> It is easy to generate those automatically, once the test are setup, with use of external services.

- end2end test for (web) user interfaces. [example with protractor and angular](https://angular.github.io/protractor/#/)
> Once the web page has any interface, e2e tests should be implemented.

- track dependencies (with [VersionEye](https://www.versioneye.com/),
  [David](https://david-dm.org/) or other service depending on codebase language)
> Checking for dependency updates should be done regularly. It can save a lot of time,
> avoiding code dependent on deprecated functionality.

## Documentation
- `README.md` - clear explanation of the goal of the project with pointers to other documentation resources.
> Use [GitHub flavoured markdown](https://help.github.com/categories/writing-on-github) for, e.g.,
> [syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks).
> README is targeted towards developers, it is more technical than home page.
> Keeping basic documentation in README.md can be even useful for lead developer,
> to track steps and design decisions.
> Therefore it is convenient to create it from the beginning of the project,
> when initialising git repository.
> [StackOverflow on good readme](http://stackoverflow.com/questions/2304863/how-to-write-a-good-readme),
> [short gist with README.md template](https://gist.github.com/jxson/1784669)

- well defined functionality
> Ideally in README.md

- source code documentation

- usage documentation

- documented development setup
> (good example is
> [Getting started with khmer development](http://khmer.readthedocs.org/en/latest/dev/getting-started.html))
> It should be made available once there is more than one developer working on the codebase.

- contribution guidelines
> [example](https://github.com/angular/angular.js/blob/master/CONTRIBUTING.md)
> Guidelines should be made available once the code is available online and there is a process
> for external contributions. External contributions not necessary mean ‘out of NLeSC’
> it could be other engineer in NLeSC. Good guidelines will save time of both lead
> developer and contributor since things have to be explained only once.
> [GitHub supports CONTRIBUTING file](https://github.com/blog/1184-contributing-guidelines). 

- code of conduct ([contributor covenant](http://contributor-covenant.org/))
> CofC should be attached from the beginning of the project. There is no gain fro having it with one
> developer, but it does not cost anything to include it in the project and will be handy when more
> developers join.

- documented code style
> From the beginning of the project, decision on the code style has to be made
> and then it should be documented. Not having documented code style will highly
> increase the chance of inconsistent style across the codebase, even when only
> one developer writes code.

- meaning of issue labels used
> Once users start submitting issues labels should be documented.

- DOI or PID ([making your code citable](https://guides.github.com/activities/citable-code/))
> Identifiers should be associated with releases and should be created together with first release.

## Development setup

- using the NLeSC coding style is required
> NLeSC should have sane suggestion of coding style for each programming language in use in NLeSC.
> Coding styles are about consistency and making a choice and not so much about the superiority of
> one style over the other. Sane set of guides can be found on in [google documentation](https://github.com/google/styleguide).

- [editorconfig](http://editorconfig.org/)
> Using editor config is not necessary, but saves a lot of time and keeps developers from straying
> from the style of choice and helps to avoid some problems caused by formatting differences
> (line ending, tabs vs spaces)

- applied code style in automated way if possible (i.e using linters and code formatters)
> Use of linters will not only help to keep code cleaner but will also help finding bugs

- dev environment docker images in Dockerhub (with Dockerfile)
> This can be very helpful in case of complicated development environment setup and when you want to help developers quickly start
> with contributions without struggling with setup

## Use standards

- exchange format (Unicode, W3C, OGN, NetCDF, etc)
- protocols (HTTP, TCP, TLS, etc)

> Standard files and protocols should always be a primary choice.

