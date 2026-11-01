---
name: arch-help
description: "ADRenaline. Help: catalog of plugin-software-architect (skills, rules, commands)."
---

# Help — ADRenaline Software Architect

Print this catalog as the reply. Do not run any skill or command. Do not invent entries that are not listed. If a component was added to the plugin and is missing here, add one line from its frontmatter `description` and say the catalog was refreshed.

When this help command is the first command in the message, every command, skill, or rule named after it is the subject of the help. Do not run those names. Do not print the full catalog. For each name, in the order given, print its catalog line (the linked id and the sentence). When the README has a heading for that command, also print the paragraphs under that heading, up to the next heading. A skill name uses the skill's catalog line and the README group that names that skill, up to its first command heading. A name that is not in this catalog is one line: it is not in this plugin. Do not invent what it does, and do not write a file.

Write the sentences in the language of the request. Keep command names, file ids, and every URL unchanged. Every id is a markdown link to the GitHub URL on its line. Do not print a repository `name` as the visible label of a plugin.

Keep the section headings, in this order: Plugin, Commands, Skills, Rules, then Agents, Hooks, and MCP when the plugin has them, then Output, then Not in this plugin. The title and the Plugin line show `ADRenaline` plus the `displayName`, then one sentence on what the plugin does. Under Commands, group the lines by the skill named in the line. Each group opens with that skill name linked to its SKILL.md. One line per item: the linked id, then the sentence. Output links this plugin's GitHub repository under that same label. A plugin under Not in this plugin uses `ADRenaline` plus its short name, and links to `https://github.com/<owner>/<other-plugin>` only when that repository exists.

## Plugin

- [**ADRenaline Software Architect**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/README.md) — Evaluates an architecture and writes the 4+1 views and the arc42 manual. Each section is plain language plus a diagram.

## Commands

- [**/arch-help**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/README.md) — This help (one-line catalog of the plugin).
- [**describe-architecture**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/skills/describe-architecture/SKILL.md) — Writes the 4+1 document and the arc42 manual so a reader can follow them.
- [**/arch-4plus1**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/skills/describe-architecture/references/4plus1.md) — 4+1 document: logical, development, process, physical, and the scenarios that tie them, one section each, with a diagram in every view.
- [**/arch-4plus1-logical**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/skills/describe-architecture/references/logical.md) — Logical view: the responsibility of each part, in plain language and one diagram.
- [**/arch-4plus1-development**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/skills/describe-architecture/references/development.md) — Development view: how the code is organized, in plain language and one diagram.
- [**/arch-4plus1-process**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/skills/describe-architecture/references/process.md) — Process view: how the parts call each other, in plain language, one diagram, and a UML 2 sequence.
- [**/arch-4plus1-physical**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/skills/describe-architecture/references/physical.md) — Physical view: where each part runs, in plain language, one diagram, and a UML 2 deployment.
- [**/arch-4plus1-scenarios**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/skills/describe-architecture/references/scenarios.md) — Scenarios that tie the 4+1 views: which use cases exercise them. It does not write the use cases.
- [**/arch-arc42**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/skills/describe-architecture/references/arc42.md) — arc42 manual: the twelve sections, citing the 4+1, the decisions, and the quality scenarios, with a diagram where a section explains a picture.
- [**/arch-arc42-context**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/skills/describe-architecture/references/context.md) — System context: what sits outside the system, with one diagram of the boundary.
- [**/arch-arc42-strategy**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/skills/describe-architecture/references/strategy.md) — Solution strategy: the quality goals, the constraints, and the chosen approach.
- [**/arch-arc42-concepts**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/skills/describe-architecture/references/concepts.md) — Crosscutting concepts: what repeats across the parts.
- [**/arch-arc42-risks**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/skills/describe-architecture/references/risks.md) — Risks and technical debt: what a source already says is wrong or undecided.
- [**/arch-arc42-glossary**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/skills/describe-architecture/references/glossary.md) — Architecture glossary: one term per concept in this description.
- [**evaluate-architecture**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/skills/evaluate-architecture/SKILL.md) — Evaluates one architecture concern and records the decision.
- [**/arch-evaluation**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/skills/evaluate-architecture/references/evaluation.md) — Architecture evaluation: the concern, the six-part scenario, the options, and the decision, with a diagram of the options.
- [**/arch-evaluation-scenario**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/skills/evaluate-architecture/references/quality-scenario.md) — Quality scenario: the concern and the six-part scenario for one architectural characteristic.
- [**/arch-evaluation-tradeoff**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/skills/evaluate-architecture/references/tradeoff.md) — Architecture tradeoff: the options in play and what each one costs, with one diagram.
- [**/arch-evaluation-adr**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/skills/evaluate-architecture/references/adr.md) — Architecture decision record: a decision already taken, with its context and consequences.

## Skills

- [**describe-architecture**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/skills/describe-architecture/SKILL.md) — Writes the 4+1 document and the arc42 manual. Each section is a few plain sentences and one diagram.
- [**evaluate-architecture**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/skills/evaluate-architecture/SKILL.md) — Writes the quality scenario, the options and the tradeoff, and the decision record.

## Rules

- [**output-folder**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/rules/output-folder.mdc) — Every file goes in `adrenaline/software-architect/` (or in `outputDirs["plugin-software-architect"]` of `.cursor/adrenaline.json`). The artifact follows the language of the request.
- [**architecture-description**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/rules/architecture-description.mdc) — Each explained section is plain language plus one diagram. The arc42 manual cites the 4+1.
- [**architecture-evaluation**](https://github.com/ADRenaline-Suite/plugin-software-architect/blob/main/rules/architecture-evaluation.mdc) — A scenario has six parts. Fewer than two options leaves the file proposed.

## Output

- Repository: [**ADRenaline Software Architect**](https://github.com/ADRenaline-Suite/plugin-software-architect).
- Folder: `adrenaline/software-architect/` (override via `.cursor/adrenaline.json`). An existing `software-architect/` at the project root keeps receiving files.
- Name: `<NNN>-<type>-<topic>.md`, with monotonic `<NNN>`. The prose follows the language of the request. The type stays the English piece id.

| Format | Description |
| --- | --- |
| `.md` | A 4+1 document, one view, the arc42 manual, one arc42 section, an evaluation, a quality scenario, a tradeoff, or an ADR. |
| `STATUS.md` | State of each file. Columns stay `N`, `archivo`, `estado`, `sustituye`, `notas`. |
| `ORIGIN.json` | Folder marker: `suite`, `plugin`, `repository`, `convention` `adr-001`. Not an `<NNN>` file. |

## Not in this plugin

- UML diagram → [**ADRenaline UML Diagrams**](https://github.com/ADRenaline-Suite/plugin-uml-diagrams).
- Use case → ADRenaline Project Manager (`plugin-project-manager`).
- OpenAPI contract → ADRenaline APIs (`plugin-apis`).
- Threat model → ADRenaline Security (`plugin-security`).
- Data model → ADRenaline Data (`plugin-data`).
- Domain model → ADRenaline Backend (`plugin-backend`).
- Tutorial, how-to, reference, or explanation for a reader → ADRenaline Documentation (`plugin-documentation`).
- Screen specification → [**ADRenaline UI/UX Design**](https://github.com/ADRenaline-Suite/plugin-ui-ux-design).

In Claude Code, commands use the prefix `/plugin-software-architect:` (example: `/plugin-software-architect:arch-help`).

## Done

- With no names after this command, the reply is this catalog. Every id is a markdown link to the GitHub URL listed here. Commands are grouped by skill.
- With names after this command, the reply is only the help for those names, in that order: the catalog line and, when the README has it, the paragraphs under that heading. The other names were not run.
- No skill ran. No command ran. No file was written.
- No entry was invented. If a component exists in the plugin and is missing here, one line was added from its `description` and the reply says the catalog was refreshed.
