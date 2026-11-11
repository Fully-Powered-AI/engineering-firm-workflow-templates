# Design assumption change register: an invented example

*Illustrative example with invented data.* The firm, the project, the people and every figure below are invented. The firm is an invented engineering firm, called the Firm here, and the project is the invented Quay Road pump station upgrade. Roles stand in for people. The project engineer asks for the register on 10 November 2026. First come the inputs the project engineer supplied, in full, then the register the capability returned.

## The inputs

### 1. Settings (typed by the project engineer)

```
Project: Quay Road pump station upgrade
Design basis: DB-01, revision C
Today: 2026-11-10
Project engineer (runs this): Project engineer
Responsible engineer (confirms the technical basis): Responsible engineer
Client confirmers (confirm changed requirements): Client project owner
```

### 2. Recorded requirements (from DB-01 revision C)

```
req_id,topic,value,unit,status,source_ref
R01,Design life,50,years,Confirmed,2.1
R02,Peak design flow,120,L/s,Confirmed,3.1
R03,Standby generator autonomy,8,hours,Confirmed,4.2
R04,Control room floor loading,5,kPa,Confirmed,5.3
R05,Design flood level,4.20,m,Confirmed,6.1
R06,Boundary noise limit,45,dB(A),Provisional,7.4
```

### 3. Source items

```
source_id,date,source_type,from,text
S1,2026-10-14,Client instruction,Client project owner,"Please design to a peak flow of 150 L/s instead of 120 L/s, following the revised catchment growth figures."
S2,2026-10-20,Workshop note,Project engineer (workshop 3 notes),"Client operations manager asked for a 60-year design life; to go back to the project owner. Boundary noise limit may be tightened to 40 dB(A), council letter awaited. Control room floor loading of 5 kPa to stay as is."
S3,2026-10-27,Client instruction,Client project owner,"For now, assume 12 hours of generator autonomy until the utility sends its outage records."
S4,2026-11-03,Client instruction,Client technical representative,"Please use 140 L/s for peak flow, from our own modelling."
S5,2026-11-05,Client instruction,Client project owner,"Control room floor loading is now 7.5 kPa for the new switchboard. Design flood level is to be 4.65 m, per the council's updated map. Please also add a requirement for a second tanker access road."
S6,2026-11-09,Engineer confirmation,Responsible engineer,"Technical basis for R04 at 7.5 kPa confirmed against the switchboard supplier's data."
```

### 4. Previous register

```
change_id,req_id,to_value,unit,status,source_ids
C1,R06,40,dB(A),Open,W2
```

## The register

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
