# Discipline interface issue register

After a coordination meeting exposes conflicts between disciplines, the design coordinator gets one register: each conflict from the minutes, linked to the clash-export rows and model revisions involved, with the lead who owns each system and the decision still needed. Nothing is resolved.

*Workflow template · Engineering firms · Project and delivery · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/discipline-interface-issue-register/)*

## The outcome

A conflict raised on Thursday does not go missing by the next meeting. The coordinator leaves the room with a numbered register: what the conflict is, in the words of the minutes, where it is, which systems and which disciplines are involved, which rows of the clash export touch it, which model revisions those rows were run against, and which lead owns each system.

Beside every issue sits the decision still needed, written as a question for the lead who makes it. Where the meeting reached a direction, the register records it as recorded, not as confirmed, until the lead says so in writing. Where nobody was asked to take an issue forward, or nobody owns a system, the register says so plainly and puts it on a short list for the coordinator.

The register also shows when a conflict was found against an old model. If the export was run on a structural revision that has since been replaced, the issue carries a question: does the conflict still stand on the current one?

The discipline leads still resolve the conflicts and approve any change. The assistant resolves no clash, proposes no design change and opens no model.

## Who starts the work, and when

The design coordinator starts it after a coordination meeting, once the minutes are written and the latest clash export and model revision index are to hand. It can be run again after the next meeting with the previous register, so earlier issues carry forward and none quietly drops out.

## What they supply

- The minutes of the coordination meeting.
- The clash-report export, as a table with set column headers.
- The model revision index: each model, its discipline, its current revision and the date of that revision.
- The firm's table of responsibilities: each system, its discipline and the lead who owns it.
- Any discipline sketches submitted, listed with the issue number they cite.
- The previous register, when there is one.

## What comes out

One register in a fixed order. Each issue has a number, the conflict, its location, the systems with their leads, the export rows linked (stated, or only possible), the model references each marked current, outdated or not in the index, the lead the minutes named, the direction the meeting recorded, the decision needed and its status. Under the issues: a short list for the coordinator to confirm, export rows nobody discussed, sketches that cite no issue and anything carried forward. If the inputs do not line up, the assistant stops and asks before writing anything.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Project and delivery](https://fullypowered.ai/functions/project-and-delivery/), which owns the thread from a design meeting to a decision somebody is accountable for.
- [Engineering firms](https://fullypowered.ai/industries/engineering-firms/), where the structural, civil, mechanical and electrical teams each keep their own model and their own view of the clash.
- [Construction](https://fullypowered.ai/industries/construction/), where a conflict carried between trades and consultants costs the most when it is found late.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where coordination lives in a few people's notebooks and should live in one register.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when more projects run at once than the coordinator can hold in mind.

It is a different piece of work from [three-week look-ahead constraint review](https://fullypowered.ai/workflows/three-week-look-ahead-constraint-review/), which looks at what could hold up planned site activity, from [project status report](https://fullypowered.ai/workflows/project-status-report/), which reports a project's workstreams to its sponsor, and from [design assumption change register](https://fullypowered.ai/workflows/design-assumption-change-register/), which records changes to client criteria and design assumptions against the design basis. None of them builds a register of conflicts between design disciplines.

## What has to change for your company

Fill in your responsibilities table first; the register is only as good as the owners it names, and the assistant invents none. Agree your discipline names and lead roles, how your clash tool labels its columns and statuses, and your model naming and revision scheme. Decide who writes the minutes and how a cited clash number appears in them, since a number in the minutes is what links an issue to its export row. Decide where the approved register lives and how a lead confirms a recorded direction in writing. The assistant works from files you supply and needs no connection to your modelling tools.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried on its invented example on 10 November 2026 in one run; the record is published with it, and lists the small edits made afterward that have not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on one or two past meetings your coordinator remembers well, plus hard cases written in advance: a system with no owner, a conflict cited in the minutes but missing from the export, an export run on an old revision, an item nobody was asked to take forward. The coordinator checks every link against the minutes and the export before anyone relies on the register. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) builds that test set, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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

- [Three-week look-ahead constraint review](https://fullypowered.ai/workflows/three-week-look-ahead-constraint-review/)
- [Project status report](https://fullypowered.ai/workflows/project-status-report/)
- [Design assumption change register](../design-assumption-change-register/)
- [Submittal register review](https://fullypowered.ai/workflows/submittal-register-review/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
