# Discipline interface issue register: an invented example

*Illustrative example with invented data.* The firm, the project, the roles, the model names, the clash numbers, the dates and every line below are invented. The firm is an invented engineering consultancy, Quillon Bay Engineers, with structural, civil, mechanical and electrical teams and a design coordinator. First come the inputs the coordinator supplied, in full, then the register the capability returned.

## The inputs

### 1. Settings

```
Project: Block C Laboratory Annex
Coordinator role: Design coordinator
Meeting date: Thursday 5 November 2026
Today: Friday 6 November 2026
Next coordination meeting: Thursday 19 November 2026
```

### 2. Minutes (numbered items, as typed by the coordinator)

```
1. Level 2, grids C4 to C6: chilled water mains clash with the primary steel framing (CL-101). Mechanical lead to look at routing the mains below the beam. Structural lead will not accept a web penetration in the transfer beam. No agreement reached.
2. Level 1 corridor: supply air ductwork and main cable tray share the ceiling void (CL-102). Agreed in the meeting that the cable tray rises 150 mm. Electrical lead to confirm in writing by Friday 13 November 2026.
3. Grid line A: a pile cap sits close to the new stormwater drain. Civil lead and Structural lead each asked the other to adjust. Nobody was asked to take it forward.
4. Level 3 plant room: main cable tray crosses the primary steel framing (CL-105). Electrical lead says the tray was laid out against the structural model at revision P06. Electrical lead to recheck against the current structural model.
5. Roof: the generator exhaust flue rises through the roof plant platform edge. Nobody present could say who owns the flue.
6. Level 2 riser: chilled water pipework and main cable tray (CL-106). Mechanical lead moves the pipework 100 mm towards the wall; Electrical lead agrees. Mechanical lead to update the model.
```

### 3. Clash export

```
clash_id,status,discipline_a,system_a,model_a,revision_a,discipline_b,system_b,model_b,revision_b,zone,found_on
CL-101,active,Mechanical,Chilled water pipework,MECH-C,P04,Structural,Primary steel framing,STR-C,P07,Level 2 grids C4-C6,2026-10-29
CL-102,active,Mechanical,Supply air ductwork,MECH-C,P04,Electrical,Main cable tray,ELEC-C,P03,Level 1 corridor,2026-10-29
CL-103,new,Civil,Stormwater drainage,CIV-C,P02,Structural,Foundation pile caps,STR-C,P06,Grid line A,2026-10-29
CL-104,resolved,Mechanical,Supply air ductwork,MECH-C,P03,Structural,Secondary steel framing,STR-C,P06,Level 1 east bay,2026-10-22
CL-105,new,Electrical,Main cable tray,ELEC-C,P03,Structural,Primary steel framing,STR-C,P07,Level 3 plant room,2026-10-29
CL-106,active,Mechanical,Chilled water pipework,MECH-C,P04,Electrical,Main cable tray,ELEC-C,P03,Level 2 riser,2026-10-29
```

### 4. Model revision index

```
model_id,discipline,current_revision,revision_date
STR-C,Structural,P08,2026-11-02
MECH-C,Mechanical,P04,2026-10-28
ELEC-C,Electrical,P03,2026-10-27
CIV-C,Civil,P02,2026-10-20
```

### 5. Responsibilities table

```
system,owning_discipline,owner_role
Primary steel framing,Structural,Structural lead
Roof plant platform,Structural,Structural lead
Foundation pile caps,Structural,Structural lead
Chilled water pipework,Mechanical,Mechanical lead
Supply air ductwork,Mechanical,Mechanical lead
Main cable tray,Electrical,Electrical lead
Stormwater drainage,Civil,Civil lead
```

### 6. Discipline sketches

```
sketch_id,discipline,dated,subject,cites
SK-M-07,Mechanical,2026-11-04,Chilled water mains rerouted below the transfer beam,CL-101
SK-E-03,Electrical,2026-11-04,Cable tray raised 150 mm in the corridor,CL-102
SK-S-02,Structural,2026-11-03,Transfer beam reinforcement option,-
```

### 7. Previous register

None. This is the first register for the project.

## The output

**DISCIPLINE INTERFACE ISSUE REGISTER: Block C Laboratory Annex**

For: Design coordinator. Meeting Thursday 5 November 2026; register prepared Friday 6 November 2026. Next meeting Thursday 19 November 2026.
Built from: minutes (6 items), clash export (6 rows, found 2026-10-22 to 2026-10-29), model revision index (4 models), responsibilities table (7 systems), sketches (3), previous register (none).
Issues: 6. Flagged: 4. Direction recorded in the minutes: 2. Open with no direction: 4.

**I-01** Chilled water mains clash with the primary steel framing.
- Minutes: item 1. Location: Level 2, grids C4 to C6.
- Systems: Chilled water pipework, Mechanical, Mechanical lead. Primary steel framing, Structural, Structural lead.
- Export rows: CL-101, active, found 2026-10-29 (stated in the minutes).
- Model references: MECH-C cited P04 in CL-101, current P04 (2026-10-28): current. STR-C cited P07 in CL-101, current P08 (2026-11-02): outdated.
- Lead named in the minutes: Mechanical lead.
- Direction in the minutes: none. The Structural lead will not accept a web penetration in the transfer beam.
- Decision needed: how the chilled water mains clear the primary steel framing, from the Mechanical lead and the Structural lead; and whether the conflict still stands on STR-C P08, from the Structural lead.
- Sketches: SK-M-07.
- Status: Open. Flags: revision.

**I-02** Supply air ductwork and main cable tray share the Level 1 corridor ceiling void.
- Minutes: item 2. Location: Level 1 corridor.
- Systems: Supply air ductwork, Mechanical, Mechanical lead. Main cable tray, Electrical, Electrical lead.
- Export rows: CL-102, active, found 2026-10-29 (stated in the minutes).
- Model references: MECH-C cited P04 in CL-102, current P04 (2026-10-28): current. ELEC-C cited P03 in CL-102, current P03 (2026-10-27): current.
- Lead named in the minutes: Electrical lead.
- Direction in the minutes: the cable tray rises 150 mm, agreed in the meeting.
- Decision needed: written confirmation of the recorded direction by Friday 13 November 2026, from the Electrical lead.
- Sketches: SK-E-03.
- Status: Direction recorded, not confirmed. Flags: none.

**I-03** A pile cap sits close to the new stormwater drain.
- Minutes: item 3. Location: Grid line A.
- Systems: Stormwater drainage, Civil, Civil lead. Foundation pile caps, Structural, Structural lead (names taken from the possible export row).
- Export rows: CL-103, new, found 2026-10-29 (possible match: same zone and systems named in similar words; the coordinator confirms).
- Model references: CIV-C cited P02 in CL-103, current P02 (2026-10-20): current. STR-C cited P06 in CL-103, current P08 (2026-11-02): outdated.
- Lead named in the minutes: none.
- Direction in the minutes: none. The Civil lead and the Structural lead each asked the other to adjust.
- Decision needed: how the pile cap and the drain clear each other, from the Civil lead and the Structural lead; and whether the conflict still stands on STR-C P08, from the Structural lead; and which lead takes the issue forward, from the Design coordinator.
- Sketches: none.
- Status: Open. Flags: revision, no lead named, possible match.

**I-04** Main cable tray crosses the primary steel framing.
- Minutes: item 4. Location: Level 3 plant room.
- Systems: Main cable tray, Electrical, Electrical lead. Primary steel framing, Structural, Structural lead.
- Export rows: CL-105, new, found 2026-10-29 (stated in the minutes).
- Model references: ELEC-C cited P03 in CL-105, current P03 (2026-10-27): current. STR-C cited P07 in CL-105, current P08 (2026-11-02): outdated. STR-C cited P06 in minutes item 4, current P08 (2026-11-02): outdated.
- Lead named in the minutes: Electrical lead.
- Direction in the minutes: none.
- Decision needed: how the main cable tray and the primary steel framing clear each other, from the Electrical lead and the Structural lead; and whether the conflict still stands on STR-C P08, from the Structural lead and from the Electrical lead, who is to recheck.
- Sketches: none.
- Status: Open. Flags: revision.

**I-05** The generator exhaust flue rises through the roof plant platform edge.
- Minutes: item 5. Location: Roof.
- Systems: Generator exhaust flue, discipline not stated, owner not assigned. Roof plant platform, Structural, Structural lead.
- Export rows: none.
- Model references: none cited.
- Lead named in the minutes: none.
- Direction in the minutes: none.
- Decision needed: who owns the generator exhaust flue, from the Design coordinator; then how the flue clears the roof plant platform, from the leads concerned.
- Sketches: none.
- Status: Open. Flags: owner not assigned, no lead named.

**I-06** Chilled water pipework and main cable tray in the Level 2 riser.
- Minutes: item 6. Location: Level 2 riser.
- Systems: Chilled water pipework, Mechanical, Mechanical lead. Main cable tray, Electrical, Electrical lead.
- Export rows: CL-106, active, found 2026-10-29 (stated in the minutes).
- Model references: MECH-C cited P04 in CL-106, current P04 (2026-10-28): current. ELEC-C cited P03 in CL-106, current P03 (2026-10-27): current.
- Lead named in the minutes: Mechanical lead.
- Direction in the minutes: the pipework moves 100 mm towards the wall; the Electrical lead agrees.
- Decision needed: written confirmation of the recorded move, from the Mechanical lead, who is to update the model.
- Sketches: none.
- Status: Direction recorded, not confirmed. Flags: none.

**For the Design coordinator to confirm: 4**
1. I-03, possible match: whether CL-103 is this conflict.
2. I-03, no lead named: which lead takes the issue forward, the Civil lead or the Structural lead.
3. I-05, owner not assigned: who owns the generator exhaust flue.
4. I-05, no lead named: which lead takes the issue forward once the flue has an owner.

**Minutes items not entered:** none.
**Export rows not in the minutes:** CL-104, resolved as exported, Supply air ductwork (Mechanical) and Secondary steel framing (Structural), Level 1 east bay, found 2026-10-22.
**Sketches not linked:** SK-S-02, Structural, 2026-11-03, Transfer beam reinforcement option (cites no issue).
**Carried from the previous register:** none.

Draft for the Design coordinator's review. No clash has been assessed, no change proposed, no model opened, and nothing has been sent or recorded.
