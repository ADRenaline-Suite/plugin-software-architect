<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="tradeoff.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Software Architect](../../../README.md) / [Evaluate the architecture](../SKILL.md)

# Options and tradeoff

Source: ISO/IEC/IEEE 42030:2019. The file type is `tradeoff`.

## What it fixes

The options in play and what each one costs. At least two options. One Mermaid diagram: one box per option. No chosen arrow unless a decision was already named.

## How to do it

1. One short paragraph per option, in plain language: what it changes, and the cost the person or a source named.
2. Fewer than two options: write the file as `proposed` and name the gap.
3. Do not pick the winner here. That is `/arch-evaluation-adr`.

## Prompt

`/arch-evaluation-tradeoff` The options for #concern are #options.

## Done

- The file uses the template fields. A gap is a line, not a guess.
- An explained section has a few plain sentences and one Mermaid diagram. The diagram is not called UML.
- The state is `accepted` only when no gap remains. Otherwise it is `proposed`.
