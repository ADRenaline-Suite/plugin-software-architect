<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="adr.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Software Architect](../../../README.md) / [Evaluate the architecture](../SKILL.md)

# Architecture decision

Source: Michael Nygard, status, context, decision, and consequences. The file type is `adr`.

## What it fixes

A decision already taken. It does not reopen the scenario.

## How to do it

1. Status is `accepted` when the decision text is the one the person stated. `proposed` when the decision is still a candidate.
2. Context cites the quality scenario and the tradeoff when those files exist. It does not copy them.
3. Consequences name what gets easier and what gets harder, only from what was said or read.
4. No use case, no threat model, no code.

## Template

```markdown
# <NNN> — <title>

- Status: proposed | accepted

## Context

## Decision

## Consequences
```

## Prompt

`/arch-evaluation-adr` The decision for #concern is #decision.

## Done

- The file uses the template fields. A gap is a line, not a guess.
- An explained section has a few plain sentences and one Mermaid diagram. The diagram is not called UML.
- The state is `accepted` only when no gap remains. Otherwise it is `proposed`.
