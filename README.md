<h1 align="center">All Contributors Auto Action</h1>

<p align="center">Fills in missing allcontributors entries for a repository. 👪</p>

<p align="center">
	<a href="#contributors" target="_blank">
<!-- prettier-ignore-start -->
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
<img alt="All Contributors: 2" src="https://img.shields.io/badge/all_contributors-2-21bb42.svg" />
<!-- ALL-CONTRIBUTORS-BADGE:END -->
<!-- prettier-ignore-end -->
	</a>
	<a href="https://codecov.io/gh/JoshuaKGoldberg/all-contributors-auto-action" target="_blank">
		<img alt="Codecov Test Coverage" src="https://codecov.io/gh/JoshuaKGoldberg/all-contributors-auto-action/branch/main/graph/badge.svg"/>
	</a>
	<a href="https://github.com/JoshuaKGoldberg/all-contributors-auto-action/blob/main/.github/CODE_OF_CONDUCT.md" target="_blank">
		<img alt="Contributor Covenant" src="https://img.shields.io/badge/code_of_conduct-enforced-21bb42" />
	</a>
	<a href="https://github.com/JoshuaKGoldberg/all-contributors-auto-action/blob/main/LICENSE.md" target="_blank">
		<img alt="License: MIT" src="https://img.shields.io/github/license/JoshuaKGoldberg/all-contributors-auto-action?color=21bb42">
	</a>
	<img alt="Style: Prettier" src="https://img.shields.io/badge/style-prettier-21bb42.svg" />
	<img alt="TypeScript: Strict" src="https://img.shields.io/badge/typescript-strict-21bb42.svg" />
</p>

<img align="right" alt="Project logo: the light purple wreath from the All Contributors logo, with a purple 'play' triangle from the GitHub Actions default icon" src="./all-contributors-auto-action.png" height="128px" width="128px">

## Usage

This action will:

1. Ask [`all-contributors-for-repository`](https://github.com/JoshuaKGoldberg/all-contributors-for-repository) to collect the current repository's contributors
2. Post [`@all-contributors add` bot comments](https://allcontributors.org/docs/en/bot/usage) in the newest issues and PRs for each contributor

> **Warning**
> This tool only sees contributions that can be detected from the last 500 events in GitHub's API.
> Don't forget to manually add in other forms of contributions!

For example, the following job will run on every push to `main`:

```yml
# .github/workflows/contributors.yml
jobs:
  contributors:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: JoshuaKGoldberg/all-contributors-auto-action@v0.3.2

name: Contributors

on:
  push:
    branches:
      - main
```

...and will post comments like the following automatically:

> @all-contributors please add @JoshuaKGoldberg for code.
>
> > 🤖 Beep boop! This comment was added automatically by [all-contributors-auto-action](https://github.com/marketplace/actions/all-contributors-auto-action).
> >
> > Not all contributions can be detected from Git & GitHub alone.
> > Please comment any missing contribution types this bot missed.
> >
> > ...and of course, thank you for contributing! 💙

## Development

See [`.github/CONTRIBUTING.md`](./.github/CONTRIBUTING.md), then [`.github/DEVELOPMENT.md`](./.github/DEVELOPMENT.md).
Thanks! 💖

## Contributors

<!-- spellchecker: disable -->
<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tbody>
    <tr>
      <td align="center" valign="top" width="14.28%"><a href="https://johnnyreilly.com/"><img src="https://avatars.githubusercontent.com/u/1010525?v=4?s=100" width="100px;" alt="John Reilly"/><br /><sub><b>John Reilly</b></sub></a><br /><a href="#ideas-johnnyreilly" title="Ideas, Planning, & Feedback">🤔</a></td>
      <td align="center" valign="top" width="14.28%"><a href="http://www.joshuakgoldberg.com"><img src="https://avatars.githubusercontent.com/u/3335181?v=4?s=100" width="100px;" alt="Josh Goldberg"/><br /><sub><b>Josh Goldberg</b></sub></a><br /><a href="#tool-JoshuaKGoldberg" title="Tools">🔧</a></td>
    </tr>
  </tbody>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->
<!-- spellchecker: enable -->

<!-- You can remove this notice if you don't want it 🙂 no worries! -->

> 💙 This package is based on [@JoshuaKGoldberg](https://github.com/JoshuaKGoldberg)'s [create-typescript-app](https://github.com/JoshuaKGoldberg/create-typescript-app).
