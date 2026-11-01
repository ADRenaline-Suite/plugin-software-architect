# plugin-software-architect

Evaluates an architecture and writes two documents a reader can follow: the 4+1, one file with five sections, and the arc42 manual, which cites the 4+1. Each explained section is a few plain sentences and one diagram. The procedure is in `skills/describe-architecture/SKILL.md` and `skills/evaluate-architecture/SKILL.md`.

Files go in `adrenaline/software-architect/` at the project root, or in the path `.cursor/adrenaline.json` sets under `outputDirs["plugin-software-architect"]`. If `adrenaline/software-architect/` does not exist yet and `software-architect/` at the project root already has this plugin's `ORIGIN.json` or `STATUS.md`, keep writing there and say so. A part that no source named is a gap, not a guess. A UML drawing is asked of `plugin-uml-diagrams`. The Mermaid in the section is an explanation, not that drawing.
