# Deliverable issue completeness check: an invented example

*Illustrative example with invented data.* The firm, the project, the people and every document below are invented. Engineering Firm A is an invented consulting engineering firm. Priya, its document controller, is checking the package for a bridge deck rehabilitation (an invented project, "Site 7") on 15 October 2026, five days before the planned issue to the client. First come the inputs she supplied, in full, then the checklist the workflow template returned.

## The inputs

### 1. Settings

```
Package: Site 7 bridge deck rehabilitation, design package
Purpose of issue: issue to client for review
Planned issue: 20 October 2026
Responsible engineer: Engineer Z
Quality reviewer: Reviewer Y
Run by: Priya, document controller
Today: 15 October 2026
Outcomes that count as approved: Approved
```

### 2. Issue checklist

```
item_id,requirement,applies_to,test
C01,Document is in the index and has an entry in the revision register,all,listed
C02,Index revision register revision and title block revision agree,all,revision-match
C03,A review record approves the issue revision by someone other than the author and is dated on or after the revision,all,review-record
C04,Every calculation cited is in the index and cited at its current revision,"report,drawing",calc-reference
C05,Responsible engineer's confirmation of the design basis is recorded on the report cover,report,by-hand
```

### 3. Deliverable index

```
doc_no,title,type,revision,title_block_revision,author
CALC-001,Deck slab flexure calculation,calculation,B,B,Engineer P
CALC-002,Bearing pad calculation,calculation,A,A,Engineer Q
RPT-001,Rehabilitation design basis report,report,C,C,Engineer R
DWG-101,Deck plan and sections,drawing,D,C,Engineer S
DWG-102,Bearing replacement details,drawing,B,B,Engineer S
DWG-103,Traffic staging plan,drawing,A,A,Engineer T
```

### 4. Revision register

```
doc_no,revision,date,description
CALC-001,A,2026-09-14,First issue for check
CALC-001,B,2026-10-05,Updated for revised dead load
CALC-002,A,2026-09-21,First issue for check
RPT-001,B,2026-09-30,Client comments incorporated
RPT-001,C,2026-10-12,Bearing section added
DWG-101,C,2026-10-02,Joint locations revised
DWG-101,D,2026-10-14,Updated to calculation revision B
DWG-102,A,2026-09-28,First issue
DWG-102,B,2026-10-09,Bearing size changed
DWG-104,A,2026-10-10,Lighting conduit layout
```

### 5. Recorded review approvals

```
doc_no,revision,reviewer,date,outcome
CALC-001,B,Checker M,2026-10-08,Approved
CALC-002,A,Checker M,2026-09-19,Approved
RPT-001,C,Engineer R,2026-10-13,Approved
DWG-101,C,Checker N,2026-10-03,Approved
DWG-102,B,Checker N,2026-10-10,Approved
```

### 6. Calculation references

```
doc_no,calc_ref,calc_revision
RPT-001,CALC-001,B
RPT-001,CALC-002,A
DWG-101,CALC-001,A
DWG-102,CALC-002,A
DWG-102,CALC-009,A
```

## The output

```
DELIVERABLE ISSUE COMPLETENESS CHECK: Site 7 bridge deck rehabilitation, design package

For: Priya, document controller. Purpose of issue: issue to client for review, planned 20 October 2026. Responsible engineer: Engineer Z. Quality reviewer: Reviewer Y.
Prepared: 15 October 2026, from the issue checklist (5 items), the deliverable index (6 documents), the revision register (10 rows), the review approvals (5 rows) and the calculation references (5 rows). Outcomes that count as approved: Approved.
Results: 23 (12 met, 9 not met, 2 left for a person). Documents with at least one not met: 5 of 6.

To settle before issue: 6
1. CALC-002: the only approval of revision A is dated before the revision. Question for Reviewer Y: is the approval to stand?
2. RPT-001: the only approval of revision C was recorded by its author, Engineer R. Question for Reviewer Y: who checks revision C?
3. DWG-101: the title block shows revision C while the index and register show D; the only approval is for revision C; it cites CALC-001 at revision A, and the index shows B. Question for Engineer Z: which revision is right, D or the title block's C, who approves revision D, and which revision of CALC-001 does the drawing rest on?
4. DWG-102: it cites CALC-009, which is not in the index. Question for Engineer Z: is CALC-009 part of this package, and if so what is its number, revision and approval?
5. DWG-103: it has no register entry and no approval. Question for Priya: is DWG-103 meant to be in this package? Question for Reviewer Y: who approves revision A?
6. DWG-104: it is in the register and not in the index. Question for Priya: is DWG-104 part of this package?

Document by document

CALC-001 Deck slab flexure calculation (calculation, revision B)
  C01 Met: register entry for revision B, 5 October 2026.
  C02 Met: index B, register B, title block B.
  C03 Met: Checker M approved revision B on 8 October 2026; author Engineer P.

CALC-002 Bearing pad calculation (calculation, revision A)
  C01 Met: register entry for revision A, 21 September 2026.
  C02 Met: index A, register A, title block A.
  C03 Not met: Checker M approved revision A on 19 September 2026, before the revision's register date, 21 September 2026. See 1.

RPT-001 Rehabilitation design basis report (report, revision C)
  C01 Met: register entry for revision C, 12 October 2026.
  C02 Met: index C, register C, title block C.
  C03 Not met: the only record for revision C is by Engineer R, the author. See 2.
  C04 Met: cites CALC-001 at B (index B) and CALC-002 at A (index A).
  C05 By hand: the assistant cannot see the report cover. Decided by Engineer Z.

DWG-101 Deck plan and sections (drawing, revision D)
  C01 Met: register entry for revision D, 14 October 2026.
  C02 Not met: index D, register D, title block C. See 3.
  C03 Not met: the only record is for revision C (Checker N, 3 October 2026); none for revision D. See 3.
  C04 Not met: cites CALC-001 at A; the index shows B. See 3.

DWG-102 Bearing replacement details (drawing, revision B)
  C01 Met: register entry for revision B, 9 October 2026.
  C02 Met: index B, register B, title block B.
  C03 Met: Checker N approved revision B on 10 October 2026; author Engineer S.
  C04 Not met: cites CALC-002 at A (index A) and CALC-009 at A, which is not in the index. See 4.

DWG-103 Traffic staging plan (drawing, revision A)
  C01 Not met: no register entry. See 5.
  C02 Not met: no register revision to compare; index A, title block A. See 5.
  C03 Not met: no review record. See 5.
  C04 By hand: no calculation references supplied for DWG-103. Decided by Engineer Z.

Package-level discrepancies: 2
In the register and not in the index: DWG-104, revision A, 10 October 2026, "Lighting conduit layout". See 6.
Cited and not in the index: CALC-009 (cited by DWG-102 at revision A). See 4.
In the review approvals and not in the index: none.

Left for a person: 2
RPT-001 C05: Engineer Z checks that the report cover records the responsible engineer's design-basis confirmation.
DWG-103 C04: Engineer Z says whether the drawing relies on any calculation.

Completeness check only. No calculation has been checked, no design judged and nothing signed off, issued, changed or sent. Engineer Z and Reviewer Y confirm technical adequacy and authorize issue.
```

Every result traces to a row in a list Priya supplied. What happens next is hers and the engineers': they settle the six questions, correct the lists and the documents themselves, and run the check again.
