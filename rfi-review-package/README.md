# RFI review package

The project engineer gets one packet for each request for information: the register entry, the question word for word, the drawing revisions and specification extracts it touches, earlier responses, and a numbered list of what is unresolved. No answer is proposed.

*Workflow template · Engineering firms · Project and delivery · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/rfi-review-package/)*

## The outcome

A request for information usually arrives as an email or a form with a sentence or two and a drawing number. Before anyone can answer it, someone has to find the drawing at its current revision, pull the specification section, remember whether a similar question was answered a month ago, and work out who should look at it. This workflow template does that gathering and puts it on one page.

The packet shows the question exactly as the sender wrote it, the documents the sender cited set against the index of current revisions, the extracts you supplied quoted word for word, and every earlier response that touches the same documents. Where two documents print different values for the same item, both are shown side by side. Where the sender cites an old revision, mentions a site condition nobody has supplied, or hints at extra cost or time, it appears as a numbered question, addressed to the engineer or to the project manager.

The workflow template does not answer the question, says nothing about which document governs and checks no design. The responsible engineer reads the packet, interprets the design and approves the response. The project manager approves any commitment on cost or time.

## Who starts the work, and when

The project engineer, or the project coordinator working for them, starts it when a request for information reaches the design team, before it is routed to a reviewer. It can be run again after the person adds an extract, a missing revision or the sender's reply to a question.

## What they supply

- The request: its number, subject, sender, the discipline it is addressed to, the date received, the date the sender wants a response, the documents it cites, any site context, and the question as written.
- The document index: each drawing, specification section and bulletin with its current revision and the date of that revision.
- Extracts from the documents the request touches, each labelled with the document, revision and location.
- The prior responses on the project, with the documents each one cited.
- Your routing rules: which role reviews each discipline, and who approves a commitment.
- Today's date, who decides, and the response period your project allows.

## What comes out

One dated packet in a fixed order: a summary, the register entry, the documents the request cites checked against the index, documents that may be related, the extracts quoted word for word, printed values that differ, relevant prior responses, what the request mentions but nobody supplied, any wording that hints at cost or time, the proposed routing, and numbered questions. Where a section is empty it says so, and the packet states that no response has been drafted.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Engineering firms](https://fullypowered.ai/industries/engineering-firms/), where the design team receives questions from the contractor while the drawings keep changing.
- [Construction](https://fullypowered.ai/industries/construction/), for a firm whose own design team receives questions from the trades and wants each one tied to the right revision before it is routed.
- [Project and delivery](https://fullypowered.ai/functions/project-and-delivery/), which owns the response times the schedule depends on.
- [Quality management](https://fullypowered.ai/functions/quality-management/), which wants a record of what was in front of the reviewer when the response was given.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), with a standing request log and a routine for it.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when the number of open requests has outgrown one coordinator's memory.

## What has to change for your company

Set the response period your project allows and the field names your log uses. Write your routing rules: which role reviews each discipline and who approves a commitment. Decide which words should send a request to the project manager as a possible effect on cost or time. Agree how revisions are written so the index and the requests match exactly. This workflow template reads text and quotes it; it does not read drawings as images, check calculations or decide what a design means.

## What has been checked

Fully Powered AI wrote this workflow template in its own words from its own map of the work, with no third-party text. It was editorially reviewed on 10 November 2026. It was tried on its invented example in Claude on 10 November 2026; the record is published with it. Small wording edits made to the instructions and example after that trial have not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing on your project means running it on requests your project engineer already answered, with cases written in advance: a cited revision that is out of date, two documents that disagree, a request that mentions a condition nobody supplied. The project engineer checks every quotation and date against the documents before anyone relies on the packet. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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

- [Submittal register review](https://fullypowered.ai/workflows/submittal-register-review/)
- [Reviewer comments into one resolution list](https://fullypowered.ai/workflows/reviewer-comments-resolution-list/)
- [Project scope baseline](https://fullypowered.ai/workflows/project-scope-baseline/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
