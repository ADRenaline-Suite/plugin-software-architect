---
name: evaluate-architecture
description: Evaluates one architecture concern. It writes the quality scenario, the options and the tradeoff, and the decision record, with a diagram of the choice. Use it when someone asks which option to pick, or to record a decision already taken.
---

<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="SKILL.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Software Architect](../../README.md)

# Evaluate the architecture

An evaluation is one decision, in three steps. The scenario says the concern in a way that can be checked. The tradeoff compares the options. The ADR records the option that was chosen. A step without the previous one stays `proposed` and names the command that fills the gap.

Source: ISO/IEC/IEEE 42030:2019. ISO/IEC 25010:2023, the nine product quality names. Quality attribute scenario as used by ATAM (SEI) and the Quality Attribute Workshop: source of the stimulus, stimulus, environment, artifact, response, and response measure. ADR, Michael Nygard: status, context, decision, and consequences.

## Before writing

1. Read only the reference for this situation: [quality-scenario](references/quality-scenario.md), [tradeoff](references/tradeoff.md), [adr](references/adr.md), or [evaluation](references/evaluation.md).
2. A command names one reference. Write that situation only.
3. A request that asks to evaluate an architecture and names no command does the same as `/arch-evaluation`.
4. Name the quality characteristic with a current ISO/IEC 25010:2023 name: functional suitability, performance efficiency, compatibility, interaction capability, reliability, security, maintainability, flexibility, or safety. Do not use usability or portability.
5. An evaluation without at least two options is not complete. It stays `proposed`.
6. Do not draw a UML diagram here. If a view is needed to judge the options, ask `plugin-uml-diagrams` and link it. Do not write the use case, the test scenario, or the threat model.

## Diagrams

The tradeoff and the full evaluation each include one Mermaid diagram. The boxes are the options a source named. One arrow marks the option that was chosen, and only when a decision was made. Under the figure, one sentence says what it shows. The diagram is an explanation. Do not call it UML.

## Language

The instructions stay in English. Write the artifact in the language of the request. If the request names a language, use that one. Otherwise use the language the request is written in. Keep names the person already used. Translate the headings of the reference template and keep the same fields. The type in the file name stays the English piece id. `STATUS.md` columns stay `N`, `archivo`, `estado`, `sustituye`, `notas`. The reply uses that same language.

## When a prerequisite is missing

A single-step command with no concern, or an ADR with no decision, writes no file.

When the gap asks the person to supply a fact, write the same four parts in that section of the report and in the chat. Use the language of the request. Keep the command names.

1. What is missing. Two or three sentences. Name the missing fact, say what this section does with it, and say what this section does not write. Say the file stays `proposed` until that fact is cited.
2. How to fill it. The steps, in order. Say where the fact comes from: text the person pastes, or an accepted file from the plugin that owns it. When a file of this topic already exists, name it and say to amend it.
3. Template. The prompt from the reference, filled with what the person already said. Where a value is still missing, leave the gap (`#…`).
4. Example. One filled message, after the template. It keeps the names the person already used and fills only the gaps with sample values. Its first line says it is a sample to replace, that it is not a citation, and that those sample values are not facts in the document.

A gap that asks for nothing to be typed stays one line.

`/arch-evaluation` still writes the evaluation file. A missing step is that four-part gap and the file stays `proposed`. The reply repeats those four parts.

## Delivery

The folder is `adrenaline/software-architect/` at the project root. If `.cursor/adrenaline.json` has `outputDirs["plugin-software-architect"]` set to a relative path, without `..` and not absolute, use that path. If the file, the key, or a valid path is missing, use `adrenaline/software-architect/` and, in the last case, say so. If `adrenaline/software-architect/` does not exist yet and `software-architect/` at the project root already has this plugin's `ORIGIN.json` or `STATUS.md`, keep writing there and say so. Create the folder if it does not exist. Do not write outside it.

The file is `<NNN>-<type>-<topic>.md`. `<NNN>` is the next free integer, three digits, and it is not reused. `<type>` is the English piece id from the reference.

Keep `<folder>/STATUS.md` with columns `N`, `archivo`, `estado`, `sustituye`, and `notas`.

Keep `<folder>/ORIGIN.json` beside `STATUS.md`. It is not an `<NNN>` file and it has no row in `STATUS.md`. Write it when the folder is created. On a later delivery, write it again only when it is missing or a field differs. The fields are `suite` `ADRenaline-Suite`, `plugin` `plugin-software-architect`, `repository` `https://github.com/ADRenaline-Suite/plugin-software-architect`, and `convention` `adr-001`.

`notas` lists `sources: <relative path>; read: <UTC timestamp>` using `yyyy-MM-ddTHH:mm:ssZ`. Do not put `|` inside `notas`.

If the topic already has a file:

- The user asks to amend that same file: edit it, keep the `<NNN>`, and keep `accepted` if it already was.
- A replacement: next `<NNN>`, the previous row becomes `superseded`.
- New topic: next `<NNN>`.

`accepted` when the reference's required fields are filled and the tradeoff has at least two options. `proposed` when a gap remains. An accepted ADR is what `/arch-arc42` cites. When you close, say the folder, the file, the `N`, and the state.

## Done

Before you close, evaluate this list and the `## Done` list in the reference for this situation. A command fixes the situation: use the reference that command names. Every item is true, or you fix the delivery in this turn. Do not leave a file that fails an item. Do not mark it `accepted` while an item fails. A template the reference names is applied and recorded under Assumed; the delivery uses the state that reference names. A prerequisite that still stops the delivery is not a failed list: follow "When a prerequisite is missing" and write no files for that piece.

- The situation of this turn is the only one written, unless the request asked for two. Each delivery has its own `<NNN>`.
- Files are only in the output folder, named as Delivery says. `<NNN>` is not reused. `STATUS.md` matches the files and the state this situation allows. `ORIGIN.json` is in that folder, its four fields match this plugin, and it has no row in `STATUS.md`. A gap the reference leaves as `proposed` stays `proposed`.
- The artifact language matches the request. `STATUS.md` columns stay `N`, `archivo`, `estado`, `sustituye`, `notas`.
- The quality name is one of the nine ISO/IEC 25010:2023 names. The scenario has six parts. The tradeoff names at least two options, or the file stays `proposed`.
- The diagram, when this situation has one, shows only options that were named. It is not called UML.
- No part was invented. A gap that asks the person to supply a fact is the four-part gap in the report and in the reply: what is missing, how to fill it, the template, and one example. The example is marked as a sample and is not a fact. A gap that asks for nothing to be typed stays one line.
- The reply names the folder, the files, the `N`, and the state. When a prerequisite stops the piece, the reply is that same four-part gap and names no new file.

## Example

Input: "the catalog must answer 2,000 reads per second at peak, under 200 ms, without losing orders. Options: a read replica or a cache." The request is in English and names no command.

Output: `001-evaluation-catalog-reads.md`, state `proposed`, because no option is chosen yet. The scenario has six parts. The Mermaid shows the two options and no chosen arrow. The reply names `adrenaline/software-architect/`, the file, `001`, and `proposed`, and says `/arch-evaluation-adr` records the choice.
