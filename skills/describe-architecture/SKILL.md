---
name: describe-architecture
description: Writes the 4+1 document and the arc42 manual so a reader can follow them. Each section is a few plain sentences and one diagram. Use it when someone asks what the system is, how the code is organized, how the parts call each other, where they run, or for the architecture manual.
---

<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="SKILL.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Software Architect](../../README.md)

# Describe the architecture

Write a document a reader can follow without knowing the method. The 4+1 is one file with five sections. The arc42 manual is another file. It cites the 4+1. It does not copy it.

Source: ISO/IEC/IEEE 42010:2022 (entity of interest, stakeholders, concerns, viewpoints, views). arc42 template 9.1, English, October 2026. Philippe Kruchten, "Architectural Blueprints — The 4+1 View Model of Software Architecture", IEEE Software, 1995. C4, Simon Brown (https://c4model.com/), for the context section only.

## Before writing

1. Read only the reference for this situation: [4plus1](references/4plus1.md), [logical](references/logical.md), [development](references/development.md), [process](references/process.md), [physical](references/physical.md), [scenarios](references/scenarios.md), [arc42](references/arc42.md), [context](references/context.md), [strategy](references/strategy.md), [concepts](references/concepts.md), [risks](references/risks.md), or [glossary](references/glossary.md).
2. A command names one reference. Write that situation only.
3. A request that asks for the 4+1 and names no command does the same as `/arch-4plus1`. A request that asks for the arc42 manual and names no command does the same as `/arch-arc42`.
4. Read the folder or the files the person named. Use the names found there. A part, a call, a port, or a node that no source named is not written. The gap is one line in that section.
5. Do not write the use-case text, the OpenAPI contract, the threat model, the data model, or the domain model. Ask that plugin. Cite what it already wrote.
6. Do not draw a UML diagram in this file. Ask `plugin-uml-diagrams` when the reference says so, and link the file it writes.

## Diagrams

Every section that the reference marks as explained has one diagram in the same file.

1. Two or three short sentences first. They say what the reader is looking at.
2. Then one Mermaid diagram. Boxes are parts a source named. Arrows are relations a source named. Labels use the language of the artifact.
3. Under the diagram, one sentence says what the figure shows.
4. The diagram is an explanation. Do not call it UML, C4, or a PlantUML file.
5. When the reference asks for a UML drawing, ask `plugin-uml-diagrams` for that type and version, then link the `.svg` it saved. The Mermaid stays in this document so it can be read alone.

## Language

The instructions stay in English. Write the artifact in the language of the request. If the request names a language, use that one. Otherwise use the language the request is written in. Keep names the person already used. Translate the headings of the reference template and keep the same fields. The type in the file name stays the English piece id. `STATUS.md` columns stay `N`, `archivo`, `estado`, `sustituye`, `notas`. The reply uses that same language. The prompts in the reference are the English wording: show them in the language of the request and keep the command names.

## When a prerequisite is missing

`/arch-4plus1` still writes the file. A section with no facts lists the gap and the file stays `proposed`. The scenarios section stays a gap until a use case is cited. The other sections are still written.

`/arch-arc42` still writes the file. A section that can only cite a missing piece lists that piece and the command that writes it. The file stays `proposed` until the entity of interest, the stakeholders, the concerns, and the context section have facts. It does not invent them.

A single-section command with no facts writes no file.

When the gap asks the person to supply a fact, write the same four parts in that section of the report and in the chat. Use the language of the request. Keep the command names.

1. What is missing. Two or three sentences. Name the missing fact, say what this section does with it, and say what this section does not write. Say the file stays `proposed` until that fact is cited.
2. How to fill it. The steps, in order. Say where the fact comes from: text the person pastes, or an accepted file from the plugin that owns it. When a file of this topic already exists, name it and say to amend it.
3. Template. The prompt from the reference, filled with what the person already said. Where a value is still missing, leave the gap (`#…`).
4. Example. One filled message, after the template. It keeps the names the person already used and fills only the gaps with sample values. Its first line says it is a sample to replace, that it is not a citation, and that those sample values are not facts in the document.

A gap that asks for nothing to be typed stays one line.

## Delivery

The folder is `adrenaline/software-architect/` at the project root. If `.cursor/adrenaline.json` has `outputDirs["plugin-software-architect"]` set to a relative path, without `..` and not absolute, use that path. If the file, the key, or a valid path is missing, use `adrenaline/software-architect/` and, in the last case, say so. If `adrenaline/software-architect/` does not exist yet and `software-architect/` at the project root already has this plugin's `ORIGIN.json` or `STATUS.md`, keep writing there and say so. Create the folder if it does not exist. Do not write outside it.

The file is `<NNN>-<type>-<topic>.md`. `<NNN>` is the next free integer, three digits, and it is not reused. `<type>` is the English piece id from the reference.

Keep `<folder>/STATUS.md` with columns `N`, `archivo`, `estado`, `sustituye`, and `notas`.

Keep `<folder>/ORIGIN.json` beside `STATUS.md`. It is not an `<NNN>` file and it has no row in `STATUS.md`. Write it when the folder is created. On a later delivery, write it again only when it is missing or a field differs. The fields are `suite` `ADRenaline-Suite`, `plugin` `plugin-software-architect`, `repository` `https://github.com/ADRenaline-Suite/plugin-software-architect`, and `convention` `adr-001`. The marker names the folder. It does not say that each file inside is unchanged.

`notas` lists `sources: <relative path>; read: <UTC timestamp>` using `yyyy-MM-ddTHH:mm:ssZ`. Do not put `|` inside `notas`. Paths are relative to the project root, with no `..`.

If the topic already has a file:

- The user asks to amend that same file: edit it, keep the `<NNN>`, and keep `accepted` if it already was.
- A replacement or a new decision on the same topic: next `<NNN>`, the previous row becomes `superseded` (`sustituye` points at the new `N`).
- New topic: next `<NNN>`.

`accepted` when every section the reference requires has facts and a diagram, and no gap remains. `proposed` when a section lists a gap. When you close, say the folder, the file, the `N`, and the state.

## Done

Before you close, evaluate this list and the `## Done` list in the reference for this situation. A command fixes the situation: use the reference that command names. Every item is true, or you fix the delivery in this turn. Do not leave a file that fails an item. Do not mark it `accepted` while an item fails. A template the reference names is applied and recorded under Assumed; the delivery uses the state that reference names. A prerequisite that still stops the delivery is not a failed list: follow "When a prerequisite is missing" and write no files for that piece.

- The situation of this turn is the only one written, unless the request asked for two. Each delivery has its own `<NNN>`.
- Files are only in the output folder, named as Delivery says. `<NNN>` is not reused. `STATUS.md` matches the files and the state this situation allows. `ORIGIN.json` is in that folder, its four fields match this plugin, and it has no row in `STATUS.md`. A gap the reference leaves as `proposed` stays `proposed`.
- The artifact language matches the request. `STATUS.md` columns stay `N`, `archivo`, `estado`, `sustituye`, `notas`.
- Every section the reference requires is present. Each explained section has a few plain sentences and one Mermaid diagram. The diagram is not called UML. A UML file this reference asks for is linked, or the section says it was asked of `plugin-uml-diagrams` and is not back yet.
- No part was invented. A gap that asks the person to supply a fact is the four-part gap in the report and in the reply: what is missing, how to fill it, the template, and one example. The example is marked as a sample and is not a fact. A gap that asks for nothing to be typed stays one line.
- The reply names the folder, the files, the `N`, and the state. When a prerequisite stops the piece, the reply is that same four-part gap and names no new file.

## Example

Input: a folder `apps/` whose `README.md` names three applications, `counter`, `cart`, and `orders`, and says the cart publishes an event that orders reads. The request is "write the 4+1 of apps, in English", and it names no command.

Output: `001-4plus1-counter-cart-orders.md`, state `proposed`. Sections Logical, Development, Process, and Physical each have a short text and a Mermaid diagram using only those three names and the event the README stated. The Scenarios section and the reply use the same four parts: what is missing (use cases to cite, not to write), how to fill it, the template with `#use-cases`, and one sample message. The sample is not a cited use case. The reply names `adrenaline/software-architect/`, the file, `001`, and `proposed`.
