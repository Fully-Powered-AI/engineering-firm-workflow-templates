# RFI review package: an invented example

*Illustrative example with invented data.* The firm, the project, the contractor, the people, the documents and every number below are invented. Firm Z is an invented engineering firm. Dana, its project engineer, is the invented person running the work. Contractor A, the builder of an invented parking structure, has sent a request for information. First come the inputs Dana supplied, in full, then the packet the workflow template returned.

## The inputs

### 1. Settings

```
Project: Alder Street Parking Structure
Today: 2026-11-16
Decider: project engineer
Commitment approver: project manager
Response period: the default
Effect words: the default
Stop words: the default
```

### 2. The request

```
rfi_no: RFI-0042
subject: Ramp edge embed plate size at second floor
from: Contractor A
discipline_addressed: structural
received_date: 2026-11-13
response_due_date: 2026-11-20
references_cited: S-201 rev C; S-501 rev B; 05 12 00
site_context:
question: Drawing S-201 revision C shows embed plate EP-3 at the ramp edge as 12 in. by 12 in. Detail 4 on S-501 revision B shows EP-3 as 10 in. by 10 in. Which governs? The plates are to be fabricated on 2026-11-23. If the larger plate is used, the rebar at gridline 5 may not clear it, and we may need additional detailing time.
```

### 3. The document index

```
doc_no,title,type,discipline,current_revision,revision_date
S-201,Second floor framing plan,drawing,structural,D,2026-11-06
S-202,Third floor framing plan,drawing,structural,C,2026-10-23
S-501,Slab edge and embed details,drawing,structural,B,2026-10-09
A-310,Ramp plan and sections,drawing,architectural,C,2026-10-16
05 12 00,Structural steel framing,specification,structural,1,2026-08-14
03 30 00,Cast-in-place concrete,specification,structural,2,2026-09-04
ASI-07,Ramp edge revisions,bulletin,architectural,0,2026-11-06
```

### 4. The extracts

```
doc_no: S-201
revision: D
location: Note 7, gridlines 5 to 6
text: EP-3 AT RAMP EDGE: PLATE 12 IN. X 12 IN. X 3/4 IN., FOUR 3/4 IN. HEADED STUDS.

doc_no: S-501
revision: B
location: Detail 4
text: EP-3: PLATE 10 IN. X 10 IN. X 3/4 IN., FOUR 3/4 IN. HEADED STUDS.

doc_no: 05 12 00
revision: 1
location: Part 2, item 2.4
text: Embedded plates and anchors shown on the structural drawings are furnished by the steel fabricator and set by the concrete contractor.
```

### 5. The prior responses

```
rfi_no,date_answered,subject,response_text,answered_by,docs_cited
RFI-0019,2026-09-28,Embed plate EP-1 at column base,Use EP-1 as shown on S-501 revision A.,structural engineer of record,S-501 rev A
RFI-0027,2026-10-12,Third floor duct sleeve at beam,Sleeve location is as shown on S-202 revision B.,structural engineer of record,S-202 rev B
RFI-0031,2026-10-20,Embed plate EP-2 at stair landing,EP-2 is as shown on S-501 revision A detail 3.,structural engineer of record,S-501 rev A
RFI-0036,2026-11-02,Ramp edge curb height,Curb height is 6 in. as shown on A-310 revision C.,architect's coordinator,A-310 rev C
```

### 6. The routing rules

```
discipline,reviewer_role
structural,structural engineer of record
architectural,architect's coordinator
```

## What the workflow template returned

```
RFI REVIEW PACKAGE: Alder Street Parking Structure, RFI-0042

For: project engineer. Prepared Monday 16 November 2026 from: RFI text, document index (7 rows), extracts (3), prior responses (4 rows), routing rules (2 rows), settings.
Column check: all labels and headers matched.
Settings: response period 7 days, counted in calendar days. Defaults used: response period, effect words, stop words.
Summary: RFI-0042, response due in 4 days. Documents cited: 3 (1 revision differs, 0 not in index). Possibly related, not cited: 1. Printed values that differ: 1. Prior responses listed: 3 of 4 checked (2 cite an older revision). Mentioned but not supplied: 1. Possible effects on cost or time: 1. Open questions: 7 (6 for the responsible engineer, 1 for the project manager).

Data checks
- None.

Register entry
- RFI: RFI-0042, Ramp edge embed plate size at second floor.
- From: Contractor A. Addressed to: structural.
- Received: Friday 13 November 2026, 3 days ago.
- Response due: sender asks for Friday 20 November 2026 (4 days away); the response period gives Friday 20 November 2026.
- Dates in the question: Monday 23 November 2026, 7 days away.
- Question as written: "Drawing S-201 revision C shows embed plate EP-3 at the ramp edge as 12 in. by 12 in. Detail 4 on S-501 revision B shows EP-3 as 10 in. by 10 in. Which governs? The plates are to be fabricated on 2026-11-23. If the larger plate is used, the rebar at gridline 5 may not clear it, and we may need additional detailing time."
- Status: Open. No response drafted.

Documents cited
- S-201 Second floor framing plan, structural. Cited: revision C. Current: revision D, Friday 6 November 2026. REVISION DIFFERS. Extract supplied at revision D.
- S-501 Slab edge and embed details, structural. Cited: revision B. Current: revision B, Friday 9 October 2026. REVISION MATCHES. Extract supplied at revision B.
- 05 12 00 Structural steel framing, structural. Cited: no revision. Current: revision 1, Friday 14 August 2026. NO REVISION CITED. Extract supplied at revision 1.

Possibly related, not cited
- ASI-07 Ramp edge revisions, bulletin, architectural. Matching words: ramp, edge. No extract supplied.

Extracts, word for word
- 05 12 00 revision 1, Part 2, item 2.4: "Embedded plates and anchors shown on the structural drawings are furnished by the steel fabricator and set by the concrete contractor."
- S-201 revision D, Note 7, gridlines 5 to 6: "EP-3 AT RAMP EDGE: PLATE 12 IN. X 12 IN. X 3/4 IN., FOUR 3/4 IN. HEADED STUDS."
- S-501 revision B, Detail 4: "EP-3: PLATE 10 IN. X 10 IN. X 3/4 IN., FOUR 3/4 IN. HEADED STUDS."

Printed values that differ
- EP-3 plate length and width: S-201 revision D, Note 7, gridlines 5 to 6, prints 12 in. by 12 in.; S-501 revision B, Detail 4, prints 10 in. by 10 in. No view is taken on which governs.

Prior responses (4 checked, 3 listed)
- RFI-0019, answered Monday 28 September 2026 by structural engineer of record, "Embed plate EP-1 at column base": "Use EP-1 as shown on S-501 revision A." Cited: S-501 rev A. Cites revision A; current is B.
- RFI-0031, answered Tuesday 20 October 2026 by structural engineer of record, "Embed plate EP-2 at stair landing": "EP-2 is as shown on S-501 revision A detail 3." Cited: S-501 rev A. Cites revision A; current is B.
- RFI-0036, answered Monday 2 November 2026 by architect's coordinator, "Ramp edge curb height": "Curb height is 6 in. as shown on A-310 revision C." Cited: A-310 rev C.

Mentioned but not supplied
- "the rebar at gridline 5": no reinforcing drawing or measurement is in the index or the extracts.
- Site context: not supplied.

Possible effects on cost or time, for the project manager
- "additional": "If the larger plate is used, the rebar at gridline 5 may not clear it, and we may need additional detailing time."

Routing proposed
- Addressed to structural: structural engineer of record. If relevant: architectural: architect's coordinator. Commitments: project manager.

Questions for the responsible engineer
1. S-201. The sender cites revision C; the index shows revision D, dated Friday 6 November 2026. The extract supplied is from revision D, and the text of revision C is not supplied. What does the person want done about the revision the sender worked from?
2. EP-3. S-201 revision D prints 12 in. by 12 in. and S-501 revision B prints 10 in. by 10 in. What does the person want done about the two printed sizes?
3. RFI-0019. It cites S-501 revision A; the index shows revision B. What does the person want done about this earlier response?
4. RFI-0031. It cites S-501 revision A; the index shows revision B. What does the person want done about this earlier response?
5. ASI-07. Its title shares ramp and edge with the subject, and no extract is supplied. What does the person want done about whether it is added?
6. Rebar at gridline 5. The sender mentions it, and no reinforcing drawing, measurement or site context is supplied. What does the person want done to obtain it?

Questions for the project manager
7. The sender writes that it "may need additional detailing time", and says the plates are to be fabricated on Monday 23 November 2026, 7 days away; the response is due Friday 20 November 2026. What does the person want done about the possible effect on time?
Interpretation and approval of the response rest with the responsible engineer, approval of any commitment rests with the project manager, and nothing here answers the question.

Draft for the project engineer's decisions. No response has been drafted, no one has been contacted, and no log or record has been changed.
```
