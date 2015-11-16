Checklist for 'eStep friendly' projects.

## Version control

- version control from the beginning of the project
- use git as vcs
- use [githum flow branching model](https://guides.github.com/introduction/flow/)
- public vcs repository (github)

## Release

- [semantic versioning](http://semver.org/)
- tagged releases
- one command install (pip, npm etc)
- package in package manager (pypi, npm etc)

## Licensing

- Apache 2 license
- compatible license of all libraries
- NOTICE(.txt|.md) listing licenses

## Communication

- project discussion list (github issues or gitter not private email) for all project related discussions from the beginning of the project
- for services: a demo docker image in dockerhub (with Dockerfile)
- for websites: an online demo

## Testing

- unit tests
- regression tests
- build tests
- continuous integration, public on Travis
- continuous code coverage and code quality metrics public
- end2end test for (web) user interfaces

## Documentation

- well defined functionality
- source code documentation
- usage documentation
- development setup documentation
- instructions on how to get started with development (good example is [Getting started with khmer development](http://khmer.readthedocs.org/en/latest/dev/getting-started.html))
- documented code style

## Development setup

- editorconfig
- applied code style in automated way if possible (i.e using linters and code formaters)
- dev environment docker images in Dockerhub (with Dockerfile)

## Use standards
- exchange format (Unicode, W3C, OGN, NetCDF, etc)
- protocols (HTTP, TCP, TLS, etc)
