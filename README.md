# TechTide AI Organization Profile

This is the **organization-profile and default community-health repository** for [TechTide AI](https://github.com/TechTideOhio). GitHub renders [`profile/README.md`](profile/README.md) on the organization page and can use the supported policy and template files in this public `.github` repository as defaults for repositories that do not provide their own versions.[1]

## Why this exists

**What it does.** Holds the organization profile that GitHub renders at [github.com/TechTideOhio](https://github.com/TechTideOhio) and the default community-health files (contributing, code of conduct, governance, security, support), issue forms, and a pull-request template that GitHub applies to TechTideOhio repositories that do not define their own. A read-only workflow lints Markdown and checks links on every change.

**Who it serves.** Visitors deciding whether TechTide AI's public repositories are worth their time, contributors who need one set of expectations across repositories, and maintainers who want a single place to keep policy text current.

**Why Alex built it.** The profile README was added on 2026-07-26 (`8b592a0` "docs: add organization profile README"), the day the Swarm 357 landing site became its own public repository, and the policy set followed on 2026-08-15 (`ac5d3a9` "docs: establish organization community standards"; `c7533c1` "ci: add documentation quality checks"). [REPOSITORY_STANDARDS.md](REPOSITORY_STANDARDS.md) records the intent: separate organization-wide defaults from the controls each code repository must configure itself, as "a practical quality baseline, not a claim that every project has identical risk, release, or maintenance requirements." Maintained by Alex Cinovoj, Founder & CTO of TechTide AI.

**Real-world use case (2025-2026 evidence).** **Verified in this repository.** Giving a small organization's public repositories one contribution path, one private security-reporting path, and a linted, link-checked profile without copying the same files into every repository ([`.github/workflows/documentation.yml`](.github/workflows/documentation.yml), [`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE/), [`CODEOWNERS`](CODEOWNERS)). GitHub's Octoverse 2025 report found that about 63% of public repositories include a README while only 5.5% ship contributor guides and 2% a code of conduct, and called governance documentation an ecosystem-wide gap[^1]. GitHub began surfacing `CONTRIBUTING.md` in a repository tab and sidebar in August 2025, so a default file is now visible wherever it applies[^2]. GitHub's maintainer guidance recommends contributor guidelines and a code of conduct before a community forms rather than after[^3]. The rendering mechanism for `profile/README.md` is documented in GitHub Docs[^4].

[^1]: GitHub, "Octoverse: A new developer joins GitHub every second as AI leads TypeScript to #1", <https://github.blog/news-insights/octoverse/octoverse-a-new-developer-joins-github-every-second-as-ai-leads-typescript-to-1/>, published 2025-10-28.
[^2]: GitHub Changelog, "Contributing guidelines now visible in repository tab and sidebar", <https://github.blog/changelog/2025-08-07-contributing-guidelines-now-visible-in-repository-tab-and-sidebar/>, published 2025-08-07.
[^3]: GitHub Blog, "4 steps toward building an open source community", <https://github.blog/open-source/maintainers/four-steps-toward-building-an-open-source-community/>, published 2025-03-06.
[^4]: GitHub Docs, "Customizing your organization's profile", <https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/customizing-your-organizations-profile>, evergreen documentation page, undated.

## Start Here

| Need | Path |
|---|---|
| Learn about TechTide AI and featured public work | [Organization profile](profile/README.md) |
| Propose a code or documentation change | [Contributing guide](CONTRIBUTING.md) |
| Understand decision-making and policy ownership | [Governance](GOVERNANCE.md) |
| Review expected community behavior | [Code of Conduct](CODE_OF_CONDUCT.md) |
| Report a vulnerability privately | [Security policy](SECURITY.md) |
| Find product help or general contact routes | [Support and contact](SUPPORT.md) |
| Review current standards and project-level rollout guidance | [Repository standards](REPOSITORY_STANDARDS.md) |

## What This Repository Provides

| Capability | Description |
|---|---|
| **Public organization presence** | A concise, curated profile with clear starting points for TechTide AI projects. |
| **Community-health defaults** | Organization-wide contribution, conduct, governance, security, and support guidance. |
| **Structured intake** | Default bug and feature issue forms plus a pull-request template, designed to be reusable without repository-specific labels or projects. |
| **Review accountability** | A focused `CODEOWNERS` rule for policy and profile changes in this repository. |
| **Documentation quality** | Pinned, read-only automation that lints Markdown and checks links on pull requests and updates. |

## Scope and Precedence

The files in this repository establish a consistent baseline. A repository-specific policy takes precedence when it is present, particularly for installation instructions, licensing, support, security reporting, and release practices. Contributors should therefore begin with the documentation in the repository they intend to change.

This repository should remain concise, navigable, and focused on organization-wide guidance. Propose changes to these policies through a pull request with a clear rationale; review follows [GOVERNANCE.md](GOVERNANCE.md).

## References

[1] [GitHub Docs: Creating a default community health file](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)
