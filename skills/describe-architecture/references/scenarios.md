<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="scenarios.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Software Architect](../../../README.md) / [Describe the architecture](../SKILL.md)

# Scenarios that tie the views

Source: Philippe Kruchten, IEEE Software, 1995, the "+1". The file type is `scenarios`. This is not the quality scenario. That one is `/arch-evaluation-scenario`.

## What it fixes

Which use cases exercise the four views. It cites them. It does not write them.

## How to do it

1. Cite a use case the person pasted, or an accepted file from `plugin-project-manager`.
2. For each use case, one sentence says which views it walks through.
3. One Mermaid diagram maps each use case to the views it touches. Boxes are the use-case names that were cited.
4. If none is cited, write no file. The chat uses the four-part gap from this skill. If a 4+1 file for this system already exists, put that same gap in its Scenarios section and keep that file `proposed`. The prompt is below. The example fills `#use-cases` with sample names and says which views each one walks. Mark the example as a sample. Do not store those names as cited use cases.

## Prompt

`/arch-4plus1-scenarios` These use cases tie the views of #system: #use-cases.

## Done

- The file uses the template fields. When no use case is cited, no scenarios file is written, and the reply is the four-part gap with an example besides the template. The example is not a cited use case. Any other gap is a line, not a guess.
- An explained section has a few plain sentences and one Mermaid diagram. The diagram is not called UML.
- The state is `accepted` only when no gap remains. Otherwise it is `proposed`.

- No use-case text was written here.
