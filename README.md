README

Setting up the Tech Task API project
What is this repository for?

    Tech Task API common
    0.0.1

How do I get set up?

    clone the code from the following repository address : https://bitbucket.org/helecloud/billing-api-spec/src/master/
    Make sue you have JAVA 17
    Run ./gradlew build to build the project and run the unit tests
    Database configuration - TBD
    How to run tests : TBD
    Deployment instructions : TBD

Contribution guidelines

    Writing tests
    Code review
    Other guidelines

Who do I talk to?

    Repo owner or admin
    Other community or team contact

Semantic-release tool
How does it work?
Commit message format

semantic-release uses the commit messages to determine the consumer impact of changes in the codebase. Following formalized conventions for commit messages, semantic-release automatically determines the next semantic version number, generates a changelog and publishes the release.

By default, semantic-release uses Angular Commit Message Conventions. The commit message format can be changed with the preset or config options of the @semantic-release/commit-analyzer and @semantic-release/release-notes-generator plugins.

Tools such as commitizen or commitlint can be used to help contributors and enforce valid commit messages.

The table below shows which commit message gets you which release type when semantic-release runs (using the default configuration):
Commit message 	Release type
fix(pencil): stop graphite breaking when too much pressure applied 	Patch Fix Release
feat(pencil): add 'graphiteWidth' option 	Minor Feature Release
perf(pencil): remove graphiteWidth option

BREAKING CHANGE: The graphiteWidth option has been removed.
The default graphite width of 10mm is always used for performance reasons. 	Major Breaking Release
(Note that the BREAKING CHANGE: token must be in the footer of the commit)

    The Header The header is a mandatory line that simply describes the purpose of the change (up to 100 characters).

Better yet, it consists of three parts in itself:

    Type - a short prefix that represents the kind of the change
    Scope - optional information (attached to the prefix) that represents the context of the change
    Subject - represents a concise description of the actual change

Practically, in terms of Git, it’s merely the first line of the commit message:

git commit -m "fix(core): remove deprecated and defunct wtf* apis"

Configuration file

semantic-release’s options, mode and plugins can be set via either: - A .releaserc file, written in YAML or JSON, with optional extensions: .yaml/.yml/.json/.js - A release.config.js file that exports an object - A release key in the project's package.json file

Alternatively, some options can be set via CLI arguments.

The following three examples are the same.

    Via release key in the project's package.json file:

    {
      "release": {
        "branches": ["master", "next"]
      }
    }

    Via .releaserc file:

    {
      "branches": ["master", "next"]
    }

