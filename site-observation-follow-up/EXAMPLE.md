# Site observation follow-up: an invented example

*Illustrative example with invented data.* The project (the Cedar Yard Annex, a small two-storey building), the contractors (Contractor A, B and C), the drawings, the notes, the photographs and every date below are invented. People are referred to by role. The project manager runs the report on Monday 9 November 2026, after a visit by the visiting engineer on Thursday 5 November 2026.

The inputs come first, in full, so the template can be run on them. The report follows.

## The inputs

### 1. Visit details (typed by the project manager)

```
Project: the Cedar Yard Annex
Visit date: Thursday 5 November 2026
Today: Monday 9 November 2026
Scope of the visit: Walk of Level 1 and the roof edge. Visual only; no testing and no measurement.
Visiting engineer: the visiting engineer
Confirms follow-up: the project manager
```

### 2. Field notes

```
note_no,location,element,discipline,note_text,basis,reported_by,photo_ref,drawing_no,rev_in_hand,refers_to
F-01,Grid B/2,Column base,Structural,Grout pad under the column base is cracked on the east side,observed,,IMG-201,S-201,B,OBS-03
F-02,Level 1 slab Grid C-D,Slab edge,Structural,Hairline crack along the slab edge with the length not measured,observed,,IMG-202,S-101,C,
F-03,Roof edge north,Parapet flashing,Envelope,Foreman says the flashing work is complete,reported,Foreman of Contractor A,,A-501,,
F-04,Level 1 Room 1.03,Wall panel,Mechanical,Plumber says the pipe sleeve inside the wall is sealed,reported,Plumber of Contractor B,IMG-203,M-102,A,
F-05,Level 1 corridor,Handrail,Architecture,Handrail bracket looks loose,,,IMG-204,,,
F-06,Grid B/2,Column base,Structural,Four of four anchor bolts are visible,observed,,IMG-205,S-201,B,
```

### 3. Photograph set

```
photo_ref,taken_date,location,caption,approved
IMG-201,2026-11-05,Grid B/2,Column base east side,yes
IMG-202,2026-11-05,Level 1 slab Grid C-D,Slab edge,yes
IMG-203,2026-11-05,Level 1 Room 1.03,Wall panel removed at pipe sleeve,yes
IMG-204,2026-11-05,Level 1 corridor,Handrail,no
IMG-205,2026-11-05,Grid B/2,Anchor bolts,yes
IMG-206,2026-11-05,Roof edge north,Flashing,yes
```

### 4. Drawing register

```
drawing_no,title,current_revision,revision_date
S-101,Level 1 slab plan,C,2026-10-12
S-201,Column schedule and details,C,2026-10-26
M-102,Level 1 mechanical plan,A,2026-09-14
A-501,Roof details,B,2026-10-02
```

### 5. Prior observation register

```
obs_no,location,element,observation,date_raised,register_status,owner,due_date,source_visit
OBS-03,Grid B/2,Column base,Grout pad chipped at east edge,2026-10-08,open,Structural design lead,2026-10-30,Visit 2
OBS-04,Roof edge north,Parapet flashing,Flashing lifted at north corner,2026-10-08,open,Contractor A,2026-11-06,Visit 2
OBS-05,Level 1 Room 1.01,Door frame,Frame out of plumb,2026-10-08,reported addressed,Contractor C,2026-10-23,Visit 2
```

### 6. Owner list

```
discipline,proposed_owner
Structural,Structural design lead
Mechanical,Mechanical design lead
Envelope,Architectural design lead
```

## The output

**SITE OBSERVATION REPORT: the Cedar Yard Annex, visit of Thursday 5 November 2026**

For: the visiting engineer, to verify, and the project manager, to confirm follow-up. Prepared Monday 9 November 2026 from: visit details, field notes (6 rows), photograph set (6 rows), drawing register (4 rows), prior observation register (3 rows), owner list (3 rows).  
Column check: all headers matched.  
Visit scope as typed: "Walk of Level 1 and the roof edge. Visual only; no testing and no measurement." Anything outside it is not covered by this report.  
Summary: 6 field notes. Directly observed 3, reported 2, basis not stated 1. Linked to the prior register 3 notes, to 2 earlier entries. Earlier entries with no note this visit 1. Photographs: 6 in the set, 5 approved, 4 attached, 1 not approved and not attached, 1 approved and not cited by any note; notes with no photograph attached 2. Drawings: 5 notes cite a drawing; revision in hand matches the current revision for 2, differs for 2, not stated for 1; 1 cites no drawing. Proposed follow-up owners 4, not proposed 1, in conflict 1. Questions: 6 for the visiting engineer, 4 for the project manager.

**Data checks**

- F-05 does not say whether it was observed or reported. It is not read as observed.
- F-05 cites IMG-204, which is in the set as not approved. It is not attached.
- F-03 does not state the revision in hand for A-501.
- No photograph is recorded at a different location from the note that cites it.
- The owner list has no entry for Architecture (F-05).
- No location or element is written several ways.
- Watch words: F-03 "complete", F-04 "inside", F-05 "loose". A photograph does not show a concealed condition or that work is complete; the visiting engineer decides what may be stated, and anything that may concern safety goes to the project's safety professional.

**Directly observed: 3**

- **F-01** Column base (Structural), Grid B/2. OBSERVED. Note: "Grout pad under the column base is cracked on the east side". Prior register: OBS-03, "Grout pad chipped at east edge", raised Thursday 8 October 2026, status open, owner Structural design lead, register due date passed by 10 days (due Friday 30 October 2026); linked because the note names it. Drawing: S-201, revision in hand B, current revision C (dated Monday 26 October 2026): differs. Photograph: IMG-201 (approved, taken Thursday 5 November 2026, "Column base east side"). Watch word: none. Proposed follow-up owner: Structural design lead (register owner). Technical statement: awaiting the visiting engineer's verification.
- **F-06** Column base (Structural), Grid B/2. OBSERVED. Note: "Four of four anchor bolts are visible". Prior register: OBS-03, "Grout pad chipped at east edge", raised Thursday 8 October 2026, status open, owner Structural design lead, register due date passed by 10 days (due Friday 30 October 2026); linked because of the same location and element. Drawing: S-201, revision in hand B, current revision C (dated Monday 26 October 2026): differs. Photograph: IMG-205 (approved, taken Thursday 5 November 2026, "Anchor bolts"). Watch word: none. Proposed follow-up owner: Structural design lead (register owner). Technical statement: awaiting the visiting engineer's verification.
- **F-02** Slab edge (Structural), Level 1 slab Grid C-D. OBSERVED. Note: "Hairline crack along the slab edge with the length not measured". Prior register: no earlier entry linked. Drawing: S-101, revision in hand C, current revision C (dated Monday 12 October 2026): matches. Photograph: IMG-202 (approved, taken Thursday 5 November 2026, "Slab edge"). Watch word: none. Proposed follow-up owner: Structural design lead (owner list). Technical statement: awaiting the visiting engineer's verification.

**Reported conditions: 2**

- **F-04** Wall panel (Mechanical), Level 1 Room 1.03. REPORTED by Plumber of Contractor B. Note: "Plumber says the pipe sleeve inside the wall is sealed". Prior register: no earlier entry linked. Drawing: M-102, revision in hand A, current revision A (dated Monday 14 September 2026): matches. Photograph: IMG-203 (approved, taken Thursday 5 November 2026, "Wall panel removed at pipe sleeve"). Watch word: "inside". Proposed follow-up owner: Mechanical design lead (owner list). Technical statement: awaiting the visiting engineer's verification.
- **F-03** Parapet flashing (Envelope), Roof edge north. REPORTED by Foreman of Contractor A. Note: "Foreman says the flashing work is complete". Prior register: OBS-04, "Flashing lifted at north corner", raised Thursday 8 October 2026, status open, owner Contractor A, register due date passed by 3 days (due Friday 6 November 2026); linked because of the same location and element. Drawing: A-501, revision in hand not stated, current revision B (dated Friday 2 October 2026): revision in hand not stated. Photograph: none supplied. Watch word: "complete". Proposed follow-up owner: in conflict: register owner Contractor A, owner list Architectural design lead. Technical statement: awaiting the visiting engineer's verification.

**Basis not stated: 1**

- **F-05** Handrail (Architecture), Level 1 corridor. BASIS NOT STATED. Note: "Handrail bracket looks loose". Prior register: no earlier entry linked. Drawing: none cited. Photograph: IMG-204 not approved, not attached. Watch word: "loose". Proposed follow-up owner: owner not proposed. Technical statement: awaiting the visiting engineer's verification.

**Earlier entries with no note this visit: 1**

- OBS-05, Level 1 Room 1.01, Door frame, "Frame out of plumb", status reported addressed, owner Contractor C, register due date Friday 23 October 2026.

**Photographs not used: 1**

- IMG-206, Roof edge north, "Flashing", approved, taken Thursday 5 November 2026. No note cites it.

**Questions for the visiting engineer**

1. F-01 Column base, Grid B/2. You had revision B of S-201; the current revision is C, dated Monday 26 October 2026. What do you want done about the revision difference?
2. F-03 Parapet flashing, Roof edge north. Reported by Foreman of Contractor A as "Foreman says the flashing work is complete". No photograph is attached and the revision of A-501 in hand is not stated (current revision B). What may the report state about it, and which revision did you have?
3. F-04 Wall panel, Level 1 Room 1.03. Reported by Plumber of Contractor B, and the note says "inside" the wall. IMG-203 is captioned "Wall panel removed at pipe sleeve". What may the report state about it?
4. F-05 Handrail, Level 1 corridor. The note does not say whether it was observed or reported, IMG-204 is not approved, and the note says "loose". Was it observed or reported, may the photograph be approved, and what may the report state about it? Does the project's safety professional need to be told?
5. F-06 Column base, Grid B/2. You had revision B of S-201; the current revision is C, dated Monday 26 October 2026. What do you want done about the revision difference?
6. IMG-206 is approved and was taken at Roof edge north, captioned "Flashing", but no note cites it. Which note, if any, does it belong to?

**Questions for the project manager**

1. OBS-03 (linked to F-01 and F-06), Grid B/2 column base. The register shows it open, owner Structural design lead, 10 days past its due date of Friday 30 October 2026. What follow-up and owner do you confirm?
2. OBS-04 (linked to F-03), Roof edge north parapet flashing. The register shows it open, owner Contractor A, 3 days past its due date of Friday 6 November 2026. F-03 is also in conflict over its owner: the register owner is Contractor A and the owner list names Architectural design lead for Envelope. What follow-up do you confirm, and who owns it?
3. F-05 Handrail, Level 1 corridor. Architecture is not on the owner list, so no owner is proposed. Who owns the follow-up?
4. OBS-05, Level 1 Room 1.01 door frame. No note this visit mentions it. The register shows it as reported addressed, due Friday 23 October 2026. What do you want done with it?

Every technical statement is the field note's own wording until the visiting engineer approves it. The project manager confirms every follow-up owner, including those proposed without a question.

Draft for the visiting engineer's verification and the project manager's confirmation. No condition has been assessed, and no drawing, register entry or owner has been changed. Nothing has been sent.
