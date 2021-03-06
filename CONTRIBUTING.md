<!--

Thank you for contributing changes to this document! Because we use a central repository
to synchronize this file across all our repositories, make sure to make your edits
in the correct file, which you can find here:

https://github.com/ory/meta/blob/master/templates/repository/CONTRIBUTING.md

-->

# Contributing to ORY {{Project}}

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Introduction](#introduction)
- [Contributing Code](#contributing-code)
- [Disclosing vulnerabilities](#disclosing-vulnerabilities)
- [Code Style](#code-style)
- [Documentation](#documentation)
- [Pull request procedure](#pull-request-procedure)
- [Communication](#communication)
- [Conduct](#conduct)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Introduction

Please note: We take ORY {{Project}}'s security and our users' trust very
seriously. If you believe you have found a security issue in ORY {{Project}},
please responsibly disclose by contacting us at security@ory.sh.

First: if you're unsure or afraid of anything, just ask or submit the issue or
pull request anyways. You won't be yelled at for giving it your best effort. The
worst that can happen is that you'll be politely asked to change something. We
appreciate any sort of contributions, and don't want a wall of rules to get in
the way of that.

That said, if you want to ensure that a pull request is likely to be merged,
talk to us! You can find out our thoughts and ensure that your contribution
won't clash or be obviated by ORY {{Project}}'s normal direction. A great way to
do this is via the [ORY Community](https://community.ory.sh/) or join the
[ORY Chat](https://www.ory.sh/chat).

## Contributing Code

Unless you are fixing a known bug, we **strongly** recommend discussing it with
the core team via a GitHub issue or [in our chat](https://www.ory.sh/chat)
before getting started to ensure your work is consistent with ORY {{Project}}'s
roadmap and architecture.

All contributions are made via pull request. Note that **all patches from all
contributors get reviewed**. After a pull request is made other contributors
will offer feedback, and if the patch passes review a maintainer will accept it
with a comment. When pull requests fail testing, authors are expected to update
their pull requests to address the failures until the tests pass and the pull
request merges successfully.

At least one review from a maintainer is required for all patches (even patches
from maintainers).

Before your contributions can be merged you need to sign our [Contributor License Agreement](https://cla-assistant.io/ory/).

This agreement defines the terms under which your code is contributed to ORY.
More specifically this enables ORY to make use of your contributions to the
projects without legal repercussions. You can see the Apache 2.0 license under
which our projects are published [here](https://github.com/ory/meta/blob/master/LICENSE).

Reviewers should leave a "LGTM" comment once they are satisfied with the patch.
If the patch was submitted by a maintainer with write access, the pull request
should be merged by the submitter after review.

## Disclosing vulnerabilities

Please disclose vulnerabilities exclusively to
[security@ory.sh](mailto:security@ory.sh). Do not use GitHub issues.

## Code Style

Please follow these guidelines when formatting source code:

- Go code should match the output of `gofmt -s` and pass `golangci-lint run`.
- NodeJS and JavaScript code should be prettified using `npm run format` where
  appropriate.

## Documentation

Please provide documentation when changing, removing, or adding features.
Documentation resides in the project's [docs](docs) folder. Generate API and
configuration reference documentation using `cd docs; npm run gen`.

For further instructions please head over to [docs/README.md](docs/README.md).

## Pull request procedure

To make a pull request, you will need a GitHub account; if you are unclear on
this process, see GitHub's documentation on
[forking](https://help.github.com/articles/fork-a-repo) and
[pull requests](https://help.github.com/articles/using-pull-requests). Pull
requests should be targeted at the `master` branch. Before creating a pull
request, go through this checklist:

1. Create a feature branch off of `master` so that changes do not get mixed up.
1. [Rebase](http://git-scm.com/book/en/Git-Branching-Rebasing) your local
   changes against the `master` branch.
1. Run the full project test suite with the `go test ./...` (or equivalent)
   command and confirm that it passes.
1. Run `gofmt -s` (if the project is written in Go).
1. Ensure that each commit has a subsystem prefix (ex: `controller:`).

Pull requests will be treated as "review requests," and maintainers will give
feedback on the style and substance of the patch.

Normally, all pull requests must include tests that test your change.
Occasionally, a change will be very difficult to test for. In those cases,
please include a note in your commit message explaining why.

### Working with Forks

```
# First you clone the original repository
git clone git@github.com:ory/{{Project}}.git

# Next you add a git remote that is your fork:
git remote add fork git@github.com:<YOUR-GITHUB-USERNAME-HERE>/{{Project}}.git

# Next you fetch the latest changes from origin for master:
git fetch origin
git checkout master
git pull --rebase

# Next you create a new feature branch off of master:
git checkout my-feature-branch

# Now you do your work and commit your changes:
git add -A
git commit -a -m "fix: this is the subject line" -m "This is the body line. Closes #123"

# And the last step is pushing this to your fork
git push -u fork my-feature-branch
```

Now go to the project's GitHub Pull Request page and click "New pull request"

## Communication

We use [Slack](https://www.ory.sh/chat). You are welcome to drop in and ask
questions, discuss bugs, etc.

## Conduct

Whether you are a regular contributor or a newcomer, we care about making this
community a safe place for you and we've got your back.

- We are committed to providing a friendly, safe and welcoming environment for
  all, regardless of gender, sexual orientation, disability, ethnicity,
  religion, or similar personal characteristic.
- Please avoid using nicknames that might detract from a friendly, safe and
  welcoming environment for all.
- Be kind and courteous. There is no need to be mean or rude.
- We will exclude you from interaction if you insult, demean or harass anyone.
  In particular, we do not tolerate behavior that excludes people in socially
  marginalized groups.
- Private harassment is also unacceptable. No matter who you are, if you feel
  you have been or are being harassed or made uncomfortable by a community
  member, please contact one of the channel ops or a member of the ORY
  {{Project}} core team immediately.
- Likewise any spamming, trolling, flaming, baiting or other attention-stealing
  behaviour is not welcome.

We welcome discussion about creating a welcoming, safe, and productive
environment for the community. If you have any questions, feedback, or concerns
[please let us know](https://www.ory.sh/chat).
