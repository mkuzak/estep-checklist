Checklist for 'eStep friendly' projects.

## Version control

- version control from the beginning of the project
- use git as vcs
- use [github flow branching model](https://guides.github.com/introduction/flow/)
- public vcs repository (github)
- meaningful commit messages

## Release

- [semantic versioning](http://semver.org/)
- tagged releases
- one command install (pip, npm etc)
- package in package manager (pypi, npm etc)
- discuss with coordinator
- release quick-scan by other engineer (is documentation understandable, can it be installed, etc)
- notify Lode for dissemination (news item on site / annual report, etc)

## Licensing

- Apache 2 license
- compatible license of all libraries
- NOTICE(.txt|.md) listing licenses, request citation of paper if applicable

## Communication

- project discussion list (github issues or gitter not private email) for all project related discussions from the beginning of the project
- for services: a demo docker image in dockerhub (with Dockerfile)
- for websites: an online demo
- Pitch presentation (max 1 to max 3 slides)

## Testing

- unit tests
- regression tests
- build tests
- continuous integration, public on Travis
- continuous code coverage and code quality metrics public, minimum 70% coverage required
- end2end test for (web) user interfaces

## Documentation
- `README.md` - clear explanation of the goal of the project with pointers to other documentation resources
- well defined functionality
- source code documentation
- usage documentation
- documented development setup (good example is [Getting started with khmer development](http://khmer.readthedocs.org/en/latest/dev/getting-started.html))
- contribution guidelines
- documented code style
- meaning of issue labels used
- DOI

## Development setup

- using the NLeSC coding style is required
- editorconfig
- applied code style in automated way if possible (i.e using linters and code formaters)
- dev environment docker images in Dockerhub (with Dockerfile)

## Use standards
- exchange format (Unicode, W3C, OGN, NetCDF, etc)
- protocols (HTTP, TCP, TLS, etc)
