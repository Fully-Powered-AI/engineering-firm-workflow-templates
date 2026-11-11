# RFI review package: a trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs are the invented example in [example.md](example.md): an invented firm, project, contractor and documents. No client data was used.

## Inputs used

The settings, the request (RFI-0042), the document index (7 rows), the three extracts, the four prior responses and the two routing rules, all as given under "The inputs" in example.md. The instructions followed were the fenced block in the capability template and its output format.

## A flaw in how this trial was run

The instruction was to read the example's output only after producing mine. The command that printed the inputs also printed the first part of the example's output (down to the second prior response), so I saw that much before writing my own. The second half, from the last prior response onward (mentioned but not supplied, routing and the questions), I did not see until after. Agreement on the first half therefore counts for less than agreement on the second.

## What came out

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
1. S-201. The sender cites revision C; the index shows revision D, dated Friday 6 November 2026. The extract supplied is from revision D; no extract of revision C is supplied. What does the person want done about the revision the sender cited?
2. EP-3. S-201 revision D, Note 7, prints 12 in. by 12 in.; S-501 revision B, Detail 4, prints 10 in. by 10 in. What does the person want done about the two printed sizes?
3. RFI-0019. It cites S-501 revision A; the index shows revision B. What does the person want done about this earlier response?
4. RFI-0031. It cites S-501 revision A; the index shows revision B. What does the person want done about this earlier response?
5. ASI-07. Its title shares "ramp" and "edge" with the subject, and no extract is supplied. What does the person want done about whether it is added?
6. The rebar at gridline 5. The sender mentions it, and no reinforcing drawing or measurement is supplied. What does the person want done about it?

Questions for the project manager
7. The sender writes that it "may need additional detailing time", and that the plates are to be fabricated on Monday 23 November 2026, 7 days away; the response is due Friday 20 November 2026. What does the person want done about the possible effect on time?
Interpretation and approval of the response rest with the responsible engineer, approval of any commitment rests with the project manager, and nothing here answers the question.

Draft for the project engineer's decisions. No response has been drafted, no one has been contacted, and no log or record has been changed.
```

## What was observed

Every part of the output format was produced, in order. Nothing in the instructions required me to stop: all labels and headers matched, there were no duplicate numbers and no unreadable dates. I checked the dates against a calendar and the word matches by hand.

Differences from the published example:

- **Question count and grouping.** I wrote 7 questions (6 and 1); the example has 6 (5 and 1). The example puts RFI-0019 and RFI-0031 in one question; I wrote one each. The template says a question is written for "a prior response that cites an older revision", which reads as one per response, so I think mine follows the text, but the template does not say.
- **Counts that follow.** The example's summary says 5 and 1 for the questions; mine says 6 and 1.
- **Wording only.** The question about S-201 differs in phrasing (questions 2, 5, 6 and 7 also differ slightly in wording, with no difference in fact), and the example's first prior-response question names S-501 as its heading where mine names the RFI. The routing line in the example adds "(ASI-07)" after the architectural role; mine does not. The example's question for the project manager repeats the fabrication date and so does mine.
- **Everything else matched:** the register entry, dates and day counts, the cited-document labels, the single possibly-related document, the extracts, the one differing value, the three listed prior responses and their older-revision notes, the one item not supplied, and the one cost or time sentence.

Facts not in the inputs: none found in either output. Weekdays and day counts are computed from the inputs.

Where the instructions were ambiguous and I had to choose:

1. **Order of extracts.** "Document-number order" is not defined for a mix of "05 12 00" and "S-201". I put the section number first, as the example does.
2. **One question per prior response, or one per document.** See above.
3. **"Mentioned but not supplied".** The template does not say whether a document the sender cited but at a revision other than the one supplied (S-201 revision C) belongs here. I treated it as a question about the revision instead.
4. **NO REVISION CITED.** The question list has no entry for a cited document with no revision (05 12 00), so none was asked, although it is a gap a reviewer might want raised.
5. **Which sentences count as effects.** The effect words are matched in "each sentence", but the template gives no rule for splitting sentences where a date such as "2026-11-23." ends in a full stop. This did not matter here.
6. **Prior-response relevance.** RFI-0019 qualified two ways (the cited document and two shared subject words); RFI-0036 qualified only by the two shared words, because A-310 is not a listed document. The instructions handled both, but only after reading step 8 of the procedure; the shorter instruction block says only "cite a listed document or share two subject words".
7. **Possibly related.** The procedure step says "a word match... ignoring the stop words" and counts words of four or more letters; the instruction block says "index rows not cited" and also four letters or more. They describe the same test in different words and agree in practice.
8. **Summary line "Open questions: [n]"** depends on the grouping choice in item 2.
9. **"Defaults used".** The settings said "the default" for three items, so I named all three. The template does not say whether to name a default that was set explicitly to "the default".

Shortcomings of the trial: it is one run, by one model, on one example whose acceptance tests (the twelve proposed in the template) were not run. Only the happy path was exercised; none of the stop conditions was triggered. The first half of the example's output was seen before mine was written, as noted above. The template has not been tried on any client data or in any product other than Claude.

## Edits made after this trial

After this trial, small wording edits were made following the editorial review that came before the independent review (round 1). They were not run again. The recorded output above is unchanged.

- The template and its instructions now say that a prior response citing an older revision gets one question each, and the published example now has seven questions (6 and 1), as in this run. The "Question count and grouping" difference above describes the example as it stood on the day of the run.
- The example's routing line no longer ends in "(ASI-07)", as in this run.
- The template now says a cited document labelled NO REVISION CITED raises no question, that extracts are sorted as text, and where a sentence ends when splitting the question for effect words.
- The instruction block now gives the full test for relevant prior responses.
- The example's question 1 now says revision D is "dated" rather than "issued" Friday 6 November 2026, because the index column is `revision_date`. This run wrote "dated".
- Questions 2, 5, 6 and 7 of the example were reworded slightly after this run; no fact differs from the run above.
- The template now settles two ambiguities listed above: a cited document supplied only at another revision is not listed under "Mentioned but not supplied" (item 3), and a default is named under "Defaults used" even when the settings say "the default" (item 9).
- Later wording edits to the template added the whole-word, ignoring-case title match and the kept-but-named prior response that cites a document missing from the index to the instruction block, and set where the closing sentence goes when there are no questions. None was run again.
