# Semantic Release

[Semantic release](https://github.com/semantic-release/semantic-release) facilitates fully automated release workflow. It determines the next release version number, autogenerates release notes and publishes the package.

Semantic release internally uses commit messages to determine the versions and the changelog. The table below shows which commit message gets you which release type when `semantic-release` runs:

| Commit message                                                                                                                                                                                   | Release type               |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------- |
| `fix(pencil): stop graphite breaking when too much pressure applied`                                                                                                                             | ~~Patch~~ Fix Release      |
| `feat(pencil): add 'graphiteWidth' option`                                                                                                                                                       | ~~Minor~~ Feature Release  |
| `perf(pencil): remove graphiteWidth option`<br><br>`BREAKING CHANGE: The graphiteWidth option has been removed.`<br>`The default graphite width of 10mm is always used for performance reasons.` | ~~Major~~ Breaking Release <br /> (Note that the `BREAKING CHANGE: ` token must be in the footer of the commit) |


## Links:

1. [Installation](https://github.com/semantic-release/semantic-release/blob/master/docs/usage/installation.md#installation)
2. [CI Configuration](https://github.com/semantic-release/semantic-release/blob/master/docs/usage/ci-configuration.md#ci-configuration)
    - [GitHub Actions](https://github.com/semantic-release/semantic-release/blob/master/docs/recipes/ci-configurations/github-actions.md)
3. [Configuration](https://github.com/semantic-release/semantic-release/blob/master/docs/usage/ci-configuration.md#ci-configuration) - Creating a `.relaserc` file.
4. [Plugins](https://github.com/semantic-release/semantic-release/blob/master/docs/usage/plugins.md#plugins-declaration-and-execution-order) - Commit Analyzer, Release Notes Generator and Git

> Note: The release workflow should always be run after a CI job to ensure working releases are pushed to production 