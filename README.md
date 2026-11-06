# Documentation Framework

Reusable documentation framework for software projects. It provides a consistent
way to plan, record, and track software work.

Add this repository to another project with `git subtree` to keep the shared
documentation structure and practices in one place and sync them into each
project that uses them.

## Goals

- Provide a consistent structure for technical documentation.
- Record architectural decisions and their consequences.
- Gather feedback on proposed changes before implementation.
- Turn requirements and decisions into actionable specifications.
- Document operational procedures that people and AI agents can execute safely.
- Maintain traceability between related documents and implementation work.
- Support planning, progress tracking, and review.

## Structure

- [`adrs/`](adrs/): Architecture Decision Records that explain important technical choices.
- [`rfcs/`](rfcs/): Requests for Comments that invite discussion on larger proposals.
- [`specs/`](specs/): Technical and functional specifications that guide implementation.
- [`runbooks/`](runbooks/): Step-by-step procedures for recurring operations, maintenance, and incident response.

Each directory includes a `README.md` and a starter template. Keep document
IDs, status, and links to related work up to date.

## Using as a subtree

In the consuming project, add this repository as a subtree under a dedicated
directory:

```bash
git remote add doc2gh <REPOSITORY_URL>
git fetch doc2gh
git subtree add --prefix=docs/doc2gh doc2gh main --squash
```

To pull in future updates:

```bash
git fetch doc2gh
git subtree pull --prefix=docs/doc2gh doc2gh main --squash
```

Adjust the directory path and branch name to fit the consuming project.

## Recommended Workflow

1. Write an RFC when a change needs broad discussion.
2. Once the proposal is approved, record lasting architectural choices as ADRs.
3. Turn the work into Specs with clear, verifiable acceptance criteria.
4. When a Spec introduces or changes an operational procedure, write or update
   the matching Runbook and link the two documents.
5. Link each document to its related work items and review records.
6. Keep statuses current as work progresses.

Each section's README and template define its statuses, naming rules, and
traceability fields. Until supporting tools are available, follow these
templates through the project's review workflow.

## Project Status

This repository provides the documentation framework. Tools for creating,
validating, and syncing documents may be added over time; they are not required
to start using it.
