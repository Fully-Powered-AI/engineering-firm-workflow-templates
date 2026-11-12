# Deliverable issue completeness check

Workflow template, version 0.1.0.

## Purpose

Check one calculation, report or drawing package for completeness before it is issued, against the firm's own issue checklist. For every document and every checklist item that applies to it, the assistant reports Met, Not met or By hand, with the facts from the lists supplied: the revision in the index, the register and the title block; the review approval that exists and for which revision; the calculation a document cites and the revision it cites. Documents that appear in one list and not in another are set apart, and every gap is written as a question for a named role. The assistant prepares; it checks no calculation, judges no design, signs nothing off, and never issues, sends or changes anything.

## When to use it and when not to

Use it when a package is about to be issued: a day or two ahead, so there is time to fix what turns up, and again after the gaps are closed. It suits packages that carry an index, a revision register and recorded checker approvals.

Do not use it:

- to decide whether a calculation is correct or a design is adequate. A complete package does not establish either; the responsible engineer and the quality reviewer decide;
- to authorize issue. The assistant produces a checklist, not a release;
- to review a finished engagement file after the work is done; use completed engagement file review for that;
- to check a spreadsheet's formulas before it is shared; use spreadsheet check before sharing;
- to create a checklist for a firm that has none. The firm writes its issue checklist; this workflow template applies it.

## Roles

- **Runs it:** the quality reviewer or the document controller.
- **Answers the questions about each document:** its author, the responsible engineer or the document controller, as the question names.
- **Confirms technical adequacy and authorizes issue:** the responsible engineer and the quality reviewer. Always people.
- **The AI assistant:** reads the lists the person supplies and prepares the checklist. It changes no record and contacts nobody.

## Inputs

Everything is supplied by a person, as files or pasted text. No document system is connected, and the assistant never asks for a password or a login code.

1. **The issue checklist.** The firm's requirements, one row each. Default columns: `item_id,requirement,applies_to,test`. `applies_to` is `all` or a list of document types; `test` is one of `listed`, `revision-match`, `review-record`, `calc-reference` or `by-hand`. If the checklist is missing, stop. If a `test` is not one of the five, stop and ask what it means.
2. **The deliverable index.** Default columns: `doc_no,title,type,revision,title_block_revision,author`. If it is missing, stop. If a document number appears twice, stop and ask which row is right.
3. **The revision register.** Default columns: `doc_no,revision,date,description`, dates written year-month-day. If it is missing, stop.
4. **The recorded review approvals.** Default columns: `doc_no,revision,reviewer,date,outcome`. If they are not supplied, every `review-record` result is By hand, with "approvals not supplied" as the reason.
5. **The calculation references.** Default columns: `doc_no,calc_ref,calc_revision`, one row for each calculation a document cites. If they are not supplied, every `calc-reference` result is By hand, with "references not supplied" as the reason.
6. **The settings.** The package name, the purpose of issue and the planned date, the responsible engineer, the quality reviewer, who runs the check, today's date, and [your approved outcomes] (default: Approved). If the package name is missing, stop. If a role or a date is missing, write "not stated".

If any list's headers differ in any way from the defaults, stop, show the headers found beside the defaults, and ask which column is which. Never guess a column. If a file cannot be read, say so and ask for an export or pasted rows; never report what was not seen.

## The procedure

1. **Check the inputs.** Confirm one package and count the checklist items, the indexed documents and the rows in each list. Stop on the conditions in the inputs section.
2. **Find each document's current register revision.** It is the revision on the register row with the latest date for that document number. If two rows share the latest date, do not choose: the document's `revision-match` result is Not met with that fact. A document with no register rows has no register revision.
3. **Decide which items apply to which documents.** An item applies to a document when `applies_to` is `all` or lists the document's type, compared as written. Every applicable pair of item and document gets exactly one result: Met, Not met or By hand. Print the results in the checklist's order for each document and the index's order for the documents.
4. **Run each test as the checklist names it.**
   - `listed`: Met when the document has at least one register row. Otherwise Not met: no register entry.
   - `revision-match`: Met when the index revision, the register revision and the title block revision are the same text, compared exactly (P01 and P1 are different). Otherwise Not met, showing all three, or two with a note that the third does not exist. When the document has no register revision, say so and show the other two.
   - `review-record`: Met when an approval exists for the document at the index revision, its outcome is one of the approved outcomes, its reviewer is not the document's author, and its date is on or after the register date of that revision. Otherwise Not met, with the first reason that fits, in this order: no record for the document; records only for other revisions (name them); the outcome is not an approved outcome (quote it); the reviewer is the author; dated before the revision's register date (give both dates). When the document has no register date for the revision, the date part of the test is not run and the result says so.
   - `calc-reference`: look at every calculation the document cites. Met when each is in the index and is cited at the revision the index shows. Otherwise Not met, naming each citation that fails and why: not in the index, or cited at one revision while the index shows another. If the document cites no calculation, the result is By hand: no references supplied for that document. The responsible engineer decides, as for the `by-hand` test.
   - `by-hand`: By hand. Say the assistant cannot see what the item asks for, and who decides: the responsible engineer, unless the checklist row names someone else.
5. **Find the package-level discrepancies.** List every document number that is in the register, in the approvals or in the references as a cited calculation but not in the index. Print what was found and where. These are separate from the results and are counted separately.
6. **Write the questions.** One numbered question group for each document with at least one Not met, in the index's order, then one for each package-level discrepancy not already covered by a document's group. Each group states the facts and puts a question to the role that can answer it. Several Not met results on one document share one group, and a group may put questions to more than one role. Ask what is missing or which is right; do not offer a course of action. Recommend nothing unless the person asks.
7. **Count.** The header gives the number of results and how many are Met, Not met and By hand; they must add up. It also gives the number of documents with at least one Not met. Count again before returning.
8. **Return the checklist** to the person who ran it. The responsible engineer and the quality reviewer decide what happens next. After the gaps are closed, the person supplies corrected lists and the check runs again; the assistant does not carry results from the earlier run.

## Exceptions and stop conditions

- **No checklist, no index, no register or no package name:** stop and ask.
- **Headers that differ from the defaults, an unknown test word, or the same document number twice in the index:** stop and ask.
- **Approvals or references not supplied:** continue, and mark the affected results By hand with the reason; do not report them as missing.
- **Revision labels in a different style across the lists:** compare them exactly and report the mismatch as it is. Do not decide that P1 and P01 mean the same.
- **Two register rows for one document with the same latest date:** do not pick one.
- **Asked whether the package is correct, safe or ready to issue:** decline. The completeness check says what is present and what disagrees; adequacy and issue are for the responsible engineer and the quality reviewer.
- **Asked to correct a title block, edit the index or register, record an approval, change a revision, send the package or issue it:** decline and name the role that does it.
- **Asked to check a calculation's result or a drawing's content:** decline; record the request as an item for the responsible engineer.
- **The lists contain a password, a login code or a client's personal details:** do not repeat them; tell the person to remove them from the source.

## Output format

```
DELIVERABLE ISSUE COMPLETENESS CHECK: [package name]

For: [who runs it]. Purpose of issue: [purpose], planned [date] / planned date not stated. Responsible engineer: [name or role / not stated]. Quality reviewer: [name or role / not stated].
Prepared: [today's date / not stated], from the issue checklist ([n] items), the deliverable index ([n] documents), the revision register ([n] rows), the review approvals ([n] rows / not supplied) and the calculation references ([n] rows / not supplied). Outcomes that count as approved: [outcomes].
Results: [n] ([n] met, [n] not met, [n] left for a person). Documents with at least one not met: [n] of [n].

To settle before issue: [n]
[n]. [Document number or package item]: [the facts]. Question for [role]: [the question]. [Question for another role: the question, if the group needs one.]

Document by document

[Document number] [Title] ([type], revision [index revision])
  [Item id] [Met / Not met / By hand]: [the facts, from the lists supplied][. See n.]
  ...

Package-level discrepancies: [n]
In the register and not in the index: [document number, revision, date, description as given / none][. See n.]
Cited and not in the index: [document number (cited by ... at revision ...) / none][. See n.]
In the review approvals and not in the index: [document numbers / none][. See n.]

Left for a person: [n]
[Document number] [Item id]: [what the person checks and who decides / none].

Completeness check only. No calculation has been checked, no design judged and nothing signed off, issued, changed or sent. [Responsible engineer] and [quality reviewer] confirm technical adequacy and authorize issue.
```

Write dates as day, month in words and year (15 October 2026). When "To settle before issue" is empty, print "To settle before issue: 0" and "Nothing to settle." When a document has no applicable items, print "No checklist items apply." under it. Print "Left for a person: 0" and "None." when there are none. The package-level count is the number of lines that report a finding, not the lines that say none.

## Reviewer checklist

1. Every document in the index appears once, and every result traces to a row in a list supplied. (Document controller)
2. The numbers in the header add up and match the lines below. (Document controller)
3. Each revision comparison uses the exact labels in the lists, and each date comparison is right. (Document controller)
4. Each Not met result is a fact about the lists and none is written as a conclusion about the design. (Quality reviewer)
5. Every question is addressed to a role that can answer it, and none recommends a technical answer. (Quality reviewer)
6. Every By hand item has a person who decides it. (Responsible engineer)
7. The checklist was supplied by the firm and no item was added or dropped by the assistant. (Quality reviewer)
8. Nothing has been issued, signed, edited or sent by the assistant. (Quality reviewer)

## Acceptance tests

Proposed tests. None has been run.

1. **A clean package.** Every document listed, revisions agree, approved by someone other than the author, calculations cited at current revisions. Expected: every result Met except `by-hand` items; "Nothing to settle."
2. **Title block differs.** The index and register agree and the title block shows an earlier revision. Expected: `revision-match` Not met with all three shown; no guess about which is right.
3. **Approval for an earlier revision.** Expected: Not met naming the revision the record is for.
4. **Approval by the author.** Expected: Not met, reviewer is the author.
5. **Approval dated before the revision.** Expected: Not met with both dates.
6. **Approval outcome not in the approved list.** An outcome of "Approved with comments" when only "Approved" counts. Expected: Not met quoting the outcome.
7. **Out-of-date calculation citation.** Expected: Not met naming the cited and the current revision.
8. **Calculation cited that is not in the index.** Expected: Not met on the document and a package-level discrepancy, with one question group.
9. **A document in the register and not in the index.** Expected: a package-level discrepancy and its own question; no result for it.
10. **Document with no register rows.** Expected: `listed` Not met; `revision-match` Not met saying there is nothing to compare.
11. **Two register rows with the same latest date.** Expected: no choice made, `revision-match` Not met with that fact.
12. **Revision labels P1 and P01.** Expected: reported as a mismatch.
13. **Approvals not supplied.** Expected: `review-record` results By hand with the reason; none reported as missing.
14. **Headers that differ.** Expected: the assistant stops and asks which column is which.
15. **Asked to say the package is ready, or to fix the title block.** Expected: declines, names the roles.
16. **Same number twice in the index.** Expected: stops and asks.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You check one calculation, report or drawing package for completeness
before issue, against the firm's own issue checklist, for a quality
reviewer or document controller. You prepare; people decide. You check
no calculation, judge no design and sign nothing off. You never issue,
send, correct, record or change anything, and you never ask for a
password or a login code. The responsible engineer and the quality
reviewer confirm technical adequacy and authorize issue.

The user will supply: the issue checklist (item_id, requirement,
applies_to, test); the deliverable index (doc_no, title, type, revision,
title_block_revision, author); the revision register (doc_no, revision,
date, description); the review approvals (doc_no, revision, reviewer,
date, outcome); the calculation references (doc_no, calc_ref,
calc_revision); and the settings (package name, purpose and planned date
of issue, the responsible engineer and quality reviewer, who runs the
check, today's date, the outcomes that count as approved, default
"Approved"). If the checklist, index, register or package name is
missing, stop and ask. If any list's headers differ from these, stop,
show the headers found beside these, and ask which column is which; never
guess. If a test word is not one of: listed, revision-match,
review-record, calc-reference, by-hand, or a document number appears
twice in the index, stop and ask. If a file cannot be read, say so and
ask for an export or pasted rows; never report what was not seen. If the
approvals are not supplied, mark every review-record result By hand with
the reason "approvals not supplied"; if the references are not supplied,
mark every calc-reference result By hand with the reason "references not
supplied". Continue in both cases and do not report them as missing. If a role or a date in the settings is
missing, write "not stated".

1. A document's register revision is on its register row with the latest
   date. If two rows share the latest date, choose neither: its
   revision-match result is Not met, with that fact. A document with no
   register rows has no register revision.
2. An item applies to a document when applies_to is "all" or lists the
   document's type. Give every applicable pair of item and document one
   result: Met, Not met or By hand. Documents in index order, items in
   checklist order.
3. listed: Met if the document has at least one register row; otherwise
   Not met: no register entry.
   revision-match: Met if the index, register and title block revisions
   are identical text, compared exactly (P01 and P1 are different);
   otherwise Not met, showing all three, or two with a note that the
   third does not exist. If the document has no register revision, say so
   and show the other two.
   review-record: Met if an approval exists at the index revision with an
   approved outcome, by someone other than the author, dated on or after
   the register date of that revision. Otherwise Not met with the first
   reason that fits, in this order: no record for the document; records
   only for other revisions (name them); the outcome is not an approved
   outcome (quote it); the reviewer is the author; dated before the
   revision's register date (give both dates). If the revision has no
   register date, do not run the date test and say so in the result.
   calc-reference: Met if every calculation cited is in the index and
   cited at the revision the index shows; otherwise Not met naming each
   failing citation and why (not in the index, or cited at one revision
   while the index shows another). A document citing none is By hand: no
   references supplied for that document; the responsible engineer
   decides.
   by-hand: By hand. Say you cannot see what the item asks for, and name
   who decides (the responsible engineer unless the checklist says
   otherwise).
4. List package-level discrepancies: numbers in the register, the
   approvals or the references (as a cited calculation) that are not in
   the index. Print what was found and where. Count them separately from
   the results.
5. Write one numbered question group per document with a Not met result,
   in index order, then one per package-level discrepancy not already
   covered. Each states the facts and puts a question to a role; a group
   may put questions to more than one role. Ask what is missing or which
   is right; do not offer a course of action. Recommend nothing unless
   asked.
6. The header counts results and they must add up: met, not met and by
   hand. It also counts the documents with at least one Not met. Count
   again before you return the checklist. Say nothing about whether a
   design or calculation is correct.
7. Use the output format exactly, with dates as day, month in words and
   year, and the closing line that says nothing has been issued, changed
   or sent. When there is nothing to settle, print "To settle before
   issue: 0" and "Nothing to settle." When a document has no applicable
   items, print "No checklist items apply." under it. When nothing is
   left for a person, print "Left for a person: 0" and "None." The
   package-level count is the number of lines that report a finding, not
   the lines that say none.

If asked whether the package is correct, safe or ready to issue, decline
and name the responsible engineer and the quality reviewer. If asked to
correct a title block, edit a list, record an approval, change a revision
or send or issue the package, decline and name the role that does it. If
asked to check a calculation or a drawing's content, decline and record
the request for the responsible engineer. If the lists contain a password,
a login code or a client's personal details, do not repeat them; tell
the user to remove them. Check every
count and every date comparison before you return the checklist.
```

## What to customize

- The checklist itself: your own requirements, their identifiers and the test for each. Add items that stay By hand, such as the responsible engineer's confirmation of the design basis.
- Your approved outcomes, and whether an approval by a document's author may ever count.
- Your revision labelling convention. The comparison is exact, so decide whether a package uses one style throughout.
- The document types, and which checklist items apply to which.
- The columns of your index, register, approvals and references. Change the defaults once if your document system exports other names.
- Who answers each kind of question when the named role is away.
- Which packages the check is run on, and how long before the issue date.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI from its own map of the work, with no third-party text. Editorially reviewed. Tried once on its invented example in Claude on 10 November 2026; the record is published with it. That run was blind on the inputs and found ambiguities and gaps in the instruction block, since edited; edits made after it, to the instructions, the output format and the example's wording, have not been run again. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
