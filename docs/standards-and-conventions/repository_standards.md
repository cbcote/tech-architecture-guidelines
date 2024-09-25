# Repository Standards

This document outlines the standards and conventions for repositories in the organization. Adhering to these standards will ensure consistency, maintainability, and quality across all projects.

## Purpose
The purpose of this document is to provide guidelines for contributors on how to effectively collaborate within the organizations code repositories. By following these standards, we aim to streamline our development processes, facilitate code reviews, and ensure the quality of our codebase.

## Scope
This documentation applies to all team members and contributors involved in projects. It covers essential aspects of repository management, including branching strategies, commit messages, pull requests, and more.

## Standard Files
- README.md
- DEPRECATED.md
- CONTRIBUTING.md

## Branching Strategy
Create a table with columns Branch Type, Naming Convention, and Description
| Branch Type | Naming Convention | Description |
| ----------- | ----------------- | ----------- |
| master | master, master | The main branch of the repository. This is the trunk in Trunk Based Development. All new code and features are merged into this branch regularly. |
| development | development | The branch for development.  This is a staging branch, derived from the master branch. Relevant for testing a complete feature. |
| feature | feature/\<name> | The branch for a new feature. Temporary branch for developing new features. Feature branches should be short-lived, regulary integrated into the development branch, and deleted afterward. |
| bug | bug/\<name> | The branch for a bug fix. Temporary branches for fixing bugs. Naming includes the issue ID (if using issue tracker) and short description of the bug. |
| hotfix | hotfix/\<name> | The branch for a hotfix. Used for urgent fixes that need to be applied directly to the main branch. Usually created off the main branch, fixed, tested, and merged back. |
| release | release/\<version> | The branch for a release. Created from the main branch to prepare for a production release. These are short-lived branches where final bug fixes and release task happen. |
| docs | docs/\<name> | Placeholder |
| test | test/\<name> | Placeholder |
| chore | chore/\<name> | Placeholder |
| ci | ci/\<name> | Placeholder |
| build | build/\<name> | Placeholder |
| security | security/\<name> | Placeholder |

## Merge Strategy

## Commit Messages
| Commit Type | Format | Example | Description |
| ----------- | ------ | ------- | ----------- |
| Feature | feat: [description] | feat: add user login | A new feature added to the application. |
| Fix | fix: [description] | fix: fix user login | A bug fix that resolves and issue. |
| Documentation | docs: [description] | docs: update README with setup instructions | Documentation changes or additions. |
| Refactor | refactor: [description] | refactor: refactor user login code | Code changes that neither fixes a bug nor adds a feature. |
| Test | test: [description] | test: add user login test | Changes related to testing. |
| Chore | chore: [description] | chore: update dependencies | Routine tasks that do not fit into the above categories. |

## Pull Requests
Create a table with columns Section, Format, Example, and Description
| Section | Format | Example | Description |
| ------- | ------ | ------- | ----------- |
| Title | [\<type>] \<description> | [feat] add user login | The title of the pull request. |
| Description | \<description> | add user login feature | A brief description of the changes made in the pull request. |
| Issue | fixes #\<issue> | fixes #1 | The issue number that the pull request is related to. |
| Reviewers | @\<username> | @user1, @user2 | The reviewers assigned to the pull request. |
| Labels | \<label> | bug, enhancement | The labels assigned to the pull request. |
| Milestone | \<milestone> | v1.0 | The milestone assigned to the pull request. |
| Projects | \<project> | project1 | The project assigned to the pull request. |

## Code Review process

## Commit Frequency

## Issue Tracking

## Versioning

## Continuous Integration/Continuous Deployment (CI/CD)

## Coding Standards

## Documentation Standards

## Security Standards

## Testing Standards

## Repository Structure

## Contribution Guidelines