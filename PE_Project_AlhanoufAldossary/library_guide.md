# Library Guide — How to use the TC Prompt Library

**Owner:** Alhanouf Aldossary · **Version:** v1 · **Date:** 2026_10_15

This library helps staff at the Learner Support Desk of a Training Center draft text with an AI tool. The AI only drafts. **A person checks and approves every result before it is sent.**

## What is in the library

| Folder / file | Contents |
|---|---|
| `library_index.md` | The list of the 5 templates, their status and versions |
| `templates/` | The 5 approved templates (one `.md` file each) |
| `blocks/TC-Facts-v1_2026_10_15.md` | The 7 approved facts (F1–F7) |
| `rules/TC-Rules-v1_2026_10_15.md` | The 5 verification and responsible-use rules |
| `Test_Results_Report.pdf` | Scores and screenshots that prove each template works |
| `_archive/` | Old versions, for reference only. Do not use them. |

## How to use a template (7 steps)

1. **Pick the template** for your task in `library_index.md`. Use only templates with status **Approved**.
2. **Mask first.** If the learner's message has names, phone numbers or emails, run `TC-Mask-Learner-Details` first and use the masked text. Never paste ID numbers, passwords or bank details into any AI tool.
3. **Copy the whole box** under "Template" in the file, including the RULES block. Do not delete or edit any rule.
4. **Fill the variables** in `[UPPER_CASE]`:
   - Paste the learner text (masked) into the input variable, between the `---` lines.
   - Paste the full Facts block from `blocks/` into `[TC_FACTS]`, unchanged.
   - Choose `[LANGUAGE]`, `[TONE]` and `[MAX_WORDS]` from the allowed values in the template's table. If you leave one empty, the default is used.
5. **Run it in a fresh chat** of an approved AI tool, so older chats do not affect the result.
6. **Check the output** with the CHECK section and the 5 rules in `rules/`:
   - Every fact matches the current Facts block (F1–F7).
   - Anything marked `NOT IN FACTS` is **not answered by guessing**. Find the answer through the official channel, or leave it for a person to decide.
   - No promises, prices, dates, refund statuses or links were invented.
   - No personal data was repeated or asked for.
   - The reply would be the same for any learner.
7. **Send it for human approval.** A staff member reads the draft, fixes anything wrong and only then sends it.

## When something goes wrong

- The AI states a fact that is not in the Facts block → do not use the output; report it to the owner so the rule can be tightened.
- A policy changes → the owner updates the Facts block to a new version (v2) and retests the templates. Never edit facts inside a template.
- You need a new template → copy an approved one, change the task, variables and format, test it with two fills and one edge case, and add it to the index.

## Who owns each file

| File | Owner |
|---|---|
| All templates, the Facts block, the rules file, this guide and the index | Alhanouf Aldossary |
