# Proposed execution architecture

This is a design proposal. No component described here is implemented in this package.

## Minimal run model

A task specification would contain a goal, allowed workspace, allowed tool operations, approval requirements, and explicit success criteria. A coordinator would execute a bounded sequence of operations through adapters and write an event record. A verifier would evaluate declared checks; a reporter would link the resulting evidence and artifacts.

```text
Task specification -> Policy gate -> Tool adapter -> Event record
                           ^               |              |
                           |          Artifact index      |
                     Human approval        |              v
                                           +------> Verifier -> Report
```

The diagram does not establish an isolation boundary. A policy gate must be enforced outside untrusted task or tool content; adapters must not obtain unrestricted authority by merely being registered.

## Proposed records

- **Run:** identifier, schema version, task scope, timestamps, environment summary, final state.
- **Event:** sequence, operation name, sanitized parameters, start/end time, outcome, linked artifacts, approval reference where required.
- **Artifact:** relative path, media type, byte count, digest, generating event, disclosure classification.
- **Check:** declared criterion, checker version, invocation, exit status, sanitized output reference, result of passed/failed/not-run/error.
- **Approval:** action scope, requested permission, decision, time, and expiration or single-use boundary.

Digests can help detect accidental changes to an artifact relative to a recorded value. They do not establish who produced it, completeness of the log, or authenticity of a compromised runtime.

## Run states

Proposed lifecycle: queued, running, awaiting approval, succeeded, failed, cancelled. “Succeeded” requires all mandatory checks to pass and all required artifacts to exist. A missing check must not count as a pass. Cancellation and failure must preserve the partial record when safe.

## First prototype boundary

Start with deterministic local fixtures and one narrow, non-networked adapter. Exclude credential handling, external messages, deployment, billing, and production mutation. Choose implementation language and storage after reviewing prototype requirements; no stack choice is final here.

## Safety requirements to test

Reject path traversal and out-of-scope writes. Treat tool output as untrusted data. Bound runtime and output volume. Redact known secret patterns before persistence and test the limits of redaction. Make approval action-specific. Record unavailable evidence explicitly. Keep raw sensitive traces out of public reports.

## Replay and reproducibility

A future inspection command should read a saved record without re-executing actions. Re-running a task is a separate operation with separate authorization. Identical model output or environment behavior is not promised. Any future reproducibility claim must specify the fixture, environment, and variability observed.
