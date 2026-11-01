<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="process.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Software Architect](../../../README.md) / [Describe the architecture](../SKILL.md)

# Process view

Source: Philippe Kruchten, IEEE Software, 1995. The file type is `process`. This is one section of the 4+1. The whole document is `/arch-4plus1`.

## What it fixes

How the parts call each other in one path. Also ask plugin-uml-diagrams for a UML 2 sequence and link the svg.

## How to do it

1. Read the folder the person named.
2. Write a few plain sentences, then one Mermaid diagram, as the skill defines.
3. Do not add the other four views in this file.

## Prompt

`/arch-4plus1-process` Read the folder #folder. Write this view of #system in #language.

## Done

- The file uses the template fields. A gap is a line, not a guess.
- An explained section has a few plain sentences and one Mermaid diagram. The diagram is not called UML.
- The state is `accepted` only when no gap remains. Otherwise it is `proposed`.
