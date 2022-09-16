# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [2.1.0] - 2022-09-16

## [2.0.0] - 2020-10-17

### Changed

-   Use `workflow_dispatch` instead of opening an issue as the initial trigger of the release.
    Not only is this more convenient to use, it also fixes a security vulnerability that may have allowed users without write access to execute arbitrary code within the context of the repositories GitHub action.
-   Merge `master` in `dev` after a release branch is merged.
    Previously, we used to merge the `release` branch back into `dev`.
    However, this caused some issues because the actual merge commit was not present in the `dev` branch.
    It also prevented use of the "automatically delete head branch" feature of GitHub which works well together with the "PR retargeting" feature.

## [1.4.0] - 2020-02-22

### Added

-   A whitelist of which users can trigger the release workflow.

## [1.3.0] - 2020-02-22

### Added

-   Automatically close the release issue after the release branch was merged.

## [1.2.0] - 2020-02-17

### Changed

-   Don't request reviews from pull request author for merging release branch back into dev.
    The author of the PR is github-actions[bot], we can request a review from them.
-   Don't make a separate commit for updating the version of package.json

## [1.1.0] - 2020-02-17

### Added

-   GitHub action to backport releases to dev branch

### Fixed

-   Merge commit is used to tag release instead of last commit on release branch

## [1.0.0] - 2020-02-15

### Added

-   Everything since the beginning!

[Unreleased]: https://github.com/thomaseizinger/github-action-gitflow-release-workflow/compare/2.1.0...HEAD

[2.1.0]: https://github.com/thomaseizinger/github-action-gitflow-release-workflow/compare/2.0.0...2.1.0

[2.0.0]: https://github.com/thomaseizinger/github-action-gitflow-release-workflow/compare/1.4.0...2.0.0

[1.4.0]: https://github.com/thomaseizinger/github-action-gitflow-release-workflow/compare/1.3.0...1.4.0

[1.3.0]: https://github.com/thomaseizinger/github-action-gitflow-release-workflow/compare/1.2.0...1.3.0

[1.2.0]: https://github.com/thomaseizinger/github-action-gitflow-release-workflow/compare/1.1.0...1.2.0

[1.1.0]: https://github.com/thomaseizinger/github-action-gitflow-release-workflow/compare/1.0.0...1.1.0

[1.0.0]: https://github.com/thomaseizinger/github-action-gitflow-release-workflow/compare/794c3ba521cae6b168def8bdbfe1aa6a2c285257...1.0.0
