# AI workflow templates for engineering firms

FullyPowered Workflow Templates for engineering firms turn the AI your firm already pays for into a team that knows how the work is done: a project engineer with every request for information packed for review, a design coordinator with the conflicts between disciplines gathered into one register, a quality reviewer with the drawing package checked for gaps before issue. 6 workflow templates, made to be customized and deployed. All plain Markdown, all free, MIT license.

We are FullyPowered AI. We build AI workflows for companies, and these are the templates we start from. We publish them because a good starting point should be open to everyone. Copy one. Change it. Make it yours.

> [!TIP]
> **Missing a template that is not listed here, or want these customized for your organization? Reach out to us.** These are templates, made to be customized and deployed. FullyPowered AI customizes and builds AI workflows, connects them to your business systems, installs them in your agents and puts them in the hands of the people who own the work. [See more examples for engineering firms](https://fullypowered.ai/industries/engineering-firms/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=engineering-firm-readme&from=gh-engineering-firm-readme) · [Have one built for your team](https://fullypowered.ai/pricing/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=engineering-firm-readme&from=gh-engineering-firm-readme). Not sure where to start? Email hello@fullypowered.ai and a person will answer.

**Who this is for**

- Principals and managing directors who want AI to carry real project work across the firm.
- Heads of project delivery who want coordinators running a consistent method on every project this week.
- The project manager or coordinator, who gets each packet prepared and still makes every engineering call.

**What these are for**

- **Your best way of doing it, for the whole team.** One piece of work, written down precisely enough that an assistant prepares it the same way every time.
- **Work you can check.** Every template says what it needs, what it produces, what it checked and what it could not.
- **A person decides.** Anything that sends, posts, pays or changes a record waits for someone to approve it.
- **Tied into your business systems.** A workflow can be designed to pull from the systems your company already runs, and even push data back into them, with guardrails and a person approving. [Browse the Connectors Directory](https://fullypowered.ai/connectors/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=engineering-firm-readme&from=gh-engineering-firm-readme).
- **Free, open and portable.** MIT-licensed plain instructions that run in the assistant or agent your team already uses: ChatGPT, Claude, Claude Code, Claude Cowork, Codex, Copilot, Gemini, Grok, Perplexity.

**Quick start**

1. **Prepare one request for information in a few minutes.** Open ChatGPT, Claude, Copilot or Gemini. Copy the text below into a new chat. Then paste in one real request for information from a contractor, your list of current drawing revisions, and any earlier answers on the project. Replace the square brackets with your own details. No sign-in to anything of ours, and nothing to download.

   ```text
   You prepare a review packet for a project engineer. You prepare; people
   decide. Never answer the technical question, say which document governs,
   check a design, estimate cost or time, or contact anyone. The engineer
   decides. I will paste: one request for information (number, subject,
   sender, discipline, dates, documents cited, the question), my document
   list with current revisions, short quotes from the documents it touches,
   and earlier responses. Today is [date]. Project: [name]. Build one
   packet: the request with the question word for word; each cited document
   checked against the current revision; quotes word for word; places where
   two documents print different values; earlier responses that touch the
   same documents; anything mentioned but not supplied; wording that hints
   at cost or time; then numbered questions for the engineer and the
   project manager. Say plainly that no response has been drafted. If
   something is missing, ask me instead of guessing.
   ```

2. Read what comes back. It marks what it checked and what is left for you. What a packet looks like, with invented data:

   ```text
   RFI REVIEW PACKAGE: Alder Street Parking Structure, RFI-0042

   For: project engineer. Prepared Monday 16 November 2026 from: RFI text, document index (7 rows), extracts (3), prior responses (4 rows), routing rules (2 rows), settings.
   Column check: all labels and headers matched.
   Settings: response period 7 days, counted in calendar days. Defaults used: response period, effect words, stop words.
   Summary: RFI-0042, response due in 4 days. Documents cited: 3 (1 revision differs, 0 not in index). Possibly related, not cited: 1. Printed values that differ: 1. Prior responses listed: 3 of 4 checked (2 cite an older revision). Mentioned but not supplied: 1. Possible effects on cost or time: 1. Open questions: 7 (6 for the responsible engineer, 1 for the project manager).
   ```

3. Stop there. You will know if this is for you. When you want it fitted to your company, or built into your agents, [that is what we do](https://fullypowered.ai/pricing/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=engineering-firm-readme&from=gh-engineering-firm-readme).

A person starts each workflow, supplies the inputs and decides; the template prepares and checks, and the engineers design, review and sign.

These are samples and a starting point, made to be changed to fit how your firm names things and who signs what. Your own work may not appear here, and a workflow can be one step or many, so we can build the one your firm needs.

## The workflow templates here today

- **[Deliverable issue completeness check](deliverable-issue-completeness-check/)**: As a calculation, report or drawing package nears issue, the quality reviewer or document controller gets a checklist: missing review records, revisions that disagree between the index, the register and the title block, and citations of out-of-date calculations. Issue stays with the engineers.
- **[Design assumption change register](design-assumption-change-register/)**: When client criteria or design assumptions change, the project engineer gets one sourced register: what changed, which recorded requirements it touches, how firm each source is, and what still needs confirmation. No design basis is altered.
- **[Discipline interface issue register](discipline-interface-issue-register/)**: After a coordination meeting exposes conflicts between disciplines, the design coordinator gets one register: each conflict from the minutes, linked to the clash-export rows and model revisions involved, with the lead who owns each system and the decision still needed. Nothing is resolved.
- **[Project experience sheet](project-experience-sheet/)**: For one finished project and one proposal, turn the firm's approved project records into a one-page experience sheet: the firm's role, the scope it performed, partners' work kept apart, and the record behind each line. Names, images and permissions still to confirm are listed for sign-off.
- **[RFI review package](rfi-review-package/)**: The project engineer gets one packet for each request for information: the register entry, the question word for word, the drawing revisions and specification extracts it touches, earlier responses, and a numbered list of what is unresolved. No answer is proposed.
- **[Site observation follow-up](site-observation-follow-up/)**: After a site visit, the visiting engineer and the project manager get one observation report: each field note beside its location, source photograph, drawing revision and any earlier register entry, a proposed follow-up owner, and the questions still open. It assesses no condition.

## How to use one

Open a folder and start with its README. Every folder stands alone, so copy the one you want and leave the rest. The templates are written for ChatGPT, Claude, Copilot and Gemini: paste the instruction block and the output format in as custom instructions, or load the folder in a product that reads `SKILL.md` packages.

To take the whole collection, press **Use this template** at the top of this page: it copies every folder into a repository in your own account, yours to change.

In every template a person starts the work, supplies the inputs and decides. The template prepares and checks. Anything that sends, posts, pays or changes a record waits for a person to approve it.

## What SKILL.md is

Each folder holds a file named `SKILL.md`. It is the technical file: the same instructions and output format as the template, in the packaged form that AI products which load instructions from a folder read. It is generated from `TEMPLATE.md`, so the two always agree. The workflow template is the whole folder; `SKILL.md` is one way of loading it. If your AI product does not read that format, use `TEMPLATE.md`.

## What "checked" means here

Each folder says exactly what was checked and when: who wrote it, that its sources and rights were reviewed, the date of its editorial review, and whether it has been tried on its invented example in a named AI product. Nothing is described as tested for a client unless it was. Test a template on your own past work before your team relies on it; each one comes with acceptance tests for that.

## More workflow templates

The [FullyPowered Workflows Directory](https://fullypowered.ai/workflows/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=engineering-firm-readme&from=gh-engineering-firm-readme) lists every workflow template across functions and industries, with search. A machine-readable list of this repository is in [index.json](index.json).

For the work these templates come from, by area of the business and by task, see [AI workflow examples for engineering firms](https://fullypowered.ai/industries/engineering-firms/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=engineering-firm-readme&from=gh-engineering-firm-readme).

## Licence and credits

MIT, in [LICENSE](LICENSE) and in every folder. Each folder's SOURCES.md names what the workflow template drew on. Published by [FullyPowered AI](https://fullypowered.ai/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=engineering-firm-readme&from=gh-engineering-firm-readme).
