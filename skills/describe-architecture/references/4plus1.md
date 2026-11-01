<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="4plus1.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Software Architect](../../../README.md) / [Describe the architecture](../SKILL.md)

# 4+1 document

Source: Philippe Kruchten, IEEE Software, 1995. The file type is `4plus1`.

## What it fixes

One document a reader can follow, divided into five sections: Logical, Development, Process, Physical, Scenarios. It does not wait for arc42 or for the evaluation.

## How to do it

1. Read the folder the person named. Use the names found there.
2. Write the five sections in that order. Each of the first four has two or three sentences and one Mermaid diagram, as the skill defines.
3. Process also asks `plugin-uml-diagrams` for a UML 2 sequence and links the `.svg`. Physical asks for a UML 2 deployment and links the `.svg`.
4. Scenarios cites use cases the person pasted or an accepted file from `plugin-project-manager`. It does not write the use-case text. If none is cited, that section is the four-part gap from this skill: what is missing, how to fill it, the template, and one example. The example is not a cited use case. The file stays `proposed`. The reply repeats those four parts.
5. A section with no facts still has its heading. If that gap asks the person to supply a fact, use the four-part gap. If it does not, one gap line. The other sections are written.

## Template

The file has the title, then five headings in this order: Logical view, Development view, Process view, Physical view, Scenarios. Under each of the first four: two or three sentences, one Mermaid diagram, and one sentence that says what the figure shows. Under Scenarios: the cited use cases, or the four-part gap.

## Prompt

`/arch-4plus1` Read the folder #folder. Write the 4+1 of #system in #language.

## Done

- The file uses the template fields. A gap that asks the person to supply a fact is the four-part gap, with an example besides the template. The example is not a fact. Any other gap is a line, not a guess.
- An explained section has a few plain sentences and one Mermaid diagram. The diagram is not called UML.
- The state is `accepted` only when no gap remains. Otherwise it is `proposed`.
