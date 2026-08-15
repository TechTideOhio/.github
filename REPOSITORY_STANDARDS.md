# Repository Standards

## Purpose

This document distinguishes the **organization-wide defaults** maintained in this repository from the controls that must be configured in each individual code repository. It is a practical quality baseline, not a claim that every project has identical risk, release, or maintenance requirements.

## Organization-Wide Baseline

| Standard | Status | Implementation |
|---|---|---|
| Clear organization profile | Established | `profile/README.md` presents the mission, selected projects, and direct next steps. |
| Community-health defaults | Established | Contribution, conduct, governance, security, and support policies are maintained at the repository root. GitHub can apply these to repositories that do not define their own file of the same type. [1] |
| Structured contributor intake | Established | Default bug and feature forms plus a pull-request template are in `.github/`. |
| Review ownership | Established | `CODEOWNERS` requests maintainer review for changes to this repository. |
| Documentation quality checks | Established | A read-only workflow lints Markdown and checks links on pull requests and updates. |
| Dynamic profile widgets | Intentionally deferred | The profile uses curated, organization-controlled content rather than unowned activity counters or third-party badges. |

## Per-Repository Rollout

Each public code repository should be reviewed against the following standards. The responsible maintainer should select the controls that fit the repository’s language, package ecosystem, deployment model, and security exposure.

| Area | Recommended control | Why it matters |
|---|---|---|
| **Discoverability** | Add a useful repository description, topics, a current README, and a project license. | Helps users assess purpose, compatibility, and reuse conditions quickly. |
| **Ownership** | Add repository-specific `CODEOWNERS` and protect the default branch with required reviews and required checks. | Makes accountable review and merge controls explicit. |
| **Security reporting** | Add a repository-specific `SECURITY.md` when a project has unique scope or contact requirements; enable private vulnerability reporting where available. | Gives researchers a safe, actionable reporting path. |
| **Dependency maintenance** | Configure Dependabot for supported manifests; group low-risk updates and set a review cadence. [2] | Reduces the time dependencies remain outdated without creating unmanageable pull-request volume. |
| **Workflow hardening** | Pin third-party actions to immutable commit SHAs, use explicit least-privilege permissions, and disable persistent checkout credentials unless needed. [3] | Reduces supply-chain exposure in CI. |
| **Supply-chain posture** | Run OpenSSF Scorecard for public code repositories and act on relevant findings. [4] | Provides repeatable signals for checks such as branch protection, pinned actions, token permissions, and vulnerability disclosure. |
| **Quality verification** | Run the project’s tests, formatters, type checks, and security checks on pull requests. | Gives contributors and maintainers a fast, reproducible quality signal. |
| **Release integrity** | Define versioning, changelog, artifact provenance, and rollback expectations in the repository. | Makes releases easier to evaluate, consume, and recover. |

## Review Sequence

A maintainer should first confirm that the repository’s README, license, support, and security path are accurate. Next, establish branch protection and a focused CI workflow. Then add dependency automation and supply-chain checks appropriate to the project. This order ensures that automation reinforces accountable ownership rather than creating unattended signals.

## Non-Goals

This organization-profile repository does not centralize secrets, deploy production services, enforce hidden organization settings, or replace repository-specific security design. A workflow or policy file here cannot automatically impose per-repository branch protection, Dependabot configuration, release practice, or private vulnerability-reporting settings.

## References

[1] [GitHub Docs: Creating a default community health file](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)

[2] [GitHub Docs: Dependabot options reference](https://docs.github.com/en/code-security/reference/supply-chain-security/dependabot-options-reference)

[3] [GitHub Docs: Use `GITHUB_TOKEN` for authentication in workflows](https://docs.github.com/en/actions/tutorials/authenticate-with-github_token)

[4] [OpenSSF Scorecard: Check documentation](https://github.com/ossf/scorecard/blob/main/docs/checks.md)
