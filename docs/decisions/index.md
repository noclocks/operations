# Architectural Decision Records (ADR) Index

> [!NOTE]
> At No Clocks, we use [Architectural Decision Records (ADRs)](https://adr.github.io/) to document the architectural
> decisions made on our projects and products.
>
> This index provides an overview of all the ADRs in the repository.

## Overview

In order to ensure that decisions are reviewed and implemented in a timely manner, we use ADRs to document the context, problem statement, decision, and consequences of each decision. This allows us to track the evolution of our architecture and understand the rationale behind each decision.

The workflow involved is detailed as follows:

1. **Create a new ADR**: When a a concern is raised, or a decision is made, a new ADR is created to document the context, problem statement, decision, and consequences.
1. **Create a pull request**: The ADR is created in a new branch and a pull request is opened to review the decision.
1. **Review and merge**: The decision is reviewed by the team and merged into the main branch once approved.
1. **Update the index**: The index is updated to include the new ADR.

## Index

- [00-template](00-template.md): A template for creating new ADRs.
- [01-dependabot](01-dependabot.md): Decision to manually review and merge Dependabot pull requests.
- [02-branching-strategy](02-branching-strategy.md): Decision to utilize Git Branching Best Practices.
