<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="quality-scenario.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Software Architect](../../../README.md) / [Evaluate the architecture](../SKILL.md)

# Quality scenario

Source: ATAM and the Quality Attribute Workshop. ISO/IEC 25010:2023. The file type is `quality-scenario`. This is not `/arch-4plus1-scenarios`.

## What it fixes

One concern written so it can be checked: source of the stimulus, stimulus, environment, artifact, response, and response measure. The quality name is one of the nine current names.

## How to do it

1. Fill the six parts from what the person said or from a file that was read. A part they did not give stays a gap and the file stays `proposed`.
2. No diagram in this file. The options diagram belongs to the tradeoff.

## Template

```markdown
# <title>

- Characteristic: <one ISO/IEC 25010:2023 name>
- Source of the stimulus:
- Stimulus:
- Environment:
- Artifact:
- Response:
- Response measure:
```

## Prompt

`/arch-evaluation-scenario` The concern is #concern. The characteristic is #characteristic.

## Done

- The file uses the template fields. A gap is a line, not a guess.
- An explained section has a few plain sentences and one Mermaid diagram. The diagram is not called UML.
- The state is `accepted` only when no gap remains. Otherwise it is `proposed`.

- The six parts are present or marked as a gap.
