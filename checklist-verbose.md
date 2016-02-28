## Version control

- version control from the beginning of the project
- use git as version control system (vcs)
> Other VCS can be used if the project does not start in NLeSC and does not use git or when the preveling VCS in particular community
> is not git. Even then changing VCS should be considered (especially if svn or other centralised system is used).

- choose one branchig model, make the choice explicit in contribution guidelines, link to documentation on how to get started with it
> NLeSC default choice is [GitHub flow branching model](https://guides.github.com/introduction/flow/)
> (TL;DR: use feature branches and pull requests).
> GitHub flow is very simple and sane branching model. It supports collaboration and is based on pull requests, therefore relies
> havyly on GitHub. Other more complicated models could be used if necessary, but we should strive for simplicity and uniformity
> in NLeSc since that will enhance collaboration between the engineers. Learning new branching model should not be stand in a way
> of contributions. There are other branching models that might be more suitable for particular project. You can learn more obout
> those on [atlasian page](https://www.atlassian.com/git/tutorials/comparing-workflows)

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

- [semantic versioning](http://semver.org/)
> Semantic Versioning is the most accepted and used way to add numbers to software versions. It is a way of communicating impact of
> changes in the software on users, therefore it should be used in any software has users, internal or external. 

- tagged releases ([github releases](https://help.github.com/categories/releases/))
> Releases are a way to signify and point to particular milestone in software development.
> Read more about releases here:[]()

- CHANGELOG.md ([Keep a CHANGELOG](http://keepachangelog.com/))
> Change log if a way to communicate notable changes in release. Every release shoould have relevant entry in change log.

- one command install ([pip](https://pypi.python.org/pypi/pip), [npm](https://www.npmjs.com/package/npm) etc)
> This applies to software which is distributed as independent package or library that will be used by other software. Should be
> implemented when there are (going to be) first users of the software.

- package in package manager ([pypi](https://pypi.python.org/pypi), [npm](https://www.npmjs.com/) etc)
> Look at previous point.

- discuss release cycle with coordinator
> Release cycles will depend on the project specifics, but in general we encourage quick agile development and therefore frequent
> releases.

- release quick-scan by other engineer (is documentation understandable, can it be installed, etc)
> Think of it as kind of code review but with focus on mechanics, not code. The reviewer should check if: (i) there is easily visible
> documentation, (ii) download works, (iii) there are instructions on how to start using software, some of the things that could be
> part of this scan can be automated with continuous integration.

- notify Lode for dissemination (news item on site / annual report, etc)
> News item should be made for at least first stable and subsequent major releases (the ones with major change in semantic versioning)

> Read more about releases [here](http://www.apache.org/dev/release.html)

## Licensing

- [Apache 2 license](http://www.apache.org/licenses/LICENSE-2.0)
> Apache 2.0 is the default choice for the NLeSC software license. Other license can be used in special cases, when software has
> already attached license or there are commercial partners that require different licensing. In general those kind of projects are
> discouraged.

- compatible license of all libraries
> All software used in the project HAS TO HAVE compatible licenses. Compatibility should be checked when new external code is added to
> the project.  
- `NOTICE(.txt|.md)` listing licenses, request citation of paper if applicable
> Read more [here](http://www.apache.org/dev/licensing-howto.html)

## Communication

- home page with all the necessary introduction information, links to documenation, source code (github) and latest release
  download (eg. [github.io pages](https://pages.github.com/))
> Home page should be created together with first release, the latest. It is contact point to the outside word (or other internal
> developer) it should be targeted towards non-programming users (unless software is meant for programers i.e library) but should have
> pointers for developers to more advanced resources

- project discussion list (github issues, mailing list, not private email) for all project related
  discussions from the beginning of the project
> There should be no private discussions about the project. Therefore once discussions are started (in the email), either move them to
> github issues or if they don’t fit into issues format any more, create mailing list.

- for services: a demo docker image in dockerhub (with Dockerfile)
> If software is the service Docker image should be created at the very early stage. This will allow for easier testing and platform
> independent use.

- for websites: an online demo
> Online demo should be available since first release.

- Pitch presentation (1 to 3 slides)
> Pitch presentation should be prepared when visible results of the software are available. It is important to keep those up to date
> and that other engineers have easy access to it.

- Few sentences about the project for [nlesc technology pages](https://www.esciencecenter.nl/technology)
> Short description of the project should be provided from the beginning of the project. Starting with requirements and should be
> updated regularly.

## Testing

- [unit tests](https://en.wikipedia.org/wiki/Unit_testing)
> Once the project leaves early prototyping / throwaway phase, unit tests should be implemented.

- [continuous integration](https://en.wikipedia.org/wiki/Continuous_integration) (CI), public on [Travis](https://travis-ci.org/)
> CI meaning: compile, unit test, integration test, quality analysis etc.
> Once there is some build process established and tests set up, CI should be configured too. It will save you a lot of time debugging
> and allow for much quicker problem diagnosis.

- continuous code coverage and code quality metrics public, minimum 70% coverage required

- end2end test for (web) user interfaces. [example with protrctor and angular](https://angular.github.io/protractor/#/)
> Once there are possible interactions via web interface, e2e tests should be implemented.

- track dependencies (with [VersionEye](https://www.versioneye.com/),
  [David](https://david-dm.org/) or other service depending on codebase language)
> Checking for dependency updates should be done regularly. It can save a lot of time, avoiding code dependent on deprecated
> functionality.

## Documentation
- `README.md` - clear explanation of the goal of the project with pointers to other documentation resources.
> Use [GitHub flavored markdown](https://help.github.com/categories/writing-on-github) for, e.g.,
> [syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks).
> Keeping basic documentation in README.md can be even usefull for lead developer, to track steps and design decisions.
> Therefore it should be present from the beginning of the project, when initialising git repository.
> [StackOverflow on good redme](http://stackoverflow.com/questions/2304863/how-to-write-a-good-readme),
> [short gist with README.md template](https://gist.github.com/jxson/1784669)

- well defined functionality
> Idealy in README.md

- source code documentation

- usage documentation

- documented development setup
> (good example is
> [Getting started with khmer development](http://khmer.readthedocs.org/en/latest/dev/getting-started.html))
> It should be made available once there is more than one developer working on the codebase.

- contribution guidelines [egzample](https://github.com/angular/angular.js/blob/master/CONTRIBUTING.md)
> Guidelines should be made available once the code is available online and there is a process for external contributions. External
> contributions not necessary mean ‘out of NLeSC’ it could be other engineer in NLeSC. good guidelines will save time of both lead
> developer and contributor since things have to be explained only once.

- code of conduct ([contributor covenant](http://contributor-covenant.org/))
> CofC should be attached from the beginning of the project, it does not cost anything to add it to the project and can come handy
> once there is one more than one person working on the project.

- documented code style
> From the beginning of the project, decision on the code style has to be made and then it should be documented. Not having documented
> code style will highly increase the chance of inconsistent style across the codebase, even when only one developer writes code.

- meaning of issue labels used
> Once users start submitting issues labels have to be documented.

- DOI or PID ([making your code citable](https://guides.github.com/activities/citable-code/))
> Identifiers should be associated with releases and should be created together with first release.

## Development setup

- using the NLeSC coding style is required
> NLeSC should have sane suggestion of coding style for each programming languege in use in NLeSC. 

- [editorconfig](http://editorconfig.org/)
> Using editor config is not necessary, but saves a lot of time and keeps developers from straying from the style choice and helps to
> avoid some formating caused problems (line ending differences, tabs vs spaces)

- applied code style in automated way if possible (i.e using linters and code formaters)
> Use of linters will not only help to keep code cleaner but will also help finding bugs

- dev environment docker images in Dockerhub (with Dockerfile)
> This can be very helpful in case of complicated development environment setup and when you want to help developers quickly start
> with contributions without struggling with setup

## Use standards

- exchange format (Unicode, W3C, OGN, NetCDF, etc)
- protocols (HTTP, TCP, TLS, etc)

> Standard files and protocols should always be a primary choice.

