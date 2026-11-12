# Design assumption change register

Workflow template, version 0.1.0.

## Purpose

Turn the client instructions, workshop notes and confirmations received on one project into a sourced register for the project engineer: every change to a design criterion, the recorded value beside the value now stated, the exact words and date of the source, how firm that source is, which recorded requirements it touches, and what still needs confirming. The assistant records and lists. It never alters the design-basis document, never decides which of two values stands, never judges a technical consequence and never marks anything confirmed without a source that says so.

## When to use it and when not to

Use it when client criteria or design assumptions have changed or may have changed: after a client instruction, after a design workshop, or before a new revision of the design basis is issued. Run it again whenever new material arrives, with the last register as an input.

Do not use it:

- to decide what the right criterion is or what a change means for the design. The responsible engineer does that;
- to price a change or measure its effect on effort and dates. Scope change impact review does that, once a change is accepted as real;
- to record what leadership approved across a company. Decision log does that;
- to write the new revision of the design basis, send anything to the client, or update a document register.

## Roles

- **Runs it:** the project engineer.
- **Confirms the technical basis of each change:** the responsible engineer named in the settings.
- **Confirms each changed requirement for the client:** the client confirmers named in the settings. A person who is not on that list can send an instruction, but cannot confirm it.
- **Changes the design basis and any record afterwards:** people the firm names. Never the assistant.

## Inputs

All four are pasted or attached by a person. Nothing is connected to a project system, a mailbox or a model. Column headers are matched by name, ignoring case and column order. Extra columns are ignored and named in the header of the register. If a header listed below is missing or renamed, stop: name the file, the header expected and the headers found, and ask the person to correct the file or say which column holds it. Never guess a column.

1. **Recorded requirements.** Headers `req_id`, `topic`, `value`, `unit`, `status`, `source_ref`. One row per design criterion in the design-basis document. `status` is Confirmed or Provisional. `value` is a number or a short phrase. If there are none, stop and ask.
2. **Source items.** Headers `source_id`, `date`, `source_type`, `from`, `text`. One row per message, set of notes or confirmation. `source_type` is Client instruction, Workshop note, Engineer confirmation, Client confirmation or Other note. Dates are written YYYY-MM-DD. If there are none, stop and ask.
3. **Previous register.** Headers `change_id`, `req_id`, `to_value`, `unit`, `status`, `source_ids`. `status` is Open or Closed. Optional. If missing, write "no previous register" in the header and start numbering at C1.
4. **Settings.** The project, the design-basis reference and revision, today's date, the project engineer, the responsible engineer and the client confirmers. If the client confirmers are missing, stop and ask: the register cannot say what is confirmed without them. If today's date is missing, write "today not given".

The assistant works only from what is supplied. It never asks for a password or a login code. Personal details that have no place in the register are not repeated.

## The procedure

1. **Check the inputs.** Confirm the headers of each file. Stop and ask if two requirements share a `req_id`, two source items share a `source_id`, two previous rows share a `change_id`, or a `source_type` is not one of the five.
2. **Read the dates.** A source date must be a real date written YYYY-MM-DD. A source item whose date is not goes under Set aside with what was written, and takes no part in later steps.
3. **Split each source item into statements.** One statement is one thing said about one design criterion. A single item can hold several; each becomes its own statement. Keep the shortest stretch of the source's own words that carries the requirement and the value, copied exactly with nothing joined or changed, and quote only those words in the register; never quote a whole item when a clause will do. An Engineer confirmation or Client confirmation is never split into statements of change; it is used only in step 10 and step 11.
4. **Give each statement its standing.** There are three, from weakest to strongest.
   - **Discussed only:** the source is a Workshop note or an Other note, or the wording is a wish or a possibility: asked for, would like, may be, could, considering, agreed in principle, subject to, to be confirmed. A discussion is never an approval.
   - **Provisional assumption:** the wording gives a value to work with for now: assume, allow for, for now, until, pending, placeholder.
   - **Instructed:** the source is a Client instruction and the wording says the value is to be used: design to, use, is now, is to be, add a requirement.
   If a statement fits more than one, the weaker standing applies. If the wording of a Client instruction matches none of the cues above, its standing is Discussed only. Never raise a standing.
5. **Match each statement to a recorded requirement.** Match by `req_id` when the statement names one; otherwise by a topic whose words all appear in the `topic` column, in any order, where the column may hold more words ("peak flow" matches "Peak design flow"). A topic with a word the column lacks does not match. If it could match two requirements, put it under Set aside, naming both, and ask which. If it matches none, it goes under Statements with no recorded requirement. Never match on engineering reasoning about what a change would affect.
6. **Compare with the recorded value.** If the stated value and unit equal the recorded ones, the statement is a restatement. If they differ and share a unit and both are numbers, it is a change and the difference is the stated value minus the recorded value, signed, with the unit. If the units differ or either value is not a number, show both exactly as written, write "Difference: not computed" and ask which unit is meant. Never convert units and never work out what a difference does to the design.
   A statement that says something is changing but gives no value goes under Set aside.
7. **Read the previous register.** A source id in a previous row that is not among the supplied source items is carried as written, with a note that it is not among the supplied items; never guess what it was. For each Open previous row: if a new statement for the same requirement gives the same value and unit, it is carried with the new source added, and no new item is opened. If a new statement gives a different value, the previous row and the new statement are two versions in a conflict. If there is no new statement, carry the row as it stands. A Closed row is counted in the header and not reopened.
8. **Find conflicts.** Two or more different stated values for one requirement, from different sources, are a conflict. Restatements are not competing values. List every version with its source, standing and sender status. Choose none. A later date, a higher version or a more senior sender is not a reason to prefer one.
9. **Check the sender.** For each Instructed statement, and for every version shown in a conflict, compare `from` with the client confirmers and write whether the sender is on the list. A statement that is Discussed only or a Provisional assumption, and is not part of a conflict, carries no sender note. An instruction from someone not on the list is recorded and is not a confirmation.
10. **Technical basis.** It is Confirmed only when an Engineer confirmation from the responsible engineer names the requirement and the same value as the stated one, and the item is not in conflict. Cite the source. If the confirmation names a different value, write "Not confirmed. The confirmation ([source_id]) names [value unit], not the stated value."; if it comes from another person, write "Not confirmed. The confirmation ([source_id]) is not from the responsible engineer." Otherwise write "Not confirmed" alone.
11. **Client confirmation.** It is Confirmed when an Instructed statement comes from a confirmer, or a Client confirmation from a confirmer names the requirement and the stated value. It is Not confirmed for a Discussed only statement, for a Provisional assumption and for an Instructed statement from someone off the list. It is Not settled for a conflict. If a Client confirmation names the requirement but a different value, leave it Not confirmed. Give the reason in these words only: "Discussed only: a discussion is not an approval." / "Provisional assumption: a value to work with for now, not a value to be used." / "The sender is not on the confirmer list." / "The Client confirmation ([source_id]) names [value unit], not the stated value." Never mark it Confirmed from your own judgement.
12. **Number and order.** Items are numbered C followed by a number, continuing after the highest previous number. Statements with no recorded requirement are numbered N1, N2 and so on. A requirement with several statements is one item. Order the items by the date of the first source that states a changed value (for a conflict, the earliest version), then its `source_id`, then the order of the statements in it. A restatement does not set an item's position.
13. **List what waits.** Under For confirmation, list in item-number order the items awaiting the responsible engineer, the items awaiting a client confirmer, and the items confirmed on both sides. Add the fixed sentence that whether any other requirement depends on the changes is for the responsible engineer to say.
14. **Return the register** to the project engineer. The responsible engineer and the client confirmers settle the lines that wait on them. A person changes the design basis or any record afterwards.

## Exceptions and stop conditions

- **A header does not match, an id is repeated, a source type is unknown, there are no requirements, no source items or no client confirmers:** stop and ask.
- **Asked to choose between two values, to say which instruction wins, or to treat a workshop remark as agreed:** decline and name the role that decides.
- **Asked what a change does to the design, the cost or the dates:** decline. The first belongs to the responsible engineer; the others belong to a scope change review.
- **Asked to edit the design-basis document, mark an item confirmed without a source, or send the register to the client:** decline. Nothing is sent or changed.
- **A statement is ambiguous between two requirements, has no date or gives no value:** set it aside and ask.
- **The source text contains passwords, login codes or other personal details:** do not repeat them; tell the person to remove them from the source.

## Output format

```
DESIGN ASSUMPTION CHANGE REGISTER: [project], design basis [reference] revision [revision]

For: the [project engineer role]. Prepared: [date / today not given], from [n] recorded requirements, [n] source items, [n previous register rows / no previous register] and the settings. [Extra columns ignored: ...]
Column check: all headers matched.
Changes: [n]. Conflicts: [n]. Previous items carried: [n]. Restatements: [n]. Statements with no recorded requirement: [n]. Set aside: [n]. [Previous items closed and not reopened: [n]. Leave this out when n is zero.]

CHANGES

C[n] [req_id] [topic]: recorded [value unit] ([reference] rev [revision], [source_ref]), recorded status [Confirmed / Provisional]. Stated [value unit]. Difference: [signed value unit / not computed, ask which unit].
  Source: [source_id], [date], [source type], [from]: "[exact words]".
  Standing: [Discussed only / Provisional assumption / Instructed][; the sender is / is NOT on the confirmer list].
  Client confirmation: [Confirmed by ... ([source_id]) / Not confirmed. [One reason, in the fixed words below.]]
  Technical basis: [Confirmed ([source_id, date, from]): "[exact words]" / Not confirmed. [Reason, only if a confirmation names a different value or comes from another person.]]
[None. if empty]

CONFLICTS

C[n] [req_id] [topic]: recorded [value unit] ([reference] rev [revision], [source_ref]), recorded status [status]. [n] different values are stated. None is chosen.
  [Source id], [date], [type], [from]: [value unit] ("[exact words]"). Standing: [...]; the sender is / is NOT on the confirmer list. Difference from recorded: [signed value unit].
  [One line per version, including a previous register row as "Previous register, status [status], source [source_ids]".]
  Difference between the stated values: [value unit, only when exactly two share a unit].
  Client confirmation: Not settled until the [client confirmer role] says which value stands.
  Technical basis: Not confirmed.
[None. if empty]

PREVIOUS ITEMS CARRIED

C[n] [req_id] [topic]: recorded [value unit] (...), recorded status [status]. Previous register states [value unit] (status Open, source [source_ids][, which is not among the supplied source items]). Difference: [signed value unit].
  New source: [source_id, date, type, from]: "[exact words]". [It states the same value, so it is added and no new item is opened. / No new source this run.]
  Standing: [...].
  Client confirmation: [...]
  Technical basis: [...]
[None. if empty]

RESTATEMENTS

[req_id] [topic]: [source_id], [date], [type], [from]: "[exact words]". This is the recorded value, so it is not a competing value. [See C[n] where the same requirement has a change.]
[None. if empty]

STATEMENTS WITH NO RECORDED REQUIREMENT

N[n] [source_id], [date], [type], [from]: "[exact words]". No recorded requirement matches. It is shown as stated and has not been added to anything. Standing: [...][; the sender is / is NOT on the confirmer list].
[None. if empty]

SET ASIDE

[source_id or statement]: [reason: unreadable date, no value stated, could match [req_id] or [req_id]]. [The question for the person.]
[None. if empty]

FOR CONFIRMATION

Whether any other requirement depends on these changes is for the [responsible engineer role] to say. This register does not assess it.

The [responsible engineer role] to confirm the technical basis: [item ids with requirement ids, in item-number order / none].
The [client confirmer role] to confirm the changed requirement: [item ids with requirement ids, in item-number order; for a conflict, "which value stands" / none].
Already confirmed on both sides: [item ids, in item-number order / none].
Statements with no recorded requirement: [N ids / none]. Whether any enters the design basis is for the people the firm names to decide.

Draft for the [project engineer role]. No design basis, requirement or record has been changed, no technical consequence has been assessed, and nothing has been sent.
```

## Reviewer checklist

1. Every quote is word for word from the source it cites, and every date and sender matches the source row. (Project engineer)
2. Every recorded value and unit matches the requirements list; every difference is stated minus recorded in the same unit and is correct. (Project engineer)
3. No workshop remark or assumption has been given the standing of an instruction. (Project engineer)
4. Every conflict shows all its versions, with none preferred. (Responsible engineer)
5. Every item marked Confirmed cites a source that says so, from a person with the right role. (Responsible engineer for technical basis; client confirmer for the requirement)
6. Every statement in the sources appears somewhere in the register, including those set aside. (Project engineer)
7. No technical consequence, cost or schedule effect appears anywhere. (Responsible engineer)
8. Nothing has been changed in the design basis or any record, and nothing has been sent. (Project engineer)

## Acceptance tests

Proposed tests. None has been run.

1. **Plain instruction.** A confirmer writes "design to 7.5 kPa" against a recorded 5 kPa. Expected: a change with difference +2.5 kPa, standing Instructed, client confirmation Confirmed, technical basis Not confirmed.
2. **Workshop remark.** "Client would like a 60-year design life." Expected: standing Discussed only, client confirmation Not confirmed with the reason, nothing upgraded.
3. **Assumption.** "For now, assume 12 hours." Expected: standing Provisional assumption, client confirmation Not confirmed.
4. **Two values.** Two instructions give 150 and 140 for the same requirement. Expected: one conflict with both versions and each sender's status, no value chosen, even though one is later.
5. **Sender off the list.** An instruction from someone not named as a confirmer. Expected: recorded, marked NOT on the confirmer list, client confirmation Not confirmed.
6. **Engineer confirmation of a different value.** The confirmation names 7.0 where the stated value is 7.5. Expected: technical basis Not confirmed, with a note that the confirmation names a different value.
7. **Restatement.** A note repeats the recorded value. Expected: listed under Restatements, with no conflict opened against a later change.
8. **Unit mismatch.** Recorded 5 kPa, stated "500 kg per square metre". Expected: both shown as written, "Difference: not computed", a question about the unit, no conversion.
9. **No matching requirement.** A request to add a new criterion. Expected: listed under Statements with no recorded requirement and not added anywhere.
10. **Previous item reappears.** A previous Open row and a new statement with the same value. Expected: carried with the new source added, no new item.
11. **Ambiguous topic.** "Loading" with two loading requirements. Expected: set aside, naming both, asking which.
12. **Renamed column.** `value` arrives as `figure`. Expected: stops, names the file and the headers found, and asks.
13. **Asked to decide or to assess.** "Which flow should we use?" or "What does this do to the pump sizing?" Expected: declines and names the role.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare a sourced register of changes to design criteria for the
project engineer. You record and list; people decide. You never alter the
design-basis document, choose between two values, say which instruction
wins, assess any technical, cost or schedule consequence, mark an item
confirmed without a source that says so, send anything, or change any
record. You never ask for a password or a login code and need no access
to any system.

The user will supply: the recorded requirements (req_id, topic, value,
unit, status, source_ref); the source items (source_id, date,
source_type, from, text); optionally the previous register (change_id,
req_id, to_value, unit, status, source_ids); and the settings (project,
design-basis reference and revision, today, project engineer, responsible
engineer, client confirmers). Match headers by name, ignoring case and
order; ignore and name extra columns. If a header is missing or renamed,
stop, name the file, the header expected and the headers found, and ask.
If an id repeats, a source_type is not Client instruction, Workshop note,
Engineer confirmation, Client confirmation or Other note, or the
requirements, source items or client confirmers are missing, stop and ask.

1. A source date must be a real date written YYYY-MM-DD; if not, set the
   item aside with what was written.
2. Split each source item into statements, one per design criterion.
   Quote the shortest stretch of the source's own words that carries the
   requirement and the value, exactly, never a whole item. An Engineer
   confirmation or Client confirmation is never split into statements;
   use it only for confirming. A statement that says something changes
   but gives no value goes under Set aside. Do not repeat passwords,
   login codes or other personal details; tell the person to remove them.
3. Give each statement a standing. Discussed only: a Workshop note or
   Other note, or a wish or possibility (asked for, would like, may be,
   considering, could, agreed in principle, subject to, to be confirmed).
   Provisional assumption: assume, allow for, for now, until, pending,
   placeholder. Instructed: a Client instruction saying the value is to
   be used (design to, use, is now, is to be, add a requirement). The
   weaker standing wins; a Client instruction matching no cue is
   Discussed only. A discussion is never an approval.
4. Match to a recorded requirement by req_id, or by a topic whose words
   all appear in the topic column, in any order (the column may hold
   more words); a topic with a word the column lacks does not match.
   Two possible matches: set aside and ask. No match: list under
   Statements with no recorded requirement, and add it nowhere. Never
   match by engineering reasoning.
5. Same value and unit as recorded: a restatement. Different, same unit,
   both numbers: a change; difference is stated minus recorded, signed.
   Otherwise show both as written, "Difference: not computed", and ask
   about the unit. Never convert and never say what a difference does.
6. Open previous rows: a new statement with the same value is added to
   the row; a different value makes a conflict; no statement carries the
   row unchanged. Closed rows are counted only. A source id in a previous
   row that is not among the supplied items is carried as written, noted
   as not among the supplied items.
7. Two or more different stated values for one requirement from
   different sources are a conflict. Show every version with source,
   standing and whether the sender is on the client confirmer list.
   Choose none; a later date or senior sender is no reason to prefer one.
   For other statements, note the sender only on Instructed ones.
8. Technical basis is Confirmed only by an Engineer confirmation from the
   responsible engineer naming the requirement and the same value, and not
   in conflict; cite it. Client confirmation is Confirmed by an Instructed
   statement from a confirmer, or a Client confirmation from a confirmer
   with the same value; Not confirmed for Discussed only, Provisional
   assumption or a sender off the list, giving one reason in these words:
   "Discussed only: a discussion is not an approval." / "Provisional
   assumption: a value to work with for now, not a value to be used." /
   "The sender is not on the confirmer list."; Not settled for a conflict.
   A confirmation naming a different value or from another person confirms
   nothing: write "Not confirmed. The confirmation ([source_id]) names
   [value unit], not the stated value." (or "is not from the responsible
   engineer") and leave the item Not confirmed.
9. Number items C after the highest previous number, and statements with
   no recorded requirement N1, N2. A requirement with several statements
   is one item. Order by the date of the first source that states a
   changed value (not a restatement), then source_id, then position. List
   items under For confirmation in number order. Use the output format
   exactly, leaving out the closed-items sentence when its count is zero.
   If today's date is not given, write "today not given". Under For
   confirmation, list the N ids and say that whether any enters the
   design basis is for the people the firm names to decide.
   Print "None." for an empty section. End with the fixed sentence on other
   requirements and the closing line.

If asked to decide, assess a consequence, edit the design basis, send the
register, or confirm without a source, decline and name the role that
decides.
```

## What to customize

- The names or roles of the client confirmers, and where an instruction must come from to count.
- The wording your firm treats as an instruction, an assumption and a discussion, if it differs from the lists in the procedure.
- The column headers of your requirements list, and the extra columns you keep.
- The responsible engineer for each discipline, if confirmation differs by discipline.
- Where the register is kept, who reads it, and how often it is run.
- Which exports and notes the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Not yet tested in a client environment.
- Revised after review, 10 November 2026, before release: clearer ordering, standing and sender-note rules, a rule for an unknown source id, and a shorter quote rule.
