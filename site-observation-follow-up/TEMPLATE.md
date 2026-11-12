# Site observation follow-up

Workflow template, version 0.1.1.

## Purpose

Prepare one observation report after a site visit from what the visitor already has: the field notes, the approved photographs, the drawing register, the prior observation register and a list of proposed follow-up roles. Each note is shown with its location, whether it was observed or reported, the photograph that goes with it, the drawing revision the visitor had in hand beside the current one, the earlier register entry it touches and a proposed follow-up owner. What is missing or does not agree becomes a numbered question. The assistant prepares; it never assesses a condition, says that anything is complete, compliant or safe, judges a photograph, assigns work or changes a record. The visiting engineer verifies what was observed and approves every technical statement. The project manager confirms the follow-up.

## When to use it and when not to

Use it after a visit, once the notes are typed up and the photographs for the report have been chosen. Run it again when answers return or when the next visit adds notes.

Do not use it:

- to decide what a note means, how serious it is or whether work is acceptable. Those are the visiting engineer's decisions, and a photograph alone does not establish a concealed condition or that work is complete;
- to build the list of items for a closeout walk. That is punch list consolidation, a separate workflow template;
- to follow up concerns about safety raised on a walk. That is safety walk follow-up, a separate workflow template, and it belongs with the project's safety professional;
- to review a contractor's submittals. That is submittal register review, a separate workflow template.

## Roles

- **Runs it:** the visiting engineer, or the project manager working with them.
- **Verifies what was observed and approves every technical statement:** the visiting engineer, or your technical approver. Always a person.
- **Confirms the follow-up and who owns it:** the project manager, or your follow-up decider.
- **Owns each follow-up:** the role confirmed by the project manager.
- **Updates the observation register and sends anything on:** the people the project names, after those decisions.

## Inputs

The assistant works only from the files and notes the person supplies. It needs no connection to the project's systems and never asks for a password or a login code. It reads photograph file names and captions, not the pictures, and judges nothing from an image.

1. **The visit details,** typed: the project, the visit date, today's date, the scope of the visit in the visitor's words, the visiting engineer and who confirms follow-up.
2. **The field notes.** One row per note. Default column headers: `note_no`, `location`, `element`, `discipline`, `note_text`, `basis`, `reported_by`, `photo_ref`, `drawing_no`, `rev_in_hand`, `refers_to`. `basis` is exactly `observed` or `reported`, or blank, which is read as not stated. `reported_by` names who described the condition and is needed when `basis` is `reported`. `photo_ref`, `drawing_no`, `rev_in_hand`, `discipline` and `refers_to` may be blank. `refers_to` is an `obs_no` from the prior register, used when the person already knows the note touches that entry.
3. **The photograph set.** One row per approved or unapproved picture. Default column headers: `photo_ref`, `taken_date`, `location`, `caption`, `approved`. `approved` is exactly `yes` or `no`.
4. **The drawing register.** One row per drawing. Default column headers: `drawing_no`, `title`, `current_revision`, `revision_date`.
5. **The prior observation register.** One row per entry. Default column headers: `obs_no`, `location`, `element`, `observation`, `date_raised`, `register_status`, `owner`, `due_date`, `source_visit`. `register_status` is exactly one of `open`, `reported addressed` or `closed` (or your own status words). A blank `owner` or `due_date` is read as not supplied. An empty register is allowed.
6. **The owner list.** One row per discipline. Default column headers: `discipline`, `proposed_owner`. An empty list is allowed; then no owner is proposed from it.

**Column check.** Before any other work, compare each file's headers with the defaults, or with the project's own headers if your column headers are set. If a header is missing or named differently, stop. List the headers expected and the headers found, ask which column is which, and prepare nothing else. Never guess a column.

## The procedure

1. **Check the inputs.** Run the column check. Confirm today's date and the visit date. If a file is missing, say so and stop; an empty prior register or owner list is allowed. Stop and ask on: a `basis` that is not observed, reported or blank; an `approved` that is not yes or no; a `register_status` outside the allowed words; a date that can be read but does not exist, such as 31 November (a date that cannot be read at all is handled under Exceptions); two rows with the same `note_no`, `photo_ref`, `drawing_no` or `obs_no`; a `refers_to` that is not an `obs_no` on the register; a `photo_ref` or `drawing_no` on a note that is not on its list; a `basis` of reported with no `reported_by`.
2. **Check the data.** List under Data checks: each note with no basis stated, saying it is not read as observed; each photograph a note cites that is not approved, saying it is not attached; each note with a drawing but no revision in hand; each photograph whose location differs from its note's location; each discipline with no entry on the owner list; any location or element written several ways, saying the names are not merged; and the watch words (step 6). Say "None" for a check with nothing to report.
3. **Separate by basis.** Every note falls in exactly one group: directly observed, reported conditions, or basis not stated. A reported note prints who reported it. A note is never moved between groups by the assistant.
4. **Link to the prior register.** A note links to a register entry when its `refers_to` names it, or when its location and element both match the entry's, ignoring case, extra spaces and punctuation. If both apply, print "the note names it". If a note matches two entries by text, link neither and ask. A link by text is a pointer for the visiting engineer to confirm, not a finding. Linking is a pointer, not a comparison: print the note and the register wording side by side and say nothing about whether the condition is the same, better, worse or resolved. Show the entry's number, wording, date raised, status and owner. When the status is open and the due date is before today, add "register due date passed by [n] days" (calendar days). Do not add it for other statuses. When two notes link to the same entry, print the entry's details in full under each note; the summary counts each different entry once.
5. **Drawings.** For a note with a drawing, print the drawing number, the revision in hand and the current revision with its date, then one word: "matches", "differs" or "revision in hand not stated". Do not say which revision is right or what a change affects.
6. **Photographs and watch words.** Attach each approved photograph a note cites, with its reference, date and caption. A reference shows that a picture exists; it is not evidence that work is complete or that a hidden condition is present or absent. A note with no approved photograph says "none supplied" or "not approved, not attached". List every approved photograph that no note cites under Photographs not used. Search the note text for the watch words: concealed, behind, inside, buried, encased, below grade, complete, completed, finished, done, passed, compliant, safe, unsafe, hazard, danger, defect, failed, loose (your watch words). Match whole words, in any ordinary form (complete also catches completes and completing), and never part of a longer word (do not find "done" in "abandoned"; "unsafe" is a watch word of its own, not a hit for "safe"). Print each hit in quotation marks. Add one line saying a photograph does not show a concealed condition or that work is complete, that the visiting engineer decides what may be stated, and that anything that may concern safety goes to the project's safety professional.
7. **Propose follow-up owners.** For a linked note, the register's owner, with the basis "register owner". If there is none, or the note is not linked, the owner list's entry for the note's discipline, with the basis "owner list". If the register owner and the owner list name different roles, print "in conflict" with both roles and ask; the note counts as in conflict, not as proposed. If they name the same role, it is proposed, with the basis "register owner". If neither gives an owner, print "owner not proposed". These are proposals; the project manager confirms every one.
8. **Register entries with no note.** List each register entry that no note this visit links to, with its number, location, element, wording, status, owner and due date. Say nothing about why. The "register due date passed" line is added only for a linked entry. An open, past-due entry that no note links to gets the project manager's no-note question in step 10 without the days-passed line.
9. **Group and order.** Within each basis group, order by location alphabetically with notes that have no location last, then by note number. Group the questions by who answers. Within each reader's list, order by note number (a question about a register entry takes the lowest note number linked to it), then the question about unused photographs, then questions about register entries with no note, by entry number.
10. **Write the questions,** numbered separately for each reader. For the visiting engineer, one for each note that is reported, has no basis stated, has a watch word, has a revision that differs or is not stated, or cites an unapproved photograph, one question for the photograph set when an approved photograph is unused, and one for any note whose photograph location differs. For the project manager, one for each register entry that is open, past its due date and linked, one for each owner that is not proposed, one for each owner in conflict, and one for each register entry with no note. An owner in conflict on a note linked to a past-due entry is asked in that entry's question, which names both roles; an owner in conflict on a note whose linked entry is not past due has its own question. Two notes linked to the same entry share that entry's question. A note with several reasons shares one question. Each question states the facts first and then asks what the reader wants done, which may include what a technical statement may say. It recommends nothing and offers no wording for a message.
11. **Return the report** to the person who ran it, for the visiting engineer and the project manager. A person updates the register, assigns the work and contacts anyone.

## Exceptions and stop conditions

- **A column header is missing or named differently:** stop; list expected and found headers; ask.
- **A basis, status or approval word that is not allowed, a date that can be read but does not exist, a duplicate number, a reference not on its list or a reported note with no `reported_by`:** stop and ask.
- **A note matches two register entries by text:** link neither; ask.
- **A date that cannot be read as a date at all, such as "next week":** treat it as not supplied and show the words. This differs from a date that can be read but does not exist, which stops the work as above.
- **A file is missing:** say so and stop. An empty prior register or owner list is allowed.
- **Asked what a note means, whether a condition is serious, acceptable, safe, compliant or complete, to judge a photograph, to say that a register entry is resolved, or to choose a revision:** decline and name the visiting engineer.
- **Asked to assign an owner, close or reopen a register entry, or send the report on:** decline and name the project manager or the role that does it.
- **The files contain a password, a login code or bank details:** do not repeat them; tell the person to remove them from the source.

## Output format

```
SITE OBSERVATION REPORT: [project], visit of [weekday date]

For: [visiting engineer role], to verify, and [project manager role], to confirm follow-up. Prepared [weekday date] from: visit details, field notes ([n] rows), photograph set ([n] rows), drawing register ([n] rows), prior observation register ([n] rows), owner list ([n] rows).
Column check: [all headers matched].
Visit scope as typed: "[words]" Anything outside it is not covered by this report.
Summary: [n] field notes. Directly observed [n], reported [n], basis not stated [n]. Linked to the prior register [n] notes, to [n] earlier entries. Earlier entries with no note this visit [n]. Photographs: [n] in the set, [n] approved, [n] attached, [n] not approved and not attached, [n] approved and not cited by any note; notes with no photograph attached [n]. Drawings: [n] notes cite a drawing; revision in hand matches the current revision for [n], differs for [n], not stated for [n]; [n] cite no drawing. Proposed follow-up owners [n], not proposed [n], in conflict [n]. Questions: [n] for the visiting engineer, [n] for the project manager.

Data checks
- [Each check, with what was done / None.]

Directly observed: [n]
- [Note number] [element] ([discipline / discipline not stated]), [location]. OBSERVED. Note: "[words]". Prior register: [obs no], "[register words]", raised [weekday date], status [status], owner [role / not supplied], [register due date passed by [n] days (due [weekday date]) / due [weekday date] / no due date recorded]; linked because [the note names it / of the same location and element] / no earlier entry linked. Drawing: [number], revision in hand [rev], current revision [rev] (dated [weekday date]): [matches / differs / revision in hand not stated] / none cited. Photograph: [reference] (approved, taken [weekday date], "[caption]") / [reference] not approved, not attached / none supplied. Watch word: "[word]" / none. Proposed follow-up owner: [role] ([register owner / owner list]) / in conflict: register owner [role], owner list [role] / owner not proposed. Technical statement: awaiting the visiting engineer's verification.

Reported conditions: [n]
- [Same fields, with REPORTED by [name or role] in place of OBSERVED.] / None.

Basis not stated: [n]
- [Same fields, with BASIS NOT STATED in place of OBSERVED.] / None.

Earlier entries with no note this visit: [n]
- [Obs no], [location], [element], "[register words]", status [status], owner [role / not supplied], register due date [weekday date / not supplied]. / None.

Photographs not used: [n]
- [Reference], [location], "[caption]", approved, taken [weekday date]. No note cites it. / None.

Questions for the visiting engineer
1. [Note or photograph]. [Facts.] [Question.] / None.

Questions for the project manager
1. [Register entry or note]. [Facts.] [Question.] / None.

Every technical statement is the field note's own wording until the [visiting engineer role] approves it. The [project manager role] confirms every follow-up owner, including those proposed without a question.

Draft for the [visiting engineer role]'s verification and the [project manager role]'s confirmation. No condition has been assessed, and no drawing, register entry or owner has been changed. Nothing has been sent.
```

Write [weekday date] like Monday 9 November 2026. Every item the instructions require has a place above. Where a section has nothing in it, print "None." under its heading.

## Reviewer checklist

1. Every note appears once, in the group its basis says, with the wording as written. (Visiting engineer)
2. No note marked reported or with no basis has been listed as observed. (Visiting engineer)
3. Every register link is by the named entry or by an exact location and element, and nothing says the condition is the same, better, worse or resolved. (Project manager)
4. Each drawing line shows the revision in hand and the current one, and none says which is right. (Visiting engineer)
5. Photographs attached are approved, belong to the note that cites them, and none is described beyond its caption. (Visiting engineer)
6. Each proposed owner comes from the register or the owner list, and conflicts and gaps are asked about. (Project manager)
7. The counts in the summary agree with the lists. (Project manager)
8. No sentence assesses a condition, compliance or safety, and nothing has been sent, assigned, closed or changed. (Visiting engineer)

## Acceptance tests

Proposed tests. They have not been run as a set; the trial in `public/trial.md` ran the invented example only.

1. **Normal visit.** Several observed notes, one reported, one linked entry. Expected: three groups, side-by-side register wording, owners proposed, counts that agree.
2. **No basis stated.** A blank `basis`. Expected: listed under Basis not stated and in Data checks, with a question; never under observed.
3. **Reported condition.** `basis` of reported with `reported_by`. Expected: printed with who reported it, in the reported group.
4. **Link by name and by text.** One note with `refers_to`, one with matching location and element. Expected: "the note names it" and "of the same location and element".
5. **Two text matches.** A note whose location and element match two register entries. Expected: links neither, asks.
6. **Past due.** An open entry due before today, and an entry reported addressed with an old due date. Expected: days passed shown for the first only.
7. **Revision differs.** `rev_in_hand` B, current C. Expected: "differs", a question, no statement on which applies.
8. **Revision not stated.** Blank `rev_in_hand`. Expected: "revision in hand not stated", a question.
9. **Photograph not approved.** A note cites a photograph marked `no`. Expected: not attached, listed in Data checks, a question.
10. **Photograph unused.** An approved photograph no note cites. Expected: listed under Photographs not used and one question.
11. **Watch word.** A note saying work is "complete" and one saying "inside" a wall, and one saying a bracket is "loose". Expected: each quoted with the photograph line and the safety professional line, and a question each. A note saying "abandoned" or "unsafe" gives no hit for "done" or "safe" ("unsafe" is its own hit).
12. **Owner in conflict.** Register owner differs from the owner list. Expected: printed as in conflict with both roles, counted as in conflict and not as proposed, and asked in the question about the linked entry when it is past due, otherwise in its own question.
13. **Register entry with no note.** Expected: listed under Earlier entries with no note this visit and a question for the project manager.
14. **Renamed column.** `note_text` arrives as `comment`. Expected: stops, lists expected and found headers and asks.
15. **Asked to assess.** "Is the crack serious?" Expected: declines and names the visiting engineer.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare a site observation report for a visiting engineer and a
project manager from the visit details, field notes, photograph set,
drawing register, prior observation register and owner list they
supply. You prepare; people decide. You never assess a condition,
say that anything is complete, compliant or safe, interpret or judge a
photograph, choose a drawing revision, say that a register entry is
resolved, assign work, close or reopen a register entry, contact
anyone, send anything or change any record. The visiting engineer
verifies what was observed and approves every technical statement; the
project manager confirms follow-up. You never ask for a password or a
login code and need no system access. You read photograph file names and
captions only.

If a file is missing, say so and stop; an empty prior register or owner
list is allowed. First compare each file's column headers with the
defaults. Field notes: note_no, location, element, discipline,
note_text, basis, reported_by, photo_ref, drawing_no, rev_in_hand,
refers_to. Photograph set: photo_ref, taken_date, location, caption,
approved. Drawing register: drawing_no, title, current_revision,
revision_date. Prior register: obs_no, location, element, observation,
date_raised, register_status, owner, due_date, source_visit. Owner
list: discipline, proposed_owner. If a header is missing or different,
stop, list expected and found headers and ask; never guess a column.
Stop and ask on a basis other than observed, reported or blank; an
approved other than yes or no; a register_status other than open,
reported addressed or closed; a date that exists in form but not on the
calendar; a duplicate number; a reference not on its list; a reported
note with no reported_by. A date that cannot be read at all, such as
"next week", is treated as not supplied, with its words shown.

1. Data checks: notes with no basis (not read as observed); cited
   photographs not approved (not attached); a drawing with no revision
   in hand; photograph location different from the note's; disciplines
   missing from the owner list; names written several ways (do not
   merge them); watch words. Say "None" where there is nothing.
2. Put each note in one group: directly observed, reported conditions
   (print who reported it) or basis not stated. Never move a note
   between groups.
3. Link a note to a register entry when refers_to names it or when
   location and element both match, ignoring case, spaces and
   punctuation; if both, say the note names it. If two entries match
   by text, link neither and ask. A link by text is a pointer for the
   visiting engineer to confirm. Two notes linked to one entry each get
   its details in full. Print the note and the register
   wording side by side with number, date raised, status and owner. Say
   nothing about whether the condition is the same, better, worse or
   resolved. If the status is open and the due date is before today, add
   "register due date passed by [n] days" in calendar days.
4. Drawing: number, revision in hand, current revision with date, then
   matches, differs or revision in hand not stated. Do not say which is
   right.
5. Photographs: attach only approved ones the note cites, with
   reference, date and caption. A photograph does not show a concealed
   condition or that work is complete. List approved photographs no note
   cites. Watch words: concealed, behind, inside, buried, encased,
   below grade, complete, completed, finished, done, passed, compliant,
   safe, unsafe, hazard, danger, defect, failed, loose. Match whole
   words in any ordinary form, never part of a longer word. Quote each
   hit and add one line that the visiting engineer decides what may be
   stated and that anything that may concern safety goes to the
   project's safety professional.
6. Proposed owner: the register owner for a linked note; otherwise the
   owner list entry for the discipline; if the two name the same role,
   propose it; if they differ, print "in conflict" with both roles and
   ask, and count the note as in conflict, not as proposed; if none,
   "owner not proposed".
7. List register entries no note links to, with their details and no
   explanation.
8. Order each group by location alphabetically (none last), then note
   number. Write questions numbered separately for the visiting
   engineer (reported, no basis, watch word, revision differs or not
   stated, unapproved photograph, unused approved photograph, photograph
   location differs) and for the project manager (linked open entry past
   due, owner not proposed, owner in conflict, register entry with no
   note). A note with several reasons shares one question. An owner in
   conflict on a note linked to a past-due entry is asked in that
   entry's question, naming both roles; otherwise it has its own
   question. Two notes linked to one entry share that entry's question.
   Order each reader's questions by note number (an entry takes its
   lowest linked note number), then the unused-photograph question, then
   entries with no note by entry number. State facts
   first, then ask what the reader wants done. Recommend nothing and
   draft no message.
9. Use the output format exactly. Write dates as a weekday and date,
   like Monday 9 November 2026. Write "None." under any empty section.
   Every technical statement is the note's own wording until the
   visiting engineer approves it. End with the draft line saying no
   condition has been assessed and nothing has been changed or sent.

If asked what a note means, whether a condition is serious, acceptable,
safe, compliant or complete, to judge a photograph, to say a register
entry is resolved or to choose a revision, decline and name the visiting
engineer. If asked to assign an owner, close or reopen an entry or send
the report, decline and name the project manager or the role that does
it. If the files contain a password, a login code or bank details, do
not repeat them; tell the user to remove them. Recheck every link,
count and date before returning the report.
```

## What to customize

- Your status words for the register, and your column headers if your exports differ.
- Your watch words: the words in your notes that call for a closer look.
- Your technical approver and your follow-up decider, if they are not the visiting engineer and the project manager.
- The owner list, one proposed role for each discipline.
- How locations and elements are named, so links by text match. Name elements finely ("anchor bolts", "grout pad" rather than "column base"), or text links will join unlike things; the visiting engineer confirms each link by text before relying on it.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.1, 10 November 2026. After an independent review: how an owner in conflict is printed and counted, when a conflict shares a question with a past-due register entry, the order of questions, whole-word watch words (with "loose" added and a pointer to the project's safety professional), how a register entry shared by two notes is handled, and plain names for the related workflow templates. Run again on the invented example after these changes.
- 0.1.0, 10 November 2026. Written by Fully Powered AI from its own published map of the work. Editorially reviewed. It was tried on its invented example in Claude on 10 November 2026; the record is published with it (`public/trial.md`). The edits above were made after that first run, and the edited version was run again on the same example; both runs are in the record. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
