# How to contribute to Ignition

## Table of Contents

- [Maintainers](#maintainers)
- [Reporting Issues](#reporting-issues)
- [Feature Requests](#feature-requests)
- [Submitting Changes](#submitting-changes)
- [Issue and PR Lifecycle](#issue-and-pr-lifecycle)
- [Contributing to these guidelines](#contributing-to-these-guidelines)

## Maintainers

- Daniel Vaccaro-Senna [@dvaccarosenna](https://github.com/dvaccarosenna)
- Craig Howarth [@chowarth123](https://github.com/chowarth123)
- Steve Glover [@sglover](https://github.com/sglover)

## Reporting Issues

Firstly, consider the following:

- Ensure you are using the latest version or any version you believe is considered compatible with your current version of CP4NA

- Check the existing list of [issues](https://github.com/IBM/ignition/issues) to see if the bug you've found has already been reported.

When reporting a bug, please include:

- A description of the expected behaviour
- A description of the actual behaviour
- The steps to reproduce the issue
- Full stack trace/log files where possible
- A description of your environment:
    - If running locally, include: Python version, Operating System, CP4NA version
    - If running on OCP/Kubernetes, include: OCP/Kubernetes version, Docker image version, CP4NA version
- The `bug` label

## Feature Requests

Firstly, check the existing list of [issues](https://github.com/IBM/ignition/issues) to see if the feature has already been requested. Feel free to upvote the issue to add your support but only add comments if you intend to add to the idea, give feedback or provide additional use cases/reasons why the feature is valuable.

When requesting a feature, please include:

- A detailed description of the proposed functionality
- A description of the value or intended use case for the feature
- If possible, a rough description of the changes you believe this would require (either high level or low level code is ok)
- The `enhancement` label

## Submitting Changes

If you intend to contribute changes to this project, be sure to read the [developer docs](developer_docs/setup_developer_env.md) to setup your local development environment.

Before submitting changes, please complete the following:

- Ensure there is an open issue for your intended change. If not, raise one **before** starting work, as this allows other users/maintainers to give feedback on the suggested idea before you make changes.

- Assign yourself to the issue so others are aware it's being worked on

When working on the changes, please complete the following:

- Create a branch for your work based off the `develop` branch (**not** `master`). The `develop` branch is used for ongoing development and is merged to `master` when releases are finalised. 

- Name your branch `issue/<issue number>` where `issue number` corresponds to the unique ID of the issue e.g. work on [issue#104](https://github.com/IBM/ignition/issues/104) was completed on branch [issue/104](https://github.com/IBM/ignition/pull/105)

- Include relevant tests along with your code changes. Tests are organised by package and module under `tests/unit`, so if you changed a module, find it's corresponding test file (if there isn't one, create one).

- Read the [testing docs](developer_docs/testing.md) for instructions on how to run the unit tests. Make sure these pass before raising your PR

- Read the [build docs](developer_docs/setup_developer_env.md#build-ignition) for instructions on how to build the `whl` for this project so you may use it with a driver, to test on a real environment.

 When submitting a pull request, please complete the following:

- Create the [pull request on Github](https://github.com/IBM/ignition/compare) with `base: develop` and `compare: your-branch`. 

- In the description of your PR add `Fixes #issue-number` e.g. `Fixes #104` 

- Assign the PR to the maintainers of this project (see start of this document)

- Monitor the PR for comments/approval, responding to any suggested changes. Once at least one maintainer has approved the PR it will be merged when deemed appropriate (usually on approval but there may be rare cases where changes are put on hold).

## Issue and PR Lifecycle

Maintainers will manage the lifecycle of all issues and PRs, this includes:

- assigning/adjusting milestones
- assigning/adjusting tags
- closing issues
- merging/closing PRs

## Contributing to these guidelines

There's still a lot missing from these guidelines, such as:

- Code Style guidelines (or even better, a pre-commit hook to automatically format code)
- Mailing list/forum to ask questions

If you have any ideas to improve these guidelines, then follow the same process as a feature enhancement by raising an issue and proposing your suggestions. These can be discussed and then, where applicable, changes can be made and a PR raised (using the same process as for code changes).