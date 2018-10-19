---
title: Generating changelog
comments: true
---

## GitHub PR title

### Title Format

Github PR title has a special format that includes a type and a subject:

```html
<type>: <subject>
```

### PR types

Following are the conventional PR types that you can use while creating a PR:

| Commit Type | Description                                                                                                 |
| ----------- | ----------------------------------------------------------------------------------------------------------- |
| `feat`      | A new feature                                                                                               |
| `fix`       | A bug Fix                                                                                                   |
| `docs`      | Documentation only changes                                                                                  |
| `style`     | Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)      |
| `refactor`  | A code change that neither fixes a bug nor adds a feature                                                   |
| `perf`      | A code change that improves performance                                                                     |
| `test`      | Adding missing tests or correcting existing tests                                                           |
| `build`     | Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)         |
| `ci`        | Changes to our CI configuration files and scripts (example scopes: Travis, Circle, BrowserStack, SauceLabs) |
| `chore`     | Other changes that don't modify src or test files                                                           |
| `revert`    | Reverts a previous commit                                                                                   |

### Example PR titles:

* Added a new feature:
  ```markdown
  feat: Added support to read config from file. Closes #1.
  ```

* A bug fix for an existing feature:
  ```markdown
  fix: minor typos in code
  ```

* Updated documentation:
  ```markdown
  docs: Updated the README.
  ```

* Update or add tests:
  ```markdown
  test: Add missing tests.
  ```

## Generating Changelog

### Getting started

We use [git-chlog](https://github.com/git-chglog/git-chglog) to generate the changelog for the git repository.

> You must follow the PR title convention described in the previous section for this tool to work

### Installation

Inside your terminal and run the following command:

```
brew tap git-chglog/git-chglog
brew install git-chglog
```

### Usage

This tool requires a configuration file and a template to generate the changelog for the git repository. To get the configuration file run the following command and follow the steps:

```
git-chglog --init
```

## Generating changelog

To generate the changelog file run the follwing command it will generate the `CHANGELOG.md` file:

```
git-chglog -o CHANGELOG.md
```

## Changelog:

Changelog will look like this for the commits shown inside the commit messages page:

    Changelog
    =========
    
    ## [1.0.0](<https://github.com/some_user/some_repository/compare/v1.0.0...v0.0.1>) (2018-10-18)
    
    ### Bug fixes
    
    * Minor typos in code. ([a5ecd4d](<https://github.com/some_user/some_repository/commit/adc59ed>))
    
    ### Features
    
    * Added support to read config from file. Closes [#1](<https://github.com/some_user/some_repository/issue/1>). ([adc59ed](<https://github.com/some_user/some_repository/commit/adc59ed>))
    
    ### Tests
    
    * Add missing tests. ([a5ecd4d](<https://github.com/some_user/some_repository/commit/adc59ed>))
    
    ### Docs
    
    * Updated the README. ([a5ecd4d](<https://github.com/some_user/some_repository/commit/adc59ed>))