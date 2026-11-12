# Design assumption change register

When client criteria or design assumptions change, the project engineer gets one sourced register: what changed, which recorded requirements it touches, how firm each source is, and what still needs confirmation. No design basis is altered.

*Workflow template · Engineering firms · Project and delivery · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/design-assumption-change-register/)*

## The outcome

The project engineer opens one page and sees every change to the design criteria since the design basis was issued. Each entry gives the recorded value, the value now being stated, the exact words and the date it came from, and who has or has not confirmed it. Where a client instruction, a workshop remark and an earlier register entry disagree, all of them are shown side by side and none is chosen.

The reason for a design decision stays findable. The responsible engineer confirms the technical basis, the client confirms the changed requirement, and the register shows which of those two is still outstanding for every line.

## Who starts the work, and when

The project engineer starts it when client criteria or design assumptions change: after a client instruction arrives, after a design workshop, or before a design-basis revision is issued. The responsible engineer and the client's named confirmer receive the lines that wait on them. It is run again whenever new instructions or notes arrive, with the previous register as an input.

## What they supply

- The recorded requirements from the design-basis document, as a list with a number, topic, value, unit and status for each.
- The client instructions, workshop notes and any confirmations received, one row each, with date, sender and text.
- The previous register, if there is one.
- The settings: the project, the design-basis reference and revision, who is the responsible engineer, who may confirm for the client, and today's date.

## What comes out

One register in a fixed order: changes, conflicts, items carried from the previous register, restatements, statements that match no recorded requirement, statements set aside, and the two confirmation lists. Every entry quotes its source. Differences are shown only as simple subtraction in the same unit. No technical consequence is assessed and no record is changed.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Engineering firms](https://fullypowered.ai/industries/engineering-firms/), where a design basis is issued once and the client's criteria keep moving.
- [Construction](https://fullypowered.ai/industries/construction/), where the designer and the builder both need to know which requirement a change touches.
- [Energy](https://fullypowered.ai/industries/energy/), where design criteria depend on figures from utilities and regulators that arrive late.
- [Project and delivery](https://fullypowered.ai/functions/project-and-delivery/), which owns the coordination records around the work.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where several projects run at once and each needs the same record kept the same way.

It is a different piece of work from [Decision log](https://fullypowered.ai/workflows/decision-log/), which records what leadership approved, and from [Scope change impact review](https://fullypowered.ai/workflows/scope-change-impact-review/), which estimates what new work does to effort, cost and dates. This one only records what changed in the criteria and how firm it is.

## What has to change for your company

Decide who may confirm for the client and write their names or roles into the settings. Decide what your firm treats as an instruction and where instructions must come from. Fix the column headers of your requirements list once. Choose where the register is kept and who reads it. Agree what the responsible engineer signs against. If your design-basis document is not a list of numbered values, build the requirements list first and run this on top of it.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried on its invented example in Claude on 10 November 2026; the record is published with it. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past change you already know, with cases written in advance: two values for one requirement from different client staff, a workshop remark that nobody approved, an instruction from someone who may not confirm. The responsible engineer checks every line against the source before anyone relies on the register. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 10 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 10 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete workflow template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the workflow template drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related workflow templates

- [Scope change impact review](https://fullypowered.ai/workflows/scope-change-impact-review/)
- [Decision log](https://fullypowered.ai/workflows/decision-log/)
- [Acceptance criteria sheet](https://fullypowered.ai/workflows/acceptance-criteria-sheet/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
