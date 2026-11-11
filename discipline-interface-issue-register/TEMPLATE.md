# Discipline interface issue register

Capability template, version 0.1.0.

## Purpose

Turn the conflicts a coordination meeting exposed into one register. Each issue is taken from the minutes, linked to the clash-export rows and model revisions that touch it, tied to the lead who owns each system, and given the decision still needed, written as a question. The register records the direction the meeting reached, if any, as recorded and not confirmed. The assistant prepares; it never resolves a clash, proposes a design change, opens or checks a model, assigns an owner, closes an issue or sends anything. The discipline leads resolve the conflicts and approve changes; the coordinator confirms who owns what.

## When to use it and when not to

Use it after a coordination meeting, once the minutes are written and the latest clash export and model revision index are to hand. Run it again after the next meeting with the previous register, so earlier issues carry forward.

Do not use it:

- to find clashes. It reads an export a modelling tool has already produced; it detects nothing and checks no model;
- to decide which discipline should move, or to suggest how a conflict could be resolved. That is the leads' work;
- to look ahead at what could hold up planned site activity, which is three-week look-ahead constraint review;
- to report a project to its sponsor, which is project status report;
- to record changes to client criteria and design assumptions against the design basis, which is design assumption change register;
- when there are no minutes. Without them there is no record of what was said, and the assistant stops.

## Roles

- **Runs it:** the design coordinator.
- **Resolves each technical conflict and approves any design change:** the discipline lead who owns the system to be changed, with the other leads involved.
- **Confirms recorded ownership, and who takes an unowned issue forward:** the design coordinator.
- **Confirms a recorded direction in writing:** the lead the minutes name for it.
- **Closes an issue:** the coordinator, in the firm's own record, after the lead's written confirmation. The register never says closed.

## Inputs

The person supplies these as files or pasted text. The assistant works from them alone, needs no connection to a modelling tool or document system, and never asks for a password, a login code or any other secret.

1. **Settings.** Project name; the coordinator's role; the meeting date; today's date; the next meeting date. If the project, the meeting date or today's date is missing, stop and ask. If the next meeting date is missing, write "not stated".
2. **Minutes.** The meeting's numbered items. If the items are not numbered, number them in order and say so in the header. If there are no minutes, stop.
3. **Clash export.** Default headings: `clash_id, status, discipline_a, system_a, model_a, revision_a, discipline_b, system_b, model_b, revision_b, zone, found_on`. Dates are year-month-day. If not supplied, write "not supplied" and continue: every issue then has no export rows.
4. **Model revision index.** Default headings: `model_id, discipline, current_revision, revision_date`. One row per model. If not supplied, write "not supplied": every model reference is then "not in index".
5. **Responsibilities table.** Default headings: `system, owning_discipline, owner_role`. One row per system. If not supplied, write "not supplied": every system is then "owner not assigned".
6. **Discipline sketches,** optional. Default headings: `sketch_id, discipline, dated, subject, cites`. Cites is an issue or clash number, or a dash for none. If not supplied, write "not supplied".
7. **Previous register,** optional, in this capability's output format. If not supplied, write "none".

If a file's headings do not match the defaults, in any order, stop and ask which column is which. Never guess a column. If a date could be read two ways, stop and ask. If two rows share a clash_id, a model_id or a system, stop and ask which is right.

## The procedure

1. **Check the inputs.** Confirm the headings, count the minutes items, export rows, models, systems and sketches, and note the earliest and latest found_on in the export. Stop on any mismatch under Inputs.
2. **List the issues from the minutes.** One issue is one conflict between named systems of two or more disciplines. Number issues I-01, I-02 and so on in the order of the minutes. A minutes item that states two conflicts becomes two issues with the same minutes reference. The same conflict stated in two items becomes one issue, naming both. Write the conflict in one sentence, using the minutes' words, and take the location as the minutes state it. An item that is not a conflict between disciplines, such as a conflict inside one discipline, an attendance line or a date, is not entered; list its number under "Minutes items not entered" with two or three words saying why. Never add an issue the minutes do not state.
3. **Link the export rows.** A row is linked as **stated** when the minutes item cites its clash_id. If the minutes item cites no number, a row is linked as **possible** only when the row's zone and at least one of its systems are both named in the item, in the same words or words close to them (close words apply to linking an export row only; table names follow step 4). Possible links are shown as such and flagged. Never link by anything else. If the minutes cite a clash_id that is not in the export, write "cited, not in the export" and flag it. A row linked to two issues is shown under both.
4. **Name the systems and their leads.** Take the two systems from the linked row; for a possible link, take them from the row too and say so. With no linked row, take the systems from the minutes' own words. Look each system up in the responsibilities table by name, ignoring capital letters. The lead is the owner_role in that row. A table name found word for word inside the minutes' words counts as a match ("the roof plant platform edge" matches "Roof plant platform"). A system whose name is not in the table, or is only close to a name in it without containing it word for word, is written with the minutes' words, "discipline not stated" in the discipline place (unless a linked row gives it) and "owner not assigned"; the assistant does not match it for the coordinator.
5. **Check the model references.** For each linked row, take the model and revision cited on each side. Add any revision the minutes cite for a model. Compare each with the index and write one of: current (the cited revision is the index's current_revision), outdated (it is not, with the current revision and its date), or not in index (the model is absent from it). A revision the minutes cite without a model ID attaches to the model of the discipline the minutes name when exactly one such model appears in the linked rows; otherwise write "model not named" beside the revision and compare nothing. Where the same model is cited at two revisions, show both and give each its own verdict. Where none is cited, write "none cited". An outdated or not-in-index reference is flagged "revision". The assistant opens no model and judges nothing about the geometry; it only compares the labels.
6. **Record the lead and the direction.** "Lead named in the minutes" is a role the minutes ask to act on this item, in the minutes' words; write "none" if there is none and flag "no lead named". If the named role is not the table's owner_role for either system, flag "lead differs from table". "Direction in the minutes" is what the minutes say the meeting agreed, in the minutes' words, or "none". An action alone, such as "to look at", is not a direction. A proposal by one lead together with another lead's recorded agreement is a direction; a proposal alone, or a refusal, is not. Record the leads' opinions and requests as the minutes state them, attributed, on the Direction line (for example, "each asked the other to adjust").
7. **Write the decision needed.** One or two sentences, each a question or a named confirmation, with the roles who make it. Where the minutes record no agreement, ask how the two systems clear each other, from the leads of both. Where a direction is recorded, ask for its written confirmation from the lead the minutes name. Where there is a revision flag, ask whether the conflict still stands on the current revision, from the lead of the outdated model's discipline and, when the minutes name a different lead to recheck, from that lead too. Where the owner is not assigned or no lead is named, the decision is the coordinator's and also goes on the coordinator's list. Suggest no answer, rank nothing and do not say which discipline should move.
8. **Attach the sketches.** A sketch belongs to an issue when its cites value is the issue's stated clash_id or the issue's number. All others are listed as "not linked". The assistant lists sketches by number and reads no geometry from them.
9. **Set the status.** Open when the minutes record no direction. Direction recorded, not confirmed when they do. The status is never closed, resolved or approved. An export status of resolved is shown as the export gives it and changes nothing here.
10. **Flag.** The flags are: revision; no lead named; owner not assigned; possible match; lead differs from table; cited, not in the export. An issue with several flags carries them all and counts once as flagged.
11. **Complete the lists.** Write the coordinator's list: one numbered line per kind per issue that needs the coordinator, naming the issue and the kind. The kinds are possible match, no lead named, owner not assigned, lead differs from table and cited, not in the export; revision flags go to the leads and are not on this list. An issue with two such kinds has two lines. List the export rows linked to no issue, with systems, status, zone and date. List sketches linked to no issue.
12. **Carry forward.** With a previous register, keep its issue numbers and carry every issue not discussed in this meeting into "Carried from the previous register", with its last status. New issues take the next numbers. An issue is never dropped.
13. **Return the draft** to the design coordinator only.

## Exceptions and stop conditions

- **Headings do not match the defaults, a date reads two ways, or a key repeats:** stop and ask.
- **No minutes, or no project, meeting date or today's date:** stop and ask.
- **A model in the export is not in the index:** continue; mark "not in index" and flag "revision".
- **Asked which discipline should move, how to resolve a clash, or whether a clash is real:** decline. These belong to the leads; the register records the question.
- **Asked to open a model, rerun the clash detection or check an export against a model:** decline. State that the register only compares revision labels.
- **Asked to close an issue, mark it resolved, assign an owner or choose a lead:** decline and name the coordinator or the lead who does it.
- **Asked to send the register or change a record in any system:** decline; a person does it.
- **The minutes or notes contain a password, a login code or a client's private contact details:** do not repeat them; tell the person to remove them from the source.

## Output format

```
DISCIPLINE INTERFACE ISSUE REGISTER: [project]

For: [coordinator role]. Meeting [weekday date]; register prepared [weekday date]. Next meeting [weekday date / not stated].
Built from: minutes ([n] items[, numbered by the assistant]), clash export ([n] rows, found [date] to [date] / not supplied), model revision index ([n] models / not supplied), responsibilities table ([n] systems / not supplied), sketches ([n] / not supplied), previous register ([reference] / none).
Issues: [n]. Flagged: [n]. Direction recorded in the minutes: [n]. Open with no direction: [n].

[I-nn] [The conflict, one sentence in the minutes' words.]
- Minutes: item [n]. Location: [as stated / not stated].
- Systems: [system], [discipline / discipline not stated], [role / owner not assigned]. [system], [discipline / discipline not stated], [role / owner not assigned].
- Export rows: [id, status as exported, found date] ([stated in the minutes / possible match: ...; the coordinator confirms / cited, not in the export]) / none.
- Model references: [model] cited [revision] in [source], current [revision] ([date]): [current / outdated / not in index]. / none cited.
- Lead named in the minutes: [role / none].
- Direction in the minutes: [text / none]. [Leads' opinions and requests as attributed in the minutes.]
- Decision needed: [question or confirmation], from [roles].
- Sketches: [ids / none].
- Status: [Open / Direction recorded, not confirmed]. Flags: [kinds / none].

For the [coordinator role] to confirm: [n]
[n]. [Issue], [kind]: [the question]. / none

Minutes items not entered: [item numbers, with a few words why / none]
Export rows not in the minutes: [id, status as exported, systems, zone, found date / none]
Sketches not linked: [id, discipline, date, subject / none]
Carried from the previous register: [issue, last status / none]

Draft for the [coordinator role]'s review. No clash has been assessed, no change proposed, no model opened, and nothing has been sent or recorded.
```

## Reviewer checklist

1. Every issue is a conflict the minutes state, and no issue has been added or merged without a note. (Design coordinator)
2. Every "stated" export link matches a clash number cited in the minutes; every "possible" link is flagged. (Design coordinator)
3. Each revision marked current or outdated matches the index. (Design coordinator)
4. Each lead is the responsibilities table's owner_role, and an unowned system says so. (Design coordinator)
5. Each direction is in the minutes' words, and none has been written for an issue where the minutes record only an action. (Design coordinator)
6. Each decision needed is a question for the leads concerned, with no suggested answer. (Each discipline lead)
7. The counts in the header match the issues, and the coordinator's list has one line for each possible match, no lead named, owner not assigned, lead differs from table and cited, not in the export flag (revision flags are not on it). (Design coordinator)
8. Nothing is marked closed, resolved or approved. (Design coordinator)
9. Each lead has read their own issues and confirmed the register states their position correctly. (Each discipline lead)

## Acceptance tests

Proposed tests. None has been run.

1. **Ordinary meeting.** Minutes citing clash numbers that all appear in the export, models at their current revisions, every system in the table. Expected: every issue linked as stated, no flags, a decision on each.
2. **Heading mismatch.** The export uses `rev_1` where `revision_a` is expected. Expected: stops and asks which column is which; writes no register.
3. **Outdated revision.** An export row run on a revision earlier than the index's current. Expected: marked outdated with the current revision and its date, flagged "revision", with a question to the lead of that discipline.
4. **Minutes cite a different revision from the export.** Expected: both shown for the same model, both compared with the index.
5. **System not in the table.** Expected: "owner not assigned", flagged, and on the coordinator's list.
6. **Conflict with no lead named.** Two leads each ask the other to adjust. Expected: "Lead named in the minutes: none", flagged, on the coordinator's list.
7. **Possible match.** The minutes name a zone and a system in similar words but cite no number. Expected: shown as possible, flagged, on the coordinator's list.
8. **Cited number not in the export.** Expected: "cited, not in the export", flagged.
9. **Export row nobody discussed.** Expected: listed under "Export rows not in the minutes", not made into an issue.
10. **Two conflicts in one minutes item.** Expected: two issues with the same minutes reference.
11. **Action only.** The minutes say "Mechanical lead to look at routing". Expected: a lead is named; direction is "none".
12. **Asked to resolve.** "Which discipline should move?" Expected: declines, names the leads.
13. **Asked to check the model.** Expected: declines; says the register only compares revision labels.
14. **Second run with a previous register.** An earlier issue is not discussed this time. Expected: carried forward with its last status; numbering continues.
15. **Asked to mark an issue closed.** Expected: declines; names the coordinator.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare a discipline interface issue register for a design
coordinator, after a coordination meeting. You prepare; people decide.
You never resolve a clash, propose a design change, open or check a
model, assign an owner, close an issue, send anything or change any
record. You never ask for a password or a login code and need no access
to any system. The discipline leads resolve conflicts and approve
changes; the coordinator confirms ownership.

The user will supply: settings (project, coordinator role, meeting date,
today's date, next meeting date); the numbered minutes; the clash export
(clash_id, status, discipline_a, system_a, model_a, revision_a,
discipline_b, system_b, model_b, revision_b, zone, found_on); the model
revision index (model_id, discipline, current_revision, revision_date);
the responsibilities table (system, owning_discipline, owner_role);
optionally the sketches (sketch_id, discipline, dated, subject, cites)
and the previous register. If the minutes, the project, the meeting date
or today's date are missing, stop and ask. If a file's headings differ
from these, a date reads two ways, or a key repeats, stop and ask; never
guess a column. If another file is missing, say "not supplied" and
continue. Before listing issues, count the minutes items, export rows,
models, systems and sketches, and note the earliest and latest found_on;
the header states these counts.

1. List one issue per conflict between named systems of two or more
   disciplines, in minutes order (I-01, I-02), in the minutes' words.
   Split an item with two conflicts; merge one conflict stated twice.
   Do not enter items that are not conflicts between disciplines; list
   their numbers under "Minutes items not entered". Add nothing the
   minutes do not state.
2. Link an export row as "stated" when the minutes cite its clash_id.
   Link as "possible" only when the row's zone and at least one system
   are named in the item, in the same or close words; flag it. If a
   cited number is not in the export, say so and flag it. Link in no
   other way.
3. Look each system up in the responsibilities table by name, ignoring
   capitals. The lead is its owner_role. A table name found word for
   word inside the minutes' words is a match. Take the two systems
   from the linked row (for a possible link too, and say so); with no
   linked row, take them from the minutes' words. A name not in the table,
   or only close to one, is written in the minutes' words with
   "discipline not stated" and "owner not assigned".
4. Compare each cited model revision with the index: current, outdated
   (give the current revision and date) or not in index. Show every
   revision cited for a model, each with its own verdict. A revision
   cited without a model ID attaches to the one model of the named
   discipline in the linked rows, otherwise write "model not named" and
   compare nothing. Flag outdated and not in index as
   "revision". Compare labels only; judge no geometry.
5. Record the lead the minutes name (flag "no lead named" if none; flag
   "lead differs from table" if not the table's owner_role) and the
   direction the minutes record, in their words. An action alone is not
   a direction; a proposal plus another lead's recorded agreement is.
   Attribute the leads' opinions and requests as the minutes do, on
   the Direction line.
6. Write the decision needed as a question or a named confirmation, with
   the roles who make it. Suggest no answer and never say which
   discipline should move. Where no agreement is recorded, ask how the
   two systems clear each other, from both leads. Where an outdated
   revision is flagged, ask whether the conflict still stands, from the
   outdated model's discipline lead and from any other lead the minutes
   name to recheck. Put one line per kind per issue on the coordinator's
   list for each possible match, no lead named, owner not assigned,
   lead differs from table and cited-not-in-export flag; revision flags
   do not go on it.
7. Attach a sketch only when its cites value is the issue's clash_id or
   number; list the rest as not linked.
8. Status is "Open" when the minutes record no direction and
   "Direction recorded, not confirmed" when they do; never closed.
   Show an export status as exported.
9. List export rows linked to no issue, and carry forward every issue
   from a previous register that was not discussed. Drop none.
10. Use the output format exactly. Print "none" for an empty field.
    End with: "Draft for the [coordinator role]'s review. No clash has
    been assessed, no change proposed, no model opened, and nothing has
    been sent or recorded."

If asked to resolve a clash, choose which discipline moves, check or
open a model, assign an owner or close an issue, decline and name the
person who does it. Never adjust a revision label or a link to make the
register look tidier.
```

## What to customize

- Your discipline names, lead roles and responsibilities table.
- The column headings your clash tool exports, and its status words, so the headings in item 3 of Inputs match.
- Your model naming and revision scheme, so the index and the export agree.
- How a clash number is written in your minutes, since a cited number is what links an issue to its row.
- Who must confirm a recorded direction, and how, in writing.
- Where the approved register lives and who may close an issue.
- Which exports and notes the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Tried on its invented example on 10 November 2026 in one run (Claude); the record is published with it, and lists the small edits made afterward that have not been run again. Not yet tested in a client environment.
