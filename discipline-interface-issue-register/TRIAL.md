# Discipline interface issue register: one trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs are the invented example in `public/example.md` (the Block C Laboratory Annex at an invented engineering firm). No client data was used. The run was a single pass in a fresh session, separate from the one that wrote the template. It read the member template and the example's seven inputs, followed the instruction block and the output format, and produced the register before reading the example's output. It then compared the two.

## Inputs used

The seven inputs in `public/example.md`, section "The inputs": settings, six numbered minutes items, a six-row clash export, a four-model revision index, a seven-system responsibilities table, three sketches, and no previous register.

## What came out

The register covered all six minutes items as six issues. Counts in the header: Issues 6, Flagged 4, Direction recorded 2, Open with no direction 4.

- **I-01** (item 1, CL-101, stated): Mechanical lead and Structural lead. MECH-C P04 current; STR-C P07 outdated (current P08, 2026-11-02). No direction; the Structural lead's refusal recorded as an opinion. Sketch SK-M-07. Open. Flag: revision.
- **I-02** (item 2, CL-102, stated): both models current. Direction recorded: the cable tray rises 150 mm. Electrical lead to confirm in writing by Friday 13 November 2026. Sketch SK-E-03. Direction recorded, not confirmed. No flags.
- **I-03** (item 3, no number cited): CL-103 shown as a possible match on zone and systems. STR-C P06 outdated. No lead named. Open. Flags: revision, no lead named, possible match.
- **I-04** (item 4, CL-105, stated): STR-C shown at P07 (export) and P06 (minutes), both outdated against P08. No direction, because "recheck" is an action only. Open. Flag: revision.
- **I-05** (item 5, no export row): the generator exhaust flue is "owner not assigned"; the roof plant platform is the Structural lead's. No lead named. Open. Flags: owner not assigned, no lead named.
- **I-06** (item 6, CL-106, stated): both models current. Direction recorded: the pipework moves 100 mm towards the wall and the Electrical lead agrees. Direction recorded, not confirmed. No flags.

The coordinator's list had four lines, one per kind (I-03 possible match, I-03 no lead named, I-05 owner not assigned, I-05 no lead named). The run weighed one line per issue against one per kind and chose per kind. Items not entered: none. Export rows not in the minutes: CL-104 (resolved as exported, Level 1 east bay, found 2026-10-22). Sketches not linked: SK-S-02. Carried from the previous register: none. The register ended with the required closing sentence.

## What was observed

- Every required part of the output format was produced. The assistant was not told to stop for anything: headings matched, no date read two ways, no key repeated, and there were minutes.
- The result matched the published example on all counts, links, revision verdicts, flags, statuses, sketches and the unlisted export row and sketch. It did not match word for word.
- Differences from the published example:
  - I-04 decision: the template says to ask the lead of the outdated model's discipline. That is the Structural lead. The example asks the Electrical lead after the recheck, with the Structural lead. Following the template gave a narrower question.
  - I-04 model references: the example folds the minutes' P06 into one line with P07. The run listed both revisions as outdated.
  - I-06 decision: the example adds "once the mechanical model carries it", which comes from the minutes' "to update the model". The run asked only for written confirmation.
  - Titles: the example's I-06 sentence uses the word "conflict", which the minutes item does not use.
- No fact appears in the run's output that is not in the inputs. In the example's output, every fact traces to the inputs.

## Where the instructions were ambiguous

1. **Counting the coordinator's list.** "One numbered line per item that needs the coordinator" can mean per issue or per kind. The example is per kind. The template should say so.
2. **A system with no table entry and no discipline.** For the flue, nothing says what to write in the discipline place. The example writes only "owner not assigned". The run had to choose between leaving the place blank and writing "discipline not stated".
3. **A partial name match.** The minutes say "the roof plant platform edge" and the table has "Roof plant platform". The matching rule says a name that is only close is "owner not assigned". The run treated it as a match because the table name appears word for word. A stricter reading would not.
4. **Which model a minutes revision belongs to.** Item 4 says "the structural model at revision P06". It does not name STR-C. The run assumed STR-C because the linked row has only one structural model. The template does not say how to attach a revision to a model the minutes do not name by its ID.
5. **What counts as a direction.** Item 6 says "Electrical lead agrees" but not "agreed in the meeting". The run counted it as a direction. Step 6 does not cover a proposal plus agreement.
6. **Model references on a possible link.** Step 5 says to take them from "each linked row". It is unclear whether an unconfirmed possible match should supply revisions and a revision question. The example does, and so did the run.
7. **The decision for an outdated revision.** Step 7 names the outdated model's discipline lead, but when the lead named in the minutes differs (as in I-04), the template does not say whether to ask both.
8. **Version notes.** The template still says it was not yet tried on its example. That is now out of date and should change when this record is accepted.

No fact was invented by the run. The run did not open any model, assess any clash, or suggest which discipline should move.

## Edits made after this run

After an independent review, small edits were made to the template, the example and the profile. They have not been run again, and nothing above has been changed. They are: the label and version notes now say the template was tried on its invented example (ambiguity 8); the coordinator's list is defined as one line per kind per issue, with the kinds named and revision flags excluded (ambiguity 1); a table name found word for word inside the minutes' words counts as a match (ambiguity 3); a system with no discipline is written "discipline not stated" (ambiguity 2); a minutes revision with no model ID attaches to the one model of the named discipline in the linked rows, and two revisions for one model get one verdict each (ambiguity 4); a proposal plus another lead's recorded agreement counts as a direction (ambiguity 5); a recheck by a lead other than the outdated model's discipline lead is asked of both (ambiguity 7). In the example, the I-04 decision now asks how the two systems clear each other and the revision question of both leads, the flue's discipline reads "discipline not stated", and opinions sit on the Direction line. A second round of small edits followed a further review, also not run again: the example's I-04 now gives each STR-C revision its own verdict, the I-03 decision line carries the coordinator's question of who takes the issue forward, the I-06 title and decision use the minutes' words, and the flue sentence was removed from the I-05 Direction line; the Direction rule now covers leads' opinions and requests as the minutes state them, attributed; and the instruction block states the step 1 counts, where the systems are taken from, and how status follows direction. A rerun on the example would make this record stronger and has not been done.
