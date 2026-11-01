<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="evaluation.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Software Architect](../../../README.md) / [Evaluate the architecture](../SKILL.md)

# Evaluation

Source: ISO/IEC/IEEE 42030:2019. The file type is `evaluation`.

## What it fixes

The three steps in one file: the six-part scenario, the options and the tradeoff with its diagram, and a link to the ADR when a decision was chosen. If a decision was chosen in this turn, also write the ADR as its own `<NNN>-adr-<topic>.md`.

## How to do it

1. Write the scenario section and the tradeoff section. The diagram follows the skill.
2. If no option is chosen, the decision section is the gap `No decision yet. Record it with /arch-evaluation-adr.` and the file stays `proposed`.
3. If an option is chosen, write the ADR file too and link it. Do not paste the ADR body here.

## Prompt

`/arch-evaluation` The concern is #concern. The options are #options.

## Done

- The file uses the template fields. A gap is a line, not a guess.
- An explained section has a few plain sentences and one Mermaid diagram. The diagram is not called UML.
- The state is `accepted` only when no gap remains. Otherwise it is `proposed`.
