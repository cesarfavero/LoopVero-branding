# LoopVero

**Don’t just show the answer. Show the work.**

LoopVero is a planned execution harness for AI-assisted work: a way to connect a requested task to the actions taken, the artifacts produced, and the checks actually run.

**Current stage: design and documentation.** This package contains the project direction, a proposed architecture, contribution policies, and an original visual identity. It does not contain an executable harness, working integrations, benchmark results, or a runnable demo. Licensing is pending; this is not an open-source release.

## The idea

An answer alone rarely tells you whether a change was made, a test passed, or a result can be inspected. LoopVero aims to make that distinction explicit. A future run should leave a reviewable record of observable work, including failures, skipped checks, and actions waiting for approval.

“Show the work” means tool actions, inputs safe to disclose, outputs, artifacts, and verification results. It does not mean exposing a model’s private reasoning or collecting secrets.

## Planned workflow

1. **Define the task.** Record the goal, permitted actions, and success criteria.
2. **Execute within scope.** Run allowed tools and stop at approval boundaries.
3. **Capture evidence.** Link observable events to outputs and artifacts.
4. **Check the result.** Report which checks passed, failed, or did not run.
5. **Hand off the record.** Produce a concise summary with inspectable evidence.

These are design goals, not available features. A record is evidence of recorded events, not proof that every action was captured or that a result is correct.

## What exists today

| Area | Status | Evidence |
| --- | --- | --- |
| Product direction | Written | [Positioning](docs/POSITIONING.md) |
| Technical design | Proposed | [Architecture](docs/ARCHITECTURE.md) |
| Delivery milestones | Planned | [Roadmap](docs/ROADMAP.md) |
| Brand assets | Draft SVG and tokens | [Brand guide](brand/README.md) |
| Execution engine, integrations, demo | Not implemented | No runtime included |
| Security controls | Requirements only | [Security](SECURITY.md) |

There are no installation or quickstart commands yet. The first demo will be documented only after it can be run and its evidence inspected.

## Contribute

Start with [CONTRIBUTING.md](CONTRIBUTING.md), [PROVENANCE.md](PROVENANCE.md), and [LICENSING.md](LICENSING.md). Architecture feedback should identify a concrete user need, a proposed change, and a testable acceptance criterion. A contribution or distribution license has not yet been selected.

## Em português

**Não mostre só a resposta. Mostre o trabalho.**

LoopVero é o planejamento de um harness para execução verificável de tarefas assistidas por IA. A proposta é conectar o pedido às ações observáveis, aos arquivos produzidos e às verificações realmente executadas.

Hoje existem documentação, arquitetura proposta e identidade visual. Ainda não há motor de execução, integrações comprovadas ou demo funcional. A licença será definida antes de uma distribuição pública. A trilha de evidências deverá mostrar também falhas e verificações não executadas, sem expor segredos ou raciocínio privado do modelo.
