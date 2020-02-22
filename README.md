# poPR: Find potential Pull Requests

[![Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![CodeScene Code Health](https://codescene.io/projects/7153/status-badges/code-health)](https://codescene.io/projects/7153)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=katrinleinweber_poPR&metric=alert_status)](https://sonarcloud.io/dashboard?id=katrinleinweber_poPR)

> I believe it is worthwhile trying to discover more about the
> [octoverse], even if this only teaches us how little we
> [have merged].
>
> -- liberally quoted from: [Karl Popper's _Conjectures and Refutations: The Growth of Scientific Knowledge_ (1963)](https://en.wikiquote.org/wiki/Karl_Popper#Conjectures_and_Refutations:_The_Growth_of_Scientific_Knowledge_(1963))

This tool helps maintainers observe all forks of a given repository.
It finds branches that could be sent upstream by their authors,
but weren't (for whatever reason).
Thus, _poPR_ helps to review forked code, in order to merge or cherry-pick it.

## Install & use

> git clone https://github.com/katrinleinweber/poPR
> cd poPR 
> python3 main.py --origin=namespace/repo

The script will find all branches in all forks and prompt you to open GitHub's
own comparison page to review the changes with the option to start a PR.
This approach aims to keep code complexity and the number of API requests low.

To analyse larger repositories, create a [Personal Access Token][PAT]
with at least the `public_repo` scope and and pass it with the `--PAT=` option.

[PAT]: https://github.com/settings/tokens
