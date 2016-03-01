Checkmatrix for 'eStep friendly' projects.

This matrix shows what parts of the software sustainability checklist should be taken care of at(perhaps slightly before) what state of a project.

## Explanation of project states

- Day One: Always.
- Multiple Developers: As soon as someone (also within the same organization) starts helping out.
- Users: Please are using your code.
- Released: The software has a release
- External Contributors: Developers outside NLeSC contribute to your.
- Community Project: The software is actively used and contributed to by so many people that it becomes a community project rther than a NLeSC project.

These states do not neccesairily happen in order.

##Version Control

Item | Day one | Has multiple developers | Has users | Has a release | Has external contributors | Is a community project
-----|:-------:|:-----------------------:|:---------:|:-------------:|:-------------------------:|:---------------------:|
use git as version control system (vcs)|X
use [GitHub flow branching model](https://guides.github.com/introduction/flow/) (use feature branches and pull requests)|X
public vcs repository ([github](https://github.com/))|X
meaningful commit messages|X


##Releases

Item | Day one | Has multiple developers | Has users | Has a release | Has external contributors | Is a community project
-----|:-------:|:-----------------------:|:---------:|:-------------:|:-------------------------:|:---------------------:|
[semantic versioning](http://semver.org/)|X
tagged releases ([github releases](https://help.github.com/categories/releases/))|X
CHANGELOG.md ([Keep a CHANGELOG](http://keepachangelog.com/))|X
one command install ([pip](https://pypi.python.org/pypi/pip), [npm](https://www.npmjs.com/package/npm) etc)|X
package in package manager ([pypi](https://pypi.python.org/pypi), [npm](https://www.npmjs.com/) etc)|X
discuss release cycle with coordinator|X
release quick-scan by other engineer (is documentation understandable, can it be installed, etc)|X
notify Lode for dissemination (news item on site / annual report, etc)|X

##Licensing

Item | Day one | Has multiple developers | Has users | Has a release | Has external contributors | Is a community project
-----|:-------:|:-----------------------:|:---------:|:-------------:|:-------------------------:|:---------------------:|
[Apache 2 license](http://www.apache.org/licenses/LICENSE-2.0)|X
compatible license of all libraries|X
`NOTICE(.txt|.md)` listing licenses, request citation of paper if applicable|X

##Communication

Item | Day one | Has multiple developers | Has users | Has a release | Has external contributors | Is a community project
-----|:-------:|:-----------------------:|:---------:|:-------------:|:-------------------------:|:---------------------:|
home page with all the necessary introduction information, links to documenation, source code (github) and latest release download (eg. [github.io pages](https://pages.github.com/))|X
project discussion list (github issues, mailing list, not private email) for all project related discussions from the beginning of the project|X
for services: a demo docker image in dockerhub (with Dockerfile)|X
for websites: an online demo|X
Pitch presentation (1 to 3 slides)|X
Few sentences about the project for [nlesc technology pages](https://www.esciencecenter.nl/technology)|X

##Testing

Item | Day one | Has multiple developers | Has users | Has a release | Has external contributors | Is a community project
-----|:-------:|:-----------------------:|:---------:|:-------------:|:-------------------------:|:---------------------:|
[unit tests](https://en.wikipedia.org/wiki/Unit_testing)|X
build tests|X
[continuous integration](https://en.wikipedia.org/wiki/Continuous_integration), public on [Travis](https://travis-ci.org/)|X
continuous code coverage and code quality metrics public, minimum 70% coverage required|X
end2end test for (web) user interfaces|X
track dependencies (with [VersionEye](https://www.versioneye.com/), [David](https://david-dm.org/) or other service depending on codebase language)|X

##Documentation

Item | Day one | Has multiple developers | Has users | Has a release | Has external contributors | Is a community project
-----|:-------:|:-----------------------:|:---------:|:-------------:|:-------------------------:|:---------------------:|
`README.md` - clear explanation of the goal of the project with pointers to other documentation resources. Use [GitHub flavored markdown](https://help.github.com/categories/writing-on-github) for, e.g., [syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks).|X
well defined functionality|X
source code documentation|X
usage documentation|X
documented development setup (good example is [Getting started with khmer development](http://khmer.readthedocs.org/en/latest/dev/getting-started.html))|X
contribution guidelines [egzample](https://github.com/angular/angular.js/blob/master/CONTRIBUTING.md)|X
code of conduct ([contributor covenant](http://contributor-covenant.org/))|X
documented code style|X
meaning of issue labels used|X
DOI or PID ([making your code citable](https://guides.github.com/activities/citable-code/))|X


## Development setup

Item | Day one | Has multiple developers | Has users | Has a release | Has external contributors | Is a community project
-----|:-------:|:-----------------------:|:---------:|:-------------:|:-------------------------:|:---------------------:|
using the NLeSC coding style is required|X
[editorconfig](http://editorconfig.org/)|X
applied code style in automated way if possible (i.e using linters and code formaters)|X
dev environment docker images in Dockerhub (with Dockerfile)|X

## Use standards

Item | Day one | Has multiple developers | Has users | Has a release | Has external contributors | Is a community project
-----|:-------:|:-----------------------:|:---------:|:-------------:|:-------------------------:|:---------------------:|
exchange format (Unicode, W3C, OGN, NetCDF, etc)|X
protocols (HTTP, TCP, TLS, etc)|X
