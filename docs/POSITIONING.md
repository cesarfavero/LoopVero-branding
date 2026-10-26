# LoopVero positioning

## Audience and problem

The initial audience is developers reviewing AI-assisted changes and small teams that need to understand what an automated task actually did. The working hypothesis is that a compact, inspectable execution record can reduce ambiguity between a proposed action and a completed, checked result. This hypothesis has not yet been validated with users.

## Product statement

LoopVero is a planned harness for observable execution and evidence-based handoff of AI-assisted tasks. Its proposed unit of value is a run record linking the task, permitted actions, generated artifacts, and verification outcomes.

## Message hierarchy

- **Name:** LoopVero
- **Tagline:** Don’t just show the answer. Show the work.
- **Portuguese tagline:** Não mostre só a resposta. Mostre o trabalho.
- **Short description:** A planned execution harness that connects AI-assisted work to inspectable evidence.
- **Current-stage description:** Product design and documentation for an evidence-oriented execution harness. Runtime and demo are not implemented yet.

## Principles

Use observable facts rather than confidence language. Keep “planned,” “implemented,” and “verified” separate. Make failures visible. Ask before crossing permission boundaries. Minimize the sensitive data retained in records.

## Boundaries

LoopVero is not presented as a model, a general guarantee of correctness, an autonomous production operator, a compliance certification, or a substitute for human review. No performance, security, compatibility, or adoption claim is established at this stage.

## Validation questions

Can a reviewer distinguish an attempted action from a completed one? Can they find the evidence behind a passing check? Does the record remain useful when a run fails? Can sensitive details be omitted without making the result misleading? These questions should guide the first prototype and interviews.
