# Deliverable issue completeness check: a trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs were the invented example in `public/example.md` (settings, issue checklist, deliverable index, revision register, review approvals and calculation references). No client data was used. The run followed the instruction block and the output format in `member/template.md`. The run read only the inputs first and compared its output with the published example afterwards. The run was done by a model that did not write the template.

## What came out

The check produced every part of the output format. These are its substantial parts.

```
DELIVERABLE ISSUE COMPLETENESS CHECK: Site 7 bridge deck rehabilitation, design package

For: Priya, document controller. Purpose of issue: issue to client for review, planned 20 October 2026. Responsible engineer: Engineer Z. Quality reviewer: Reviewer Y.
Prepared: 15 October 2026, from the issue checklist (5 items), the deliverable index (6 documents), the revision register (10 rows), the review approvals (5 rows) and the calculation references (5 rows). Outcomes that count as approved: Approved.
Results: 23 (12 met, 9 not met, 2 left for a person). Documents with at least one not met: 5 of 6.

To settle before issue: 6
1. CALC-002: the only approval (Checker M, revision A) is dated 19 September 2026; the register date of revision A is 21 September 2026. Question for Reviewer Y: is the approval to stand?
2. RPT-001: the only approval of revision C is by Engineer R, who is the author. Question for Reviewer Y: who checks revision C?
3. DWG-101: the title block shows C; the index and register show D. The only approval is for revision C. It cites CALC-001 at revision A; the index shows B (the register entry for D reads "Updated to calculation revision B"). Question for Engineer Z: which revision of CALC-001 does the drawing cite, and who approves revision D?
4. DWG-102: it cites CALC-009 at revision A, which is not in the index. Question for Engineer Z: is CALC-009 part of this package?
5. DWG-103: no register entry, no approval. Question for Priya: is DWG-103 meant to be in this package? Question for Reviewer Y: who approves revision A?
6. DWG-104: in the register (revision A, 10 October 2026, "Lighting conduit layout") and not in the index. Question for Priya: is DWG-104 part of this package?

Document by document

CALC-001 Deck slab flexure calculation (calculation, revision B)
  C01 Met: register entry for revision B, 5 October 2026.
  C02 Met: index B, register B, title block B.
  C03 Met: Checker M approved revision B on 8 October 2026; author Engineer P.

CALC-002 Bearing pad calculation (calculation, revision A)
  C01 Met: register entry for revision A, 21 September 2026.
  C02 Met: index A, register A, title block A.
  C03 Not met: Checker M approved revision A on 19 September 2026, before the register date, 21 September 2026. See 1.

RPT-001 Rehabilitation design basis report (report, revision C)
  C01 Met: register entry for revision C, 12 October 2026.
  C02 Met: index C, register C, title block C.
  C03 Not met: the approval of revision C is by Engineer R, the author. See 2.
  C04 Met: cites CALC-001 at B (index B) and CALC-002 at A (index A).
  C05 By hand: the assistant cannot see the report cover. Engineer Z decides.

DWG-101 Deck plan and sections (drawing, revision D)
  C01 Met: register entry for revision D, 14 October 2026.
  C02 Not met: index D, register D, title block C. See 3.
  C03 Not met: the only record is for revision C (Checker N, 3 October 2026). See 3.
  C04 Not met: cites CALC-001 at A; the index shows B. See 3.

DWG-102 Bearing replacement details (drawing, revision B)
  C01 Met: register entry for revision B, 9 October 2026.
  C02 Met: index B, register B, title block B.
  C03 Met: Checker N approved revision B on 10 October 2026; author Engineer S.
  C04 Not met: CALC-002 at A is right (index A); CALC-009 at A is not in the index. See 4.

DWG-103 Traffic staging plan (drawing, revision A)
  C01 Not met: no register entry. See 5.
  C02 Not met: no register revision; index A, title block A. See 5.
  C03 Not met: no review record. See 5.
  C04 By hand: no calculation references supplied for this document. Engineer Z decides.

Package-level discrepancies: 2
In the register and not in the index: DWG-104, revision A, 10 October 2026, "Lighting conduit layout".
Cited and not in the index: CALC-009 (cited by DWG-102 at revision A).
In the review approvals and not in the index: none.

Left for a person: 2
RPT-001 C05: Engineer Z checks the report cover.
DWG-103 C04: Engineer Z says whether the drawing relies on any calculation.

Completeness check only. No calculation has been checked, no design judged and nothing signed off, issued, changed or sent. Engineer Z and Reviewer Y confirm technical adequacy and authorize issue.
```

## What was observed

- Every required part was produced. The counts add up: 12 met, 9 not met and 2 left for a person make 23, and 5 of 6 documents have a not met result.
- All 23 results, the package-level findings and the six question groups agree with the published example. The differences are in wording only. The published example words some questions more fully (for example, it asks whether a title block is to be corrected, and gives the reason for DWG-103 C04 a different sentence). This run's questions were shorter.
- The run mentioned that the register entry for DWG-101 revision D reads "Updated to calculation revision B". The published example leaves that out. Both facts come from the inputs.
- No fact in either output is missing from the inputs. The role named to decide DWG-103 C04 (Engineer Z) comes from the template's by-hand rule, which the template does not state for this case (see below).
- Nothing in the run required stopping: the headers matched, no test word was unknown and no document number was repeated.

### Where the instructions were ambiguous

- **Who decides a By hand result for a document that cites no calculation.** Step 4 names the responsible engineer only for the `by-hand` test. For `calc-reference` with no citations it says only "By hand: no references supplied". The run assumed Engineer Z, as the published example does.
- **Whether a package-level discrepancy that a document group covers is a separate question.** Step 6 says a discrepancy "not already covered" by a document group gets its own. CALC-009 was judged covered by the DWG-102 group; DWG-104 was not covered and got its own.
- **How to word a question.** Step 6 says to recommend nothing. A question such as "is the approval to stand, or is the revision to be checked again?" sits close to a recommendation. The run kept to the open form.
- **Who a question goes to when a document needs both an administrative and a technical answer.** DWG-103 was given two questions in one group, to the document controller and the quality reviewer. The template allows this ("puts a question to the role") but does not say whether a group may hold more than one.
- **A leftover placeholder.** Inputs item 6 reads "[your approved outcomes]" in the middle of a sentence. It is clear from context, but it looks like unfilled text.
- **Step 5 has a stray semicolon** ("not in the index; Print what was found").
- **The instruction block is shorter than the procedure.** It omits the "no checklist items apply" and zero-count lines, the rule for a missing register revision, and the By hand reasons for unsupplied approvals. These sit in the output-format section the person pastes with it, but not in the block itself.
- **Note added after the run (10 November 2026):** the wording ambiguities above on who decides a By hand calc-reference, more than one role per group, the stray semicolon and the zero-count lines in the instruction block were addressed afterwards in the template, and the missing-register-revision rule and the reason for unsupplied approvals are now in the block too. The "[your ...]" marker is the customization convention, not an unfilled placeholder. These later edits have not been run again; the observations above record the run as it was.
- The acceptance tests in the template are still marked "Proposed. None has been run." This run covers only the invented example, not those sixteen tests.

This was one run by one model on one invented example. It does not show how the template performs on a real package or in other AI products.
