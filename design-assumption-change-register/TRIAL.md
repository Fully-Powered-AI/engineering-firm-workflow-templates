# Design assumption change register: tried on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs are the invented example in [example.md](example.md): the Quay Road pump station upgrade, its six recorded requirements, six source items, one previous register row and the settings. No client data was used. This is the third pass. Earlier passes used earlier wording of the instruction block and are replaced by this record. After an independent review, the instruction block, the output format and the example were revised: partial topic matches are defined, the "Requirements touched" line is dropped, the reasons after "Not confirmed" have set wording, the "today not given" rule is in the instruction block, and statements with no recorded requirement are listed under For confirmation. This pass applied the revised instruction block to the four inputs from the example, line by line. It was not blind and it was not a fresh independent run: the model that ran it is the one that made the revisions, it had the earlier register in front of it, and it changed only the lines the revisions affect. It did not write the original template.

## Inputs used

The four inputs in example.md under "The inputs": settings, recorded requirements, source items and previous register.

## What came out

```
DESIGN ASSUMPTION CHANGE REGISTER: Quay Road pump station upgrade, design basis DB-01 revision C

For: the Project engineer. Prepared: 2026-11-10, from 6 recorded requirements, 6 source items, 1 previous register row and the settings.
Column check: all headers matched.
Changes: 4. Conflicts: 1. Previous items carried: 1. Restatements: 1. Statements with no recorded requirement: 1. Set aside: 0.

CHANGES

C3 R01 Design life: recorded 50 years (DB-01 rev C, 2.1), recorded status Confirmed. Stated 60 years. Difference: +10 years.
  Source: S2, 2026-10-20, Workshop note, Project engineer (workshop 3 notes): "asked for a 60-year design life".
  Standing: Discussed only.
  Client confirmation: Not confirmed. Discussed only: a discussion is not an approval.
  Technical basis: Not confirmed.

C4 R03 Standby generator autonomy: recorded 8 hours (DB-01 rev C, 4.2), recorded status Confirmed. Stated 12 hours. Difference: +4 hours.
  Source: S3, 2026-10-27, Client instruction, Client project owner: "For now, assume 12 hours of generator autonomy".
  Standing: Provisional assumption.
  Client confirmation: Not confirmed. Provisional assumption: a value to work with for now, not a value to be used.
  Technical basis: Not confirmed.

C5 R04 Control room floor loading: recorded 5 kPa (DB-01 rev C, 5.3), recorded status Confirmed. Stated 7.5 kPa. Difference: +2.5 kPa.
  Source: S5, 2026-11-05, Client instruction, Client project owner: "Control room floor loading is now 7.5 kPa".
  Standing: Instructed; the sender is on the confirmer list.
  Client confirmation: Confirmed by Client project owner (S5).
  Technical basis: Confirmed (S6, 2026-11-09, Responsible engineer): "Technical basis for R04 at 7.5 kPa confirmed".

C6 R05 Design flood level: recorded 4.20 m (DB-01 rev C, 6.1), recorded status Confirmed. Stated 4.65 m. Difference: +0.45 m.
  Source: S5, 2026-11-05, Client instruction, Client project owner: "Design flood level is to be 4.65 m".
  Standing: Instructed; the sender is on the confirmer list.
  Client confirmation: Confirmed by Client project owner (S5).
  Technical basis: Not confirmed.

CONFLICTS

C2 R02 Peak design flow: recorded 120 L/s (DB-01 rev C, 3.1), recorded status Confirmed. 2 different values are stated. None is chosen.
  S1, 2026-10-14, Client instruction, Client project owner: 150 L/s ("design to a peak flow of 150 L/s"). Standing: Instructed; the sender is on the confirmer list. Difference from recorded: +30 L/s.
  S4, 2026-11-03, Client instruction, Client technical representative: 140 L/s ("use 140 L/s for peak flow"). Standing: Instructed; the sender is NOT on the confirmer list. Difference from recorded: +20 L/s.
  Difference between the stated values: 10 L/s.
  Client confirmation: Not settled until the Client project owner says which value stands.
  Technical basis: Not confirmed.

PREVIOUS ITEMS CARRIED

C1 R06 Boundary noise limit: recorded 45 dB(A) (DB-01 rev C, 7.4), recorded status Provisional. Previous register states 40 dB(A) (status Open, source W2, which is not among the supplied source items). Difference: -5 dB(A).
  New source: S2, 2026-10-20, Workshop note, Project engineer (workshop 3 notes): "Boundary noise limit may be tightened to 40 dB(A)". It states the same value, so it is added and no new item is opened.
  Standing: Discussed only.
  Client confirmation: Not confirmed. Discussed only: a discussion is not an approval.
  Technical basis: Not confirmed.

RESTATEMENTS

R04 Control room floor loading: S2, 2026-10-20, Workshop note, Project engineer (workshop 3 notes): "Control room floor loading of 5 kPa to stay as is". This is the recorded value, so it is not a competing value. See C5 where the same requirement has a change.

STATEMENTS WITH NO RECORDED REQUIREMENT

N1 S5, 2026-11-05, Client instruction, Client project owner: "add a requirement for a second tanker access road". No recorded requirement matches. It is shown as stated and has not been added to anything. Standing: Instructed; the sender is on the confirmer list.

SET ASIDE

None.

FOR CONFIRMATION

Whether any other requirement depends on these changes is for the Responsible engineer to say. This register does not assess it.

The Responsible engineer to confirm the technical basis: C1 (R06), C2 (R02), C3 (R01), C4 (R03), C6 (R05).
The Client project owner to confirm the changed requirement: C1 (R06), C2 (R02; which value stands), C3 (R01), C4 (R03).
Already confirmed on both sides: C5 (R04).
Statements with no recorded requirement: N1. Whether any enters the design basis is for the people the firm names to decide.

Draft for the Project engineer. No design basis, requirement or record has been changed, no technical consequence has been assessed, and nothing has been sent.
```

## What was observed

- Every part of the output format was produced, in the right order. All headers matched, no id repeated and no source type was unknown.
- The result matches the earlier register on every item: the same numbers (C1 to C6, N1), four changes, one conflict, one carried item, one restatement, one statement with no recorded requirement and nothing set aside; the same differences (+10 years, +4 hours, +2.5 kPa, +0.45 m, +30, +20 and 10 L/s, -5 dB(A)); the same standing for each; the same confirmations. The conflict over peak flow shows both values and neither is chosen.
- Differences from the earlier record, all from the revisions: the "Requirements touched" line is gone; each reason after "Not confirmed" uses the set wording; the quote for C1 now carries the requirement name ("Boundary noise limit may be tightened to 40 dB(A)"); For confirmation has a line for N1.
- The topic matches in the sources ("peak flow", "generator autonomy", "design life") each have all their words in one recorded topic, so each matched one requirement under the revised rule.
- The previous register cites source W2, which is not among the supplied source items; it was carried as written with a note that it is not among the supplied items. The zero-count closed-items sentence was left out. No fact appears in the output that is not in the inputs.
- The example's register is this output, so example and record agree by construction. That agreement is not an independent check.

### Ambiguities and shortcomings that remain

- How short a quote should be is still a judgement ("the shortest stretch that carries the requirement and the value"); two correct runs will quote slightly differently, and the reviewer checklist cannot check a quote's length.
- The wording of the reasons is now set for confirmations of Discussed only, Provisional assumption, an unlisted sender and a different value; a case outside those has no set wording.
- A blind re-run by a model that has not seen the example would be stronger evidence than this pass.
- The template's acceptance tests still say "None has been run"; this single trial is not a run of them.
- This was one pass by one model on one example, not blind to the example. It shows the instructions can be followed to the published result; it does not show how the template behaves on real project material, or in another AI product, and it is not a test for a client.
