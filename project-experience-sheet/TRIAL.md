# Project experience sheet: trial on the invented example

- **Product:** Claude, run in Claude Code

Model: Claude Sonnet 5.5 (model ID claude-sonnet-5-5).
Date: 2026-11-10.

The inputs were the invented example in `public/example.md` (the request and settings, a fourteen-row statement register and a five-row permissions register). No client data was used. The assistant followed the fenced instruction block and the output format in `member/template.md`. It did not execute or install anything.

One disclosure about how the trial was run: the example file was printed in one piece, so the first part of its published output (the header and the start of the sheet) was visible before the run. The full output below was still produced from the instructions and the inputs, step by step, and the comparison was made afterwards.

## What came out

```
PROJECT EXPERIENCE SHEET: DRAFT FOR VERIFICATION
Project: a pedestrian footbridge replacement for a regional parks authority
Prepared for: Proposal lead   Date: 10 November 2026
For: Response to City M's request for qualifications, rehabilitation of the
Riverside Path Bridge
Status: Draft. Not verified by the Principal-in-charge. Not approved by
Marketing lead. Not to be put in a proposal or shared outside the firm
until both have signed off.
Built from: statement register (14 rows, 12 marked yes); permissions
register (5 rows). Nothing else.

THE SHEET (about 157 words; limit 250, the default)
Footbridge replacement for a regional parks authority [P1]
Role: Firm E was appointed by a regional parks authority as lead consultant
for the replacement of a pedestrian footbridge, under a services agreement
dated 14 March 2021. [P1]
Project: The replacement footbridge is approximately 42 metres in length. [P2]
A certificate of substantial completion was issued on 22 June 2022. [P9]
Scope performed by Firm E:
- Structural design of the new deck and abutments. [P3]
- Construction drawings and specifications for the structure. [P4]
- Review of the contractor's shop drawings for the structure. [P5]
- Site visits during construction, as listed in Schedule A. [P6]
Performed by others on the project:
- Landscape and lighting design, by a partner firm (not named). [P7]
- Geotechnical investigation, by a partner firm (not named). [P8]
Supporting records: services agreement and Schedule A (14 March 2021);
subconsultant agreements (20 and 22 March 2021); certificate of substantial
completion (22 June 2022).
Image: Photograph IMG_0412, the completed bridge. Credit line "Photo: Firm E";
for use in submissions only. [K3]

FIT TO THIS REQUEST
R1 A pedestrian bridge replacement or rehabilitation project: P1, P2.
R2 Completed within the last seven years: P9.
R3 The consultant's role and the scope it performed: P1, P3, P4, P5, P6.
R4 Experience with a historic or heritage-designated structure: No matching
record.
The Principal-in-charge and the proposal lead decide whether a matching row
meets the requirement.

FOR THE PROJECT PRINCIPAL: VERIFY THE FIRM'S CONTRIBUTION
P1 Firm E was appointed ... as lead consultant for the replacement of a
   pedestrian footbridge. Source: Services agreement, clause 2, 14 Mar 2021.
   Firm. Confirmed / Changed to: ____ / Remove
P2 The replacement footbridge is approximately 42 metres in length.
   Source: Services agreement, Schedule A, 14 Mar 2021.
   Project fact. Confirmed / Changed to: ____ / Remove
P3 Structural design of the new deck and abutments. Source: Services
   agreement, Schedule A, 14 Mar 2021. Firm. Confirmed / Changed to: ____ / Remove
P4 Construction drawings and specifications for the structure. Source:
   Services agreement, Schedule A, 14 Mar 2021. Firm. Confirmed / Changed to: ____ / Remove
P5 Review of the contractor's shop drawings for the structure. Source:
   Services agreement, Schedule A, 14 Mar 2021. Firm. Confirmed / Changed to: ____ / Remove
P6 Site visits during construction, as listed in Schedule A. Source:
   Services agreement, Schedule A, 14 Mar 2021. Firm. Confirmed / Changed to: ____ / Remove
P7 Landscape and lighting design, by a partner firm (not named). Source:
   Subconsultant agreement, 20 Mar 2021. Partner's work, not the firm's.
   Confirmed / Changed to: ____ / Remove
P8 Geotechnical investigation, by a partner firm (not named). Source:
   Subconsultant agreement, 22 Mar 2021. Partner's work, not the firm's.
   Confirmed / Changed to: ____ / Remove
P9 A certificate of substantial completion was issued on 22 June 2022.
   Source: Certificate of substantial completion, 22 Jun 2022.
   Project fact. Confirmed / Changed to: ____ / Remove

FOR MARKETING: NAMES, IMAGES AND CLAIMS
Permissions
K1 Name of the parks authority: pending; no grantor or date. The sheet uses a
   plain description. Conditions: the authority's communications office is
   reviewing. Approved / Changed to: ____ / Remove
K2 Name and location of the project: not asked. The sheet uses a plain
   description. Conditions: none. Approved / Changed to: ____ / Remove
K3 Photograph IMG_0412, the completed bridge: granted, authority project
   manager, 3 Mar 2023. The sheet uses it. Conditions: credit line
   "Photo: Firm E"; for use in submissions only.
   Approved / Changed to: ____ / Remove
K4 Names of Firm Q and Firm G: not asked. The sheet uses a plain description
   ("a partner firm (not named)"). Conditions: none.
   Approved / Changed to: ____ / Remove
K5 Photograph IMG_0388, the bridge under construction: refused, Contractor C,
   6 Mar 2023. The sheet uses nothing. Conditions: shows the contractor's crew.
   Approved / Changed to: ____ / Remove
Claim lines
P2 size: The replacement footbridge is approximately 42 metres in length.
   Approved / Changed to: ____ / Remove
P9 completion: A certificate of substantial completion was issued on 22 June 2022.
   Approved / Changed to: ____ / Remove

NOT USED
- P10 (performance): a performance statement; never used. Its source is also
  not an approved project record and it does not say who did the work.
- P11 (performance): a statement of what the design is designed for; never used
  whatever its marking.
- P12 (recognition): marked ask, and its source is a photograph of the
  certificate, not the recognition record itself.
- P13 (scope): who performed the work is unclear; not placed.
- P14 (size): marked no.
- K5 (image): refused.

FOR PEOPLE TO DECIDE
- Principal-in-charge: who performed the inspection of the existing bridge
  (P13)? Place it only once it is clear.
- Principal-in-charge and engineers: P11 is a design-basis statement marked yes
  but is performance, so it is left off. Whether anything on that point goes
  in the proposal is theirs to decide.
- Marketing lead: whether to ask the authority for its name (K1, K2) and the
  partners for theirs (K4); whether the award row (P12) can be asked about and
  confirmed from the award itself.
- Marketing lead: the photograph's condition "for use in submissions only"
  against this use.
- Proposal lead: R4 has no matching record; whether this project is the right
  example for the request.
```

## What was observed

Every required part of the output format was produced. Every tag is a row in one of the two registers, every used row (P1 to P9) is on the principal's list, and no performance statement, name, location or partner name appears. The counted length was 157 words, within the 250 default. No stop condition applied: the headers matched, one project was described, and a request and both registers were supplied.

Where the instructions left a choice and a guess was needed:

- **Two things called "Project".** The format uses "Project:" for the header line (plain description) and again for the sheet's size-and-completion line. This is easy to misread; nothing says they differ other than position.
- **The title line's tag.** The format shows a tag after the title but does not say which row it rests on. P1 was used, as it is the only row that describes the project as a footbridge replacement.
- **Tags on the "Project:" line.** The format shows one tag at the end of the line, but the line holds two rows. Each statement was tagged separately.
- **Supporting records and partner names.** Two source documents are titled with the partners' names ("Subconsultant agreement with Firm Q" and "with Firm G"). Listing them as written would name the partners without a granted permission. The sources were listed as "subconsultant agreements" with their dates. The template does not say to do this.
- **Not used, for a permissions row.** The format gives "[ID] (category)" for a row not used, but a permissions row has no category. K5 was listed with "(image)". Step 5 says to list a refused row under Not used, so this was needed.
- **Reasons for a performance row.** The rule forbids repeating a performance row's wording, so the reason for P10 and P11 had to be kept vague. This worked, but the P10 reason also notes the missing "performed by", which goes beyond the rule it cites.
- **Which size, completion and recognition rows count as claims.** Only P2 (size) and P9 (completion) are claim lines. The role row P1 is not listed for marketing, as the template specifies, though it is the line a reader might most expect to be checked.
- **Unclear who made the decision on a design-basis row.** The row is marked yes but is performance; the template says to never use it, and "For people to decide" is the place to say so. It was unclear whether to name P11's content there. It was described without its figure.
- **The range of the date check.** R2 asks for "within the last seven years". The template says not to judge whether the requirement is met, so P9 was listed without comment.
- **Date format.** The format asks for "D Month YYYY", and the settings give the date in that form, so no conversion was needed.

Facts not in the inputs: none were added to the sheet. The statement "Conditions: none" for K2 and K4 reflects empty condition cells in the register. The wording "the authority's communications office is reviewing" is copied from K1's conditions column.

Differences from the published example output, compared after the run (the sheet's opening lines were seen before the run, so the match there is not independent):

- The sheet matches the example in substance. The differences are small: the Project line carries the same two tags but breaks after [P2] here and in the middle of the line in the example (lines 31 to 32); the supporting-records dates read "20 and 22 March 2021" here and "March 2021" in the example; and the image line is worded a little differently ("Photograph IMG_0412" here, "IMG_0412" and "Conditions as written" in the example). The example's count of 157 words is correct; a recount of this run's sheet gives 158.
- The principal's list: the example shortens the lines (P1 as "Firm E appointed as lead consultant under the agreement of 14 March 2021", P9 as "Certificate of substantial completion issued on 22 June 2022", P2 as "The footbridge ..."). The format says the list shows the line as it appears on the sheet, so this run kept the sheet's wording. The example also drops "(not named)" from the P7 and P8 lines.
- The example names Firm Q and Firm G in the principal's list ("subconsultant agreement with Firm Q"). This run left the partners' names out everywhere, since K4 is not granted. The template does not say whether an internal list may name them.
- Not used: the example gives P12 as "marked ask" only; this run also said its source was a photograph of the certificate rather than the recognition itself. That second reason is doubtful. A photograph of an award certificate may count as "the recognition itself", and the template does not say. The example's reason is safer.
- Not used: the example lists K5 without a category, as this run did in effect; this run wrote "(image)".
- For people to decide: the example adds that P11's marking in the register may need correcting. This run did not say so, and it is a useful point. The example also asks who approves P12; this run folded that into a marketing item.
- The example adds a closing sentence ("The sheet is built from registers the firm supplied ...") that the output format does not contain. This run did not add it.

Facts in either output that are not in the inputs: none found. "Conditions: shows the contractor's crew" for K5 is copied from the conditions column in both.

Shortcomings of the trial: one run, one product, one set of invented inputs. The acceptance tests listed in the template (renamed headers, no yes row, two projects, an instruction hidden in a record, a tighter length limit and others) were not run. This trial shows the template can produce a complete sheet from clean inputs; it does not show how it handles messy ones.

## Edits after this run, not run again

The output and observations above are as recorded and describe the template and the example as they stood at the run. Afterward, small edits were made to the template and the example, and the template has not been run again on them:

- The output format's header line is now "Project described:", so it no longer shares a name with the sheet's "Project:" line; the sheet's Project line now shows a tag after each statement; the title's tag rests on the row that describes the project; and a refused permissions row in Not used takes "image" or "name" in place of a category.
- Step 5 and the pasted instructions now say to describe a source document without any name that lacks a granted row, on the sheet and in both lists, and the principal's list now copies the sheet's line exactly. The example follows both rules.
- A recognition row counts only if its source is the award letter, or a photo or scan of the award document; a newsletter, web page or email does not.
- The pasted instructions now say to leave out personal details unrelated to the work. The role row stays off the marketing list by design; the principal verifies it.
- After the independent review, further small edits, also not run again: the example's principal's list now labels partner rows "Partner." (the format's own option) in place of "Partner's work, not the firm's."; its Supporting records line gives the two subconsultant agreement dates, so its sheet now counts 160 words; step 2 and the pasted instructions now say that a row that is both performance and unclear raises no question, and say what counts as an approved project record (an agreement, a schedule, a certificate or an issued report, or another record the requester says is approved); the pasted instructions' step 9 now also checks that no performance statement is on the sheet, and two over-long lines in the pasted block were re-wrapped. The recorded output above is unchanged and still shows the earlier wording ("Partner's work, not the firm's." and the 157-word count).
