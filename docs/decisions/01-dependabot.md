# Dependabot

> [!NOTE]
> - **Date**: 2024-03-26
> - **Author**: Jimmy Briggs <jimmy.briggs@noclocks.dev>
> - **Status**: Accepted

## Context and Problem Statement

**Dependabot** is a GitHub App that automates dependency updates for your projects. It creates pull requests to update dependencies in your project when new versions are released. Dependabot can be configured to update dependencies on a schedule or when new versions are released. The problem is that Dependabot can create a large number of pull requests, which can be overwhelming for maintainers.

The problem is that Dependabot can create a large number of pull requests, which can be overwhelming for maintainers. This decision is to determine how to manage Dependabot pull requests to reduce the number of pull requests and make it easier for maintainers to review and merge them.

At No Clocks, since we use and rely on open source software, we need to ensure that our projects are up-to-date with the latest security patches and bug fixes. Dependabot is a valuable tool for keeping our projects up-to-date, but we need to find a way to manage the pull requests it creates effectively.

## Decision Drivers

- Keep projects up-to-date with the latest security patches and bug fixes
- Reduce the number of pull requests created by Dependabot
- Make it easier for maintainers to review and merge Dependabot pull requests

## Considered Options

1. **Merge Dependabot pull requests automatically**: Automatically merge Dependabot pull requests when they are created
2. **Merge Dependabot pull requests on a schedule**: Merge Dependabot pull requests on a schedule, such as once a week
3. **Manually review and merge Dependabot pull requests**: Manually review and merge Dependabot pull requests as needed

## Decision

We have decided to **manually review and merge Dependabot pull requests**. This option allows us to review each pull request and ensure that the updates are compatible with our projects. It also gives us the opportunity to test the updates before merging them into our projects.

## Consequences

- **Pros**:
  - Allows us to review each update and ensure compatibility with our projects
  - Gives us the opportunity to test updates before merging them into our projects

- **Cons**:
  - Requires manual effort to review and merge Dependabot pull requests
  - May delay the integration of updates into our projects
  - Increases the workload for maintainers

***

## Example dependabot.yml

The following is an example [`.github/dependabot.yml`](.github/dependabot.yml) configuration file that specifies the
update schedule for various *package ecosystems*, in this case `npm`, `docker`, and `github-actions`:

```yaml
version: 2
updates:
  - package-ecosystem: "npm"
    directory: "/"
    schedule:
      interval: "weekly"
    ignore:
      - dependency-name: "*"
        update-types: ["version-update:semver-major"]
  - package-ecosystem: "docker"
    directory: "/"
    schedule:
      interval: "weekly"
  - package-ecosystem: "github-actions"
    directory: "/"
    schedule:
      interval: "weekly"
```

## References

- [Dependabot Documentation](https://docs.github.com/en/code-security/supply-chain-security/keeping-your-dependencies-updated-automatically/about-dependabot-version-updates)
