# Changelog

## [Unreleased]

### Added

- One agent, `plugin-software-architect`. It follows this plugin's skills and names when to ask another plugin. The method stays in the skill.

## [0.0.1] - 2026-10-31

### Changed

- A gap that asks for a missing fact explains what is missing, how to fill it, shows the template, and adds one sample message. The same four parts go in the report and in the chat. The sample is not a cited fact.

### Added

- Evaluation of an architecture: quality scenario, options and tradeoff, and the decision record.
- One 4+1 document with five sections. Each section is a short explanation and one diagram.
- One arc42 manual. It cites the 4+1, the decisions, and the quality scenarios.
- A command per piece, prefixed by the document: `arch-4plus1`, `arch-arc42`, and `arch-evaluation`.
