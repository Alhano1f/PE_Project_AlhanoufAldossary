# Library Index — TC Prompt Library

**Desk:** Learner Support Desk at a Training Center (Path B · Scenario B1 · prefix TC)
**Owner:** Alhanouf Aldossary · **Last updated:** 2026_10_15 · **Tested with:** ChatGPT (web), fresh chat per run

## Templates

| # | Template file | Task | Variables | Output format | Version | Test date | Facts | Status |
|---|---|---|---|---|---|---|---|---|
| 1 | `templates/TC-Reply-Inquiry-v1_2026_10_15.md` | Answer a learner's question | `[INQUIRY]` `[TC_FACTS]` `[LANGUAGE]` `[TONE]` `[MAX_WORDS]` | Greeting · Answer · Next step · Closing · CHECK | v1 | 2026_10_15 | TC-Facts-v1 | Approved (5/6/5) |
| 2 | `templates/TC-Summarize-Complaint-v2_2026_10_15.md` | Condense a learner's complaint | `[COMPLAINT]` `[TC_FACTS]` `[LANGUAGE]` `[MAX_WORDS]` | Main issue · Key details · Requested action · CHECK | v2 | 2026_10_15 | TC-Facts-v1 | Approved (5/6/5) |
| 3 | `templates/TC-Classify-Requests-v1_2026_10_15.md` | Sort incoming requests | `[REQUEST]` `[CATEGORIES]` `[TC_FACTS]` `[LANGUAGE]` | Category · Reason · Suggested next step · CHECK | v1 | 2026_10_15 | TC-Facts-v1 | Approved (5/6/5) |
| 4 | `templates/TC-Soften-Staff-Draft-v1_2026_10_15.md` | Soften a staff draft | `[STAFF_DRAFT]` `[TC_FACTS]` `[LANGUAGE]` `[TONE]` `[MAX_WORDS]` | Rewritten message · CHECK | v1 | 2026_10_15 | TC-Facts-v1 | Approved (5/6/5) |
| 5 | `templates/TC-Mask-Learner-Details-v2_2026_10_15.md` | Hide learner details | `[MESSAGE]` `[LANGUAGE]` | Masked message · Masking CHECK | v2 | 2026_10_15 | not needed | Approved (5/6/5) |

Scores are Prompt /5 · Template /6 · Output /5. Evidence and screenshots: `Test_Results_Report.pdf`.

## Shared blocks and rules

| File | What it is | Version | Owner |
|---|---|---|---|
| `blocks/TC-Facts-v1_2026_10_15.md` | The 7 Training Center facts (F1–F7). The only source of policy statements. | v1 | Alhanouf Aldossary |
| `rules/TC-Rules-v1_2026_10_15.md` | Five yes/no verification and responsible-use rules (facts, privacy, no invented commitments, fairness, human review). | v1 | Alhanouf Aldossary |

## The five `[LANGUAGE]` values (same in every template)

| Value | Meaning |
|---|---|
| Arabic | Answer in Arabic only |
| English | Answer in English only |
| Automated (default) | Reply in the main language of the input |
| Bilingual | Two separate versions: Arabic, then English |
| Mixed | One reply that merges Arabic and English |

## Archive

| File | Why it was replaced |
|---|---|
| `_archive/TC-Summarize-Complaint-v1_2026_10_15.md` | Output went over the 60-word limit (66 words). Replaced by v2. |
| `_archive/TC-Mask-Learner-Details-v1_2026_10_15.md` | Masking CHECK came out in English for an Arabic input with `[LANGUAGE]` = Automated. Replaced by v2. |

## Change log

| Date | Change | By |
|---|---|---|
| 2026_10_15 | Library created: Facts block, rules file, five templates (v1). | Alhanouf Aldossary |
| 2026_10_15 | All templates tested in ChatGPT (2 fills + 1 edge case each, fresh chats). | Alhanouf Aldossary |
| 2026_10_15 | TC-Summarize-Complaint v1 → v2 (word limit) and TC-Mask-Learner-Details v1 → v2 (language of CHECK); both retested and approved. | Alhanouf Aldossary |
| 2026_10_15 | Fairness swap test on TC-Reply-Inquiry: pass. | Alhanouf Aldossary |
