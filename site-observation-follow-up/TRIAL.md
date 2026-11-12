# Site observation follow-up: two trial runs on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10 (both runs)

This record holds two runs. The first was made on version 0.1.0 and is kept exactly as it was recorded, including the findings that led to the fixes. The second was made on version 0.1.1, after those fixes, and is described after it. The inputs are the invented example published with this workflow template. No client data was used. The model was given only the template's instruction block and output format, and the six invented inputs from `public/example.md` (visit details, field notes, photograph set, drawing register, prior observation register, owner list). It did not see the example's report until after it had produced its own. The model that made the first run did not write the template; see the second run for its limits.

## First run (version 0.1.0): what came out

**SITE OBSERVATION REPORT: the Cedar Yard Annex, visit of Thursday 5 November 2026**

For: the visiting engineer, to verify, and the project manager, to confirm follow-up. Prepared Monday 9 November 2026 from: visit details, field notes (6 rows), photograph set (6 rows), drawing register (4 rows), prior observation register (3 rows), owner list (3 rows).
Column check: all headers matched.
Visit scope as typed: "Walk of Level 1 and the roof edge. Visual only; no testing and no measurement." Anything outside it is not covered by this report.
Summary: 6 field notes. Directly observed 3, reported 2, basis not stated 1. Linked to the prior register 3 notes, to 2 earlier entries. Earlier entries with no note this visit 1. Photographs: 6 in the set, 5 approved, 4 attached, 1 not approved and not attached, 1 approved and not cited by any note; notes with no photograph attached 2. Drawings: 5 notes cite a drawing; revision in hand matches the current revision for 2, differs for 2, not stated for 1; 1 cites no drawing. Proposed follow-up owners 4, not proposed 1, in conflict 1. Questions: 6 for the visiting engineer, 5 for the project manager.

**Data checks**

- Notes with no basis stated: F-05. It is not read as observed.
- Photographs cited but not approved: F-05 cites IMG-204, which is marked not approved. It is not attached.
- Notes with a drawing but no revision in hand: F-03 (A-501).
- Photograph location differs from the note's location: None.
- Disciplines with no entry on the owner list: Architecture (F-05).
- Locations or elements written several ways: None.
- Watch words: F-03 "complete"; F-04 "inside". A photograph does not show a concealed condition or that work is complete. The visiting engineer decides what may be stated.

**Directly observed: 3**

- F-01 Column base (Structural), Grid B/2. OBSERVED. Note: "Grout pad under the column base is cracked on the east side". Prior register: OBS-03, "Grout pad chipped at east edge", raised Thursday 8 October 2026, status open, owner Structural design lead, register due date passed by 10 days (due Friday 30 October 2026); linked because the note names it. Drawing: S-201, revision in hand B, current revision C (dated Monday 26 October 2026): differs. Photograph: IMG-201 (approved, taken Thursday 5 November 2026, "Column base east side"). Watch word: none. Proposed follow-up owner: Structural design lead (register owner). Technical statement: awaiting the visiting engineer's verification.
- F-06 Column base (Structural), Grid B/2. OBSERVED. Note: "Four of four anchor bolts are visible". Prior register: OBS-03, "Grout pad chipped at east edge", raised Thursday 8 October 2026, status open, owner Structural design lead, register due date passed by 10 days (due Friday 30 October 2026); linked because of the same location and element. Drawing: S-201, revision in hand B, current revision C (dated Monday 26 October 2026): differs. Photograph: IMG-205 (approved, taken Thursday 5 November 2026, "Anchor bolts"). Watch word: none. Proposed follow-up owner: Structural design lead (register owner). Technical statement: awaiting the visiting engineer's verification.
- F-02 Slab edge (Structural), Level 1 slab Grid C-D. OBSERVED. Note: "Hairline crack along the slab edge with the length not measured". Prior register: no earlier entry linked. Drawing: S-101, revision in hand C, current revision C (dated Monday 12 October 2026): matches. Photograph: IMG-202 (approved, taken Thursday 5 November 2026, "Slab edge"). Watch word: none. Proposed follow-up owner: Structural design lead (owner list). Technical statement: awaiting the visiting engineer's verification.

**Reported conditions: 2**

- F-04 Wall panel (Mechanical), Level 1 Room 1.03. REPORTED by Plumber of Contractor B. Note: "Plumber says the pipe sleeve inside the wall is sealed". Prior register: no earlier entry linked. Drawing: M-102, revision in hand A, current revision A (dated Monday 14 September 2026): matches. Photograph: IMG-203 (approved, taken Thursday 5 November 2026, "Wall panel removed at pipe sleeve"). Watch word: "inside". Proposed follow-up owner: Mechanical design lead (owner list). Technical statement: awaiting the visiting engineer's verification.
- F-03 Parapet flashing (Envelope), Roof edge north. REPORTED by Foreman of Contractor A. Note: "Foreman says the flashing work is complete". Prior register: OBS-04, "Flashing lifted at north corner", raised Thursday 8 October 2026, status open, owner Contractor A, register due date passed by 3 days (due Friday 6 November 2026); linked because of the same location and element. Drawing: A-501, revision in hand not stated, current revision B (dated Friday 2 October 2026): revision in hand not stated. Photograph: none supplied. Watch word: "complete". Proposed follow-up owner: in conflict. Register owner: Contractor A. Owner list for Envelope: Architectural design lead. Technical statement: awaiting the visiting engineer's verification.

**Basis not stated: 1**

- F-05 Handrail (Architecture), Level 1 corridor. BASIS NOT STATED. Note: "Handrail bracket looks loose". Prior register: no earlier entry linked. Drawing: none cited. Photograph: IMG-204 not approved, not attached. Watch word: none. Proposed follow-up owner: owner not proposed. Technical statement: awaiting the visiting engineer's verification.

**Earlier entries with no note this visit: 1**

- OBS-05, Level 1 Room 1.01, Door frame, "Frame out of plumb", status reported addressed, owner Contractor C, register due date Friday 23 October 2026.

**Photographs not used: 1**

- IMG-206, Roof edge north, "Flashing", approved, taken Thursday 5 November 2026. No note cites it.

**Questions for the visiting engineer**

1. F-01 Column base, Grid B/2. The revision of S-201 in hand was B; the current revision is C, dated Monday 26 October 2026. What do you want done about the revision difference?
2. F-06 Column base, Grid B/2. The revision of S-201 in hand was B; the current revision is C, dated Monday 26 October 2026. What do you want done about the revision difference?
3. F-04 Wall panel, Level 1 Room 1.03. Reported by Plumber of Contractor B; the note says "inside" the wall. IMG-203 is captioned "Wall panel removed at pipe sleeve". What may the report state about it?
4. F-03 Parapet flashing, Roof edge north. Reported by Foreman of Contractor A; the note says "complete". No photograph was supplied, and the revision of A-501 in hand is not stated (current revision B). What may the report state about it, and which revision did you have in hand?
5. F-05 Handrail, Level 1 corridor. The note does not say whether it was observed or reported, and its photograph IMG-204 is not approved. Was it observed or reported, and what do you want done about the photograph?
6. IMG-206 is approved, was taken at Roof edge north and is captioned "Flashing", but no note cites it. Which note, if any, does it belong to?

**Questions for the project manager**

1. OBS-03 (linked to F-01 and F-06), Grid B/2 column base. The register shows it open, owner Structural design lead, 10 days past its due date of Friday 30 October 2026. What follow-up and owner do you confirm?
2. OBS-04 (linked to F-03), Roof edge north parapet flashing. The register shows it open, owner Contractor A, 3 days past its due date of Friday 6 November 2026. What follow-up do you confirm?
3. F-03 Parapet flashing, Roof edge north. The register owner is Contractor A; the owner list names Architectural design lead for Envelope. Who owns the follow-up?
4. F-05 Handrail, Level 1 corridor. Architecture is not on the owner list, so no owner is proposed. Who owns the follow-up?
5. OBS-05, Level 1 Room 1.01 door frame. No note this visit links to it. The register shows it as reported addressed, owner Contractor C, due Friday 23 October 2026. What do you want done with it?

Every technical statement is the field note's own wording until the visiting engineer approves it. The project manager confirms every follow-up owner, including those proposed without a question.

Draft for the visiting engineer's verification and the project manager's confirmation. No condition has been assessed, and no drawing, register entry or owner has been changed. Nothing has been sent.

## First run: what was observed

The run produced every part the output format asks for. Nothing in the inputs made it stop: all headers matched, every basis, status and approval word was allowed, every date was real, no number was duplicated, every reference was on its list, and the reported notes named who reported them. Every count in the summary was checked against the lists. Every weekday and date was checked against a calendar. Every fact in the output is in the inputs.

It was compared with the example's published report afterwards. The two agree on the groups, the register links, the drawing results, the photographs, the data checks and the watch words. They differ in these ways.

- **Owner counts.** The example counts F-03 as a proposed owner (5 proposed, 1 not proposed) and prints no "in conflict" figure. This run counted F-03 as in conflict, because the instructions say to print both owners and ask, and the output format has a place for "in conflict". That gives 4 proposed, 1 not proposed, 1 in conflict.
- **Project manager questions.** The example has 4: it folds the owner conflict for F-03 into the question about OBS-04. This run has 5, following the rule "one for each register entry that is open and past due and linked" and "one for each owner not proposed or in conflict" literally, so OBS-04 and the F-03 owner conflict are two questions.
- **Question wording.** This run asked the visiting engineer "What do you want done about the revision difference?", to avoid putting the choice of revision into the question. The example originally asked which revision to record against; it now uses this neutral wording.
- **Question order.** The example orders the visiting engineer's questions by note number. This run followed the order of the report's groups. The template does not say which.
- **Data checks.** Same findings. The example words them a little differently and puts the watch-word check in one line; this run used one line per check, in the template's order.

## First run: ambiguities and shortcomings

- **A note in conflict over its owner.** The template does not say whether a note whose register owner and owner-list owner differ counts among the "proposed" owners. The summary line has both "proposed" and "in conflict", but the example treats such a note as proposed.
- **One question or two for the same item.** An open, past-due register entry linked to a note whose owner is in conflict can be read as one question or two. The sentence about a note with several reasons sharing one question is in the part about the visiting engineer's questions only.
- **Question order** inside each reader's list is not set.
- **Two notes linked to one register entry** (F-01 and F-06 to OBS-03). The template does not say whether the entry's details are printed in full under each note (this run did) or only once. The summary's "to [n] earlier entries" is read here as the number of different entries.
- **Watch words.** The template does not say whether a watch word matches inside a longer word (for example "safe" inside "unsafe", or "done" inside "abandoned") or only as a whole word, or whether other forms count (for example "completes" for "complete"). This run matched whole words only. The list also leaves out words that appear in the example, such as "sealed", which was correctly not flagged.
- **Link by text** is on location and element only, so F-06 (anchor bolts) links to OBS-03 (a chipped grout pad) because both are at Grid B/2, Column base. The template says a link is only a pointer, and this run said no more than that, but a reader may find the link surprising.
- **Square-bracket references** in the "When to use it" section, such as [punch list consolidation], read as placeholders to fill in. They name other workflow templates and are not marked as links.
- **Version notes** still say the template has not yet been tried on its invented example. They will need updating once this record is accepted.

The first run's note that its example's report differs on owner counts and project manager questions describes the example as it stood then. The example was corrected afterwards (see the second run).

Fixing the first two items in the template (a stated rule for how a conflict is counted, and when a conflict and a past-due entry share a question) would make the output of any two runs agree more closely.

## Second run (version 0.1.1): what changed in the template

After an independent review of the first run, the template was edited. A conflict between the register owner and the owner list is now printed as "in conflict" with both roles and counted as in conflict, not as proposed. An owner in conflict on a note linked to a past-due entry is asked in that entry's question. Questions are ordered by note number. Watch words match whole words in any ordinary form, "loose" is a watch word, and a line sends anything that may concern safety to the project's safety professional. A register entry shared by two notes has its details printed under each note and counted once. The related workflow templates are written as plain names. The example's report was corrected to agree, and F-05 now draws the watch word "loose".

## Second run: what came out

The model was given only the 0.1.1 instruction block and output format and the six invented inputs, in one Claude Code session. It is the same model that edited the template, so this run is not independent; it shows whether the edited instructions produce the corrected report, not whether a fresh reader would. It produced the following.

**SITE OBSERVATION REPORT: the Cedar Yard Annex, visit of Thursday 5 November 2026**

For: the visiting engineer, to verify, and the project manager, to confirm follow-up. Prepared Monday 9 November 2026 from: visit details, field notes (6 rows), photograph set (6 rows), drawing register (4 rows), prior observation register (3 rows), owner list (3 rows).
Column check: all headers matched.
Visit scope as typed: "Walk of Level 1 and the roof edge. Visual only; no testing and no measurement." Anything outside it is not covered by this report.
Summary: 6 field notes. Directly observed 3, reported 2, basis not stated 1. Linked to the prior register 3 notes, to 2 earlier entries. Earlier entries with no note this visit 1. Photographs: 6 in the set, 5 approved, 4 attached, 1 not approved and not attached, 1 approved and not cited by any note; notes with no photograph attached 2. Drawings: 5 notes cite a drawing; revision in hand matches the current revision for 2, differs for 2, not stated for 1; 1 cites no drawing. Proposed follow-up owners 4, not proposed 1, in conflict 1. Questions: 6 for the visiting engineer, 4 for the project manager.

**Data checks**

- Notes with no basis stated: F-05. It is not read as observed.
- Photographs cited but not approved: F-05 cites IMG-204, which is marked not approved. It is not attached.
- Notes with a drawing but no revision in hand: F-03 (A-501).
- Photograph location differs from the note's location: None.
- Disciplines with no entry on the owner list: Architecture (F-05).
- Locations or elements written several ways: None.
- Watch words: F-03 "complete"; F-04 "inside"; F-05 "loose". A photograph does not show a concealed condition or that work is complete. The visiting engineer decides what may be stated, and anything that may concern safety goes to the project's safety professional.

**Directly observed: 3**

- F-01 Column base (Structural), Grid B/2. OBSERVED. Note: "Grout pad under the column base is cracked on the east side". Prior register: OBS-03, "Grout pad chipped at east edge", raised Thursday 8 October 2026, status open, owner Structural design lead, register due date passed by 10 days (due Friday 30 October 2026); linked because the note names it. Drawing: S-201, revision in hand B, current revision C (dated Monday 26 October 2026): differs. Photograph: IMG-201 (approved, taken Thursday 5 November 2026, "Column base east side"). Watch word: none. Proposed follow-up owner: Structural design lead (register owner). Technical statement: awaiting the visiting engineer's verification.
- F-06 Column base (Structural), Grid B/2. OBSERVED. Note: "Four of four anchor bolts are visible". Prior register: OBS-03, "Grout pad chipped at east edge", raised Thursday 8 October 2026, status open, owner Structural design lead, register due date passed by 10 days (due Friday 30 October 2026); linked because of the same location and element. Drawing: S-201, revision in hand B, current revision C (dated Monday 26 October 2026): differs. Photograph: IMG-205 (approved, taken Thursday 5 November 2026, "Anchor bolts"). Watch word: none. Proposed follow-up owner: Structural design lead (register owner). Technical statement: awaiting the visiting engineer's verification.
- F-02 Slab edge (Structural), Level 1 slab Grid C-D. OBSERVED. Note: "Hairline crack along the slab edge with the length not measured". Prior register: no earlier entry linked. Drawing: S-101, revision in hand C, current revision C (dated Monday 12 October 2026): matches. Photograph: IMG-202 (approved, taken Thursday 5 November 2026, "Slab edge"). Watch word: none. Proposed follow-up owner: Structural design lead (owner list). Technical statement: awaiting the visiting engineer's verification.

**Reported conditions: 2**

- F-04 Wall panel (Mechanical), Level 1 Room 1.03. REPORTED by Plumber of Contractor B. Note: "Plumber says the pipe sleeve inside the wall is sealed". Prior register: no earlier entry linked. Drawing: M-102, revision in hand A, current revision A (dated Monday 14 September 2026): matches. Photograph: IMG-203 (approved, taken Thursday 5 November 2026, "Wall panel removed at pipe sleeve"). Watch word: "inside". Proposed follow-up owner: Mechanical design lead (owner list). Technical statement: awaiting the visiting engineer's verification.
- F-03 Parapet flashing (Envelope), Roof edge north. REPORTED by Foreman of Contractor A. Note: "Foreman says the flashing work is complete". Prior register: OBS-04, "Flashing lifted at north corner", raised Thursday 8 October 2026, status open, owner Contractor A, register due date passed by 3 days (due Friday 6 November 2026); linked because of the same location and element. Drawing: A-501, revision in hand not stated, current revision B (dated Friday 2 October 2026): revision in hand not stated. Photograph: none supplied. Watch word: "complete". Proposed follow-up owner: in conflict: register owner Contractor A, owner list Architectural design lead. Technical statement: awaiting the visiting engineer's verification.

**Basis not stated: 1**

- F-05 Handrail (Architecture), Level 1 corridor. BASIS NOT STATED. Note: "Handrail bracket looks loose". Prior register: no earlier entry linked. Drawing: none cited. Photograph: IMG-204 not approved, not attached. Watch word: "loose". Proposed follow-up owner: owner not proposed. Technical statement: awaiting the visiting engineer's verification.

**Earlier entries with no note this visit: 1**

- OBS-05, Level 1 Room 1.01, Door frame, "Frame out of plumb", status reported addressed, owner Contractor C, register due date Friday 23 October 2026.

**Photographs not used: 1**

- IMG-206, Roof edge north, "Flashing", approved, taken Thursday 5 November 2026. No note cites it.

**Questions for the visiting engineer**

1. F-01 Column base, Grid B/2. The revision of S-201 in hand was B; the current revision is C, dated Monday 26 October 2026. What do you want done about the revision difference?
2. F-03 Parapet flashing, Roof edge north. Reported by Foreman of Contractor A; the note says "complete". No photograph was supplied, and the revision of A-501 in hand is not stated (current revision B). What may the report state about it, and which revision did you have in hand?
3. F-04 Wall panel, Level 1 Room 1.03. Reported by Plumber of Contractor B; the note says "inside" the wall. IMG-203 is captioned "Wall panel removed at pipe sleeve". What may the report state about it?
4. F-05 Handrail, Level 1 corridor. The note does not say whether it was observed or reported, its photograph IMG-204 is not approved, and the note says "loose". Was it observed or reported, what do you want done about the photograph, what may the report state about it, and does the project's safety professional need to be told?
5. F-06 Column base, Grid B/2. The revision of S-201 in hand was B; the current revision is C, dated Monday 26 October 2026. What do you want done about the revision difference?
6. IMG-206 is approved, was taken at Roof edge north and is captioned "Flashing", but no note cites it. Which note, if any, does it belong to?

**Questions for the project manager**

1. OBS-03 (linked to F-01 and F-06), Grid B/2 column base. The register shows it open, owner Structural design lead, 10 days past its due date of Friday 30 October 2026. What follow-up and owner do you confirm?
2. OBS-04 (linked to F-03), Roof edge north parapet flashing. The register shows it open, owner Contractor A, 3 days past its due date of Friday 6 November 2026. The owner of F-03 is also in conflict: the register owner is Contractor A and the owner list names Architectural design lead for Envelope. What follow-up do you confirm, and who owns it?
3. F-05 Handrail, Level 1 corridor. Architecture is not on the owner list, so no owner is proposed. Who owns the follow-up?
4. OBS-05, Level 1 Room 1.01 door frame. No note this visit links to it. The register shows it as reported addressed, owner Contractor C, due Friday 23 October 2026. What do you want done with it?

Every technical statement is the field note's own wording until the visiting engineer approves it. The project manager confirms every follow-up owner, including those proposed without a question.

Draft for the visiting engineer's verification and the project manager's confirmation. No condition has been assessed, and no drawing, register entry or owner has been changed. Nothing has been sent.

## Second run: what was observed

The run produced every part the output format asks for, and every count in the summary was checked against the lists and every weekday against a calendar. The points the review raised came out as the edits intend.

- **Owners.** F-03 was printed as "in conflict" with both roles and counted there: 4 proposed, 1 not proposed, 1 in conflict. The conflict was asked in OBS-04's question, giving 4 project manager questions.
- **Order.** Questions followed note number, with the unused photograph last. Data checks followed the order of step 2. F-03's drawing line ends with the result word.
- **Watch words.** "loose" in F-05 was found as a whole word; no word was found inside a longer word.
- **Shared entry.** OBS-03's details were printed under both F-01 and F-06; the entry was counted once in "to 2 earlier entries" and asked about once.
- **Against the example.** The report agrees with the corrected example except in the wording of the visiting engineer's revision questions (this run asks what is to be done about the difference; the example originally asked which revision to record against and has since been changed to match) and of the F-05 question.

## Second run: shortcomings that remain

- This run was not independent and was not a fresh product session, so it does not show how another reader would resolve any remaining ambiguity.
- The link by text still joins F-06 (anchor bolts) to OBS-03 (a chipped grout pad) because both are at Grid B/2, Column base. The template now says a link by text is a pointer for the visiting engineer to confirm, and suggests finer element names, but the link is still made.
- "Does the project's safety professional need to be told?" is a question the template writes for any safety-type watch word; the template does not itself judge what concerns safety.
