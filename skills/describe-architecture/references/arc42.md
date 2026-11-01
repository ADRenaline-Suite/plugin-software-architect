<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="arc42.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Software Architect](../../../README.md) / [Describe the architecture](../SKILL.md)

# arc42 manual

Source: arc42 template 9.1, English, October 2026. ISO/IEC/IEEE 42010:2022. The file type is `arc42`.

## What it fixes

The architecture manual in twelve sections. A reader gets a short paragraph per section. Sections that are views cite the 4+1 and show the same kind of explanatory diagram only when that view is not already in an accepted 4+1 file. If it is, the section links that file and does not draw a second diagram.

## How to do it

1. Sections, in order: goals and constraints and strategy; context; building blocks; runtime; deployment; concepts; decisions; quality; risks; glossary. Building blocks cites `/arch-4plus1` logical and development. Runtime cites process. Deployment cites physical.
2. Decisions lists accepted ADRs from this plugin. Quality lists accepted quality scenarios. If a citation is missing, that section is the four-part gap from this skill and names the command: `/arch-evaluation-adr` or `/arch-evaluation-scenario`. The example is not a citation. The reply repeats those four parts.
3. Context has its own diagram: the system in the center, external names around it, only names a source gave.
4. The file stays `proposed` while the entity, the stakeholders, the concerns, or the context facts are missing.
5. Do not copy a 4+1 section. Link it.

## Prompt

`/arch-arc42` Read the folder #folder. Write the arc42 manual of #system in #language.

## Done

- The file uses the template fields. A gap that asks the person to supply a fact is the four-part gap, with an example besides the template. The example is not a fact. Any other gap is a line, not a guess.
- An explained section has a few plain sentences and one Mermaid diagram. The diagram is not called UML.
- The state is `accepted` only when no gap remains. Otherwise it is `proposed`.

- The twelve sections are present. A missing citation the person must supply is the four-part gap, not a rewritten view. The example is not a citation.
