<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="context.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Software Architect](../../../README.md) / [Describe the architecture](../SKILL.md)

# Context

Source: arc42 template 9.1. The file type is `context`. The whole manual is `/arch-arc42`.

## What it fixes

What sits outside the system and which interfaces cross the boundary. One diagram: the system in the center.

## How to do it

1. Read the folder the person named.
2. Follow the diagram rule in the skill when this section explains a picture.
3. Do not write the other arc42 sections in this file.

## Prompt

`/arch-arc42-context` Read the folder #folder. Write this section of #system in #language.

## Done

- The file uses the template fields. A gap is a line, not a guess.
- An explained section has a few plain sentences and one Mermaid diagram. The diagram is not called UML.
- The state is `accepted` only when no gap remains. Otherwise it is `proposed`.
