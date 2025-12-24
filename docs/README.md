# OctoAcme Project Management Docs

## Overview
This README is the central entry point to OctoAcme's project management guidance. It summarizes our core processes, key roles, communication cadence, and quality practices, and links to the detailed process documents in this folder. Use this as the single source of truth for project artifacts, status, and onboarding.

OctoAcme runs projects as a lightweight, iterative lifecycle that moves deliberately from initiation to planning, execution, release, and retrospective. Projects begin with a focused one‑pager that captures the problem, measurable success metrics, stakeholders, and a high‑level timeline; that artifact is the gate for deciding whether to proceed to planning. Planning breaks approved initiatives into shippable increments, identifies dependencies and risks (captured in a Risk Register), and produces a prioritized backlog and release milestone map. The overall approach emphasizes customer value, clear ownership, and data‑informed decision making so teams deliver small, testable increments rather than large, risky monoliths.

Execution centers on an operational workflow supported by a visible project board and disciplined pull request practices. Work is managed on a board with columns such as Backlog, Ready, In Progress, In Review, QA, and Done; sprint and iteration planning timeboxes intake and ensure items meet the Definition of Done and have acceptance criteria. The PR workflow encourages small changes, linked issues and acceptance criteria in descriptions, automated CI checks (tests, linting, security scans) before review, and at least one approval policy. Regular demos and delivery syncs keep the team aligned on progress and surfaced risks.

Roles are clearly defined to reduce ambiguity: Product Managers own outcomes and prioritization, Project Managers coordinate delivery, schedules, risks, and communications, Developers implement and test features, QA focuses on validation and acceptance, and stakeholders provide inputs and approvals. These personas drive different artifacts—PMs and PdMs maintain the one‑pager, roadmap, and success metrics; PMs maintain the risk register and status reports; engineers own technical quality, tests, and CI pipelines—so responsibilities are explicit and trackable.

Communication and quality assurance are integral. Team rhythm includes daily standups for blockers and progress, weekly PM+PdM syncs, weekly or milestone status reports to stakeholders, and end‑of‑sprint demos; templates (e.g., weekly status) standardize updates. Quality practices require unit and integration tests, end‑to‑end smoke tests for critical flows, CI security scanning, and manual QA as needed; release readiness demands passing CI, release notes, rollback plans, and staged smoke tests in staging before production deploys. After releases and incidents, OctoAcme runs retrospectives to capture action items, track improvements, and feed lessons back into the backlog so the process continuously improves.

## Docs Directory
- [Project Management Overview](octoacme-project-management-overview.md)
- [Project Initiation Guide](octoacme-project-initiation.md)
- [Project Planning](octoacme-project-planning.md)
- [Execution & Tracking](octoacme-execution-and-tracking.md)
- [Risk Management & Communication](octoacme-risks-and-communication.md)
- [Release & Deployment Guide](octoacme-release-and-deployment.md)
- [Retrospective & Continuous Improvement](octoacme-retrospective-and-continuous-improvement.md)
- [Roles & Personas](octoacme-roles-and-personas.md)

## How to use
- Keep this README updated when process docs are added or renamed.
- Link this README from project READMEs or the repo root to improve discoverability.
- For Copilot Spaces context, add process-specific docs into `.copilot/` if you want them explicitly included for exercises.
