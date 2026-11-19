# Deliverable issue completeness check

A checklist of missing review records and revisions that disagree before a package is issued. Issue stays with the engineers. Free template.

> [!TIP]
> **Missing a template that is not listed here, or want these customized for your organization? Reach out to us.** This is a template, made to be customized and deployed. FullyPowered AI customizes and builds AI workflows, connects them to your business systems, installs them in your agents and puts them in the hands of the people who own the work. [See Deliverable issue completeness check on our website](https://fullypowered.ai/workflows/deliverable-issue-completeness-check/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=engineering-firm-deliverable-issue-completeness-check&from=gh-deliverable-issue-completeness-check) Not sure where to start? Email hello@fullypowered.ai and a person will answer.

**Quick start**

1. Read EXAMPLE.md to see what a good result looks like.
2. Copy all of TEMPLATE.md into your assistant, then give it your own inputs, or the invented ones from EXAMPLE.md.
3. Read what comes back. It marks what it checked and what is left for you.

*Workflow template · Engineering firms · Quality management · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/deliverable-issue-completeness-check/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=engineering-firm-deliverable-issue-completeness-check&from=gh-deliverable-issue-completeness-check)*

## The outcome

The question on the day before issue is rarely "is the design right?" It is "is everything that should be in this package actually here, and does it all refer to the same version of itself?" Answering that by hand means opening the index, the revision register, the review records and every drawing's title block, and comparing them one at a time.

This workflow template does that comparison against your firm's own issue checklist. For every document in the package it reports each checklist item as met, not met, or left for a person, with the facts beside it: the revision the index shows, the revision the register shows, the revision on the title block; the review record that exists, and for which revision, by whom, and when; the calculation a drawing cites and the revision it cites. Documents that appear in one list and not another are set apart.

A package can be complete and still wrong, and this check says nothing about which. It does not check a calculation, judge a design or sign anything off. The responsible engineer and the quality reviewer confirm technical adequacy and authorize issue, and every gap is written as a question for them.

## Who starts the work, and when

The quality reviewer or the document controller starts it when a package is about to be issued, usually a day or two ahead so there is time to fix what turns up. It is run again after the gaps are closed, to see what remains. Nothing is connected: the person supplies the lists.

## What they supply

- **The issue checklist,** one row per requirement: an identifier, the requirement, the document types it applies to, and which test the check should run.
- **The deliverable index** for the package: document number, title, type, revision, the revision on the title block, and author.
- **The revision register:** each revision of each document, with its date and a short description.
- **The recorded review approvals:** document, revision, reviewer, date and outcome.
- **The calculation references:** which calculation, at which revision, each report or drawing cites.
- **A few settings:** the package name, the purpose and planned date of issue, the names of the responsible engineer and the quality reviewer, today's date, and the outcomes that count as approved.

If a list's columns are named differently from the ones the template expects, the assistant stops and asks which is which.

## What comes out

1. **A header** naming the package, the purpose of issue, who confirms and who authorizes, and counts that add up: results met, not met and left for a person.
2. **What to settle before issue,** a numbered list of questions for the responsible engineer, the quality reviewer or the document controller.
3. **Document by document,** each checklist item that applies to it with its result and the facts.
4. **Package-level discrepancies:** documents found in the register, in the review approvals or cited by another document but missing from the index.
5. **Items left for a person,** with the person who decides each.

In a good checklist, every result traces to a row in a list you supplied, and no gap is described as a conclusion about the design.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Quality management](https://fullypowered.ai/functions/quality-management/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=engineering-firm-deliverable-issue-completeness-check&from=gh-deliverable-issue-completeness-check): the reviewer who confirms that a package is ready before it is issued.
- [Project and delivery](https://fullypowered.ai/functions/project-and-delivery/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=engineering-firm-deliverable-issue-completeness-check&from=gh-deliverable-issue-completeness-check): project managers and document controllers who run the issue date.
- [Engineering firms](https://fullypowered.ai/industries/engineering-firms/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=engineering-firm-deliverable-issue-completeness-check&from=gh-deliverable-issue-completeness-check): calculation, report and drawing packages with a checker's approval on record.
- [Construction](https://fullypowered.ai/industries/construction/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=engineering-firm-deliverable-issue-completeness-check&from=gh-deliverable-issue-completeness-check): design and delivery packages going to a contractor or an authority.
- [Professional services](https://fullypowered.ai/industries/professional-services/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=engineering-firm-deliverable-issue-completeness-check&from=gh-deliverable-issue-completeness-check): technical advisory work released as reports with supporting calculations.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=engineering-firm-deliverable-issue-completeness-check&from=gh-deliverable-issue-completeness-check): firms with an issue procedure that already exists and needs to be applied the same way each time.

## What has to change for your company

Your own issue checklist is the standard, so the first change is to put it in the template's columns and choose a test for each row. Decide which outcomes count as approved and whether an approval may be given by the author of the document, as the template assumes it may not. Set the revision labelling convention you use, because the check compares labels exactly. Add the item types you want left for a person. Agree who decides each kind of gap. It runs in ChatGPT, Claude, Copilot or Gemini; decide which exports it may be given.

## What has been checked

FullyPowered AI wrote this workflow template in its own words from its own map of the work, with no third-party text. It was editorially reviewed on 10 November 2026. It was tried once on its invented example in Claude on 10 November 2026; the record is published with it. The run was blind on the inputs, so the example's output was not visible to it, and it found ambiguities and gaps in the instruction block, since edited. Edits made afterward to the instructions, the output format and the example's wording have not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

- Written by FullyPowered AI.
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

- [Completed engagement file review](https://fullypowered.ai/workflows/completed-engagement-file-review/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=engineering-firm-deliverable-issue-completeness-check&from=gh-deliverable-issue-completeness-check)
- [Spreadsheet check before sharing](https://fullypowered.ai/workflows/spreadsheet-check-before-sharing/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=engineering-firm-deliverable-issue-completeness-check&from=gh-deliverable-issue-completeness-check)
- [Submittal register review](https://fullypowered.ai/workflows/submittal-register-review/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=engineering-firm-deliverable-issue-completeness-check&from=gh-deliverable-issue-completeness-check)

## Make it yours

This workflow template is an example and a starting point. FullyPowered AI adapts it to how your company works, proves it on real work and rolls it out to the roles that use it. We can also build any other workflow for your company, including one that runs several steps, in a Workflow Sprint or a scoped implementation. [Talk with us](https://fullypowered.ai/contact/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=engineering-firm-deliverable-issue-completeness-check&from=gh-deliverable-issue-completeness-check).
