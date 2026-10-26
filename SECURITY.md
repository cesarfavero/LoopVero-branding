# Security

## Current status

LoopVero has no released runtime and no supported software versions. This package contains design documentation and brand assets. Proposed controls are not implemented or independently assessed.

## Reporting

A private security reporting channel has not yet been designated. Do not post credentials, personal information, or exploitable details publicly. Ask the maintainer to establish a private channel before sharing a sensitive report. No response-time commitment or bounty program is currently offered.

Before any executable release, this policy must identify supported versions, a private reporting destination, a triage owner, and a disclosure process.

## Threats the prototype must address

Untrusted task instructions and tool output; unauthorized filesystem or network access; leaked secrets in logs; corrupted or incomplete evidence; forged approval state; unbounded execution; unsafe re-execution of recorded operations; dependency compromise.

## Planned release gates

Use least-privilege tool adapters and explicit scope enforcement. Treat external content as data, not authority. Test timeouts, cancellation, path handling, and action-specific approvals. Minimize retention and redact sensitive fields before persistence. Review dependency provenance. Document the environment and residual risks.

A run record is not an independent security audit. Passing tests do not establish that the system is safe for production or for untrusted code.
