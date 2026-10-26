# Technical roadmap

Dates and delivery commitments have not been set. Each milestone has an acceptance gate; completing a document does not establish that a runtime feature works.

## Evidence states

- **Planned:** requirements or design exist, but no implementation evidence exists.
- **Implemented:** code exists and can be inspected; the stated verification gate may still be unmet.
- **Verified:** the named gate passed in a recorded environment with linked evidence. Verification is limited to that gate and environment.

## Current baseline

Available artifacts: project documentation, proposed architecture, draft identity, and policies. All runtime milestones below are **planned**, not implemented or verified.

| Milestone | Deliverable | Acceptance gate | Status |
| --- | --- | --- | --- |
| 0. Scope and rights | Prototype scope, license selection, dependency intake rules | Owner approves scope and licensing before publication or contributions | Planned |
| 1. Record contract | Versioned run/event/check schemas and fixtures | Validators reject invalid records; passing, failing, and missing checks are distinguishable | Planned |
| 2. Bounded executor | One local fixture adapter, timeout, cancellation, workspace constraints | Tests demonstrate success, failure, timeout, cancellation, and denied writes | Planned |
| 3. Evidence report | Artifact index and readable report | Every success claim links to a completed check; altered/missing artifacts are flagged | Planned |
| 4. Approval and privacy | Action-specific approvals and redaction | Denied/expired approvals block actions; seeded secrets are excluded from persisted reports | Planned |
| 5. Demonstrable release | Runnable deterministic demo, failure example, versioned instructions | Fresh environment reproduces documented outcomes; reviewer inspects complete evidence | Planned |
| 6. Integration evaluation | One selected model or tool adapter | Compatibility and threat assumptions documented; integration tests recorded | Planned |

## First demo proposal

Use a small deterministic fixture that writes a file inside an isolated test workspace and checks its content. Include a deliberate failing check and an attempted forbidden path. Show the task, the permitted action, the produced artifact, and the actual check outcomes. This is a demo plan, not an available demo.

## Release evidence

For each completed milestone, retain the commit identifier, environment, exact command, exit status, relevant artifacts, and known limitations. Replace claims in the README only when those references exist. Benchmarks need a stated workload, baseline, sample size, and reproducible procedure before any comparative claim.
