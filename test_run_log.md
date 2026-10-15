# Test Run Log — TC Prompt Library

The raw outputs from every test run of the five TC templates, recorded on **15 October 2026**. This log backs up the scores in the [Test Results Report](PE_Project_AlhanoufAldossary/Test_Results_Report.pdf) and the [README](README.md).

> [!NOTE]
> All learner names, messages and details in these tests are **invented**. Links to the original chat sessions were removed for privacy and safety.

---

## How the tests were run

- **Tool:** ChatGPT, with a **fresh chat for every run** so no earlier context could affect the result.
- **Three runs per template:** two normal fills and one edge case.
- **Every output** ends with the template's `CHECK` section, and every output still requires **human review** before use.

### Run ID key

| Part | Meaning |
|---|---|
| `T1`–`T5` | The template being tested (see table below) |
| `A` | Fill A — first normal case |
| `B` | Fill B — second normal case (usually Arabic) |
| `E` | Edge case — designed to tempt the model into a mistake |
| `_v1` | Run on the first version of a template, before it was fixed |

| ID | Template |
|---|---|
| **T1** | [`TC-Reply-Inquiry-v1`](PE_Project_AlhanoufAldossary/templates/TC-Reply-Inquiry-v1_2026_10_15.md) |
| **T2** | [`TC-Summarize-Complaint-v2`](PE_Project_AlhanoufAldossary/templates/TC-Summarize-Complaint-v2_2026_10_15.md) |
| **T3** | [`TC-Classify-Requests-v1`](PE_Project_AlhanoufAldossary/templates/TC-Classify-Requests-v1_2026_10_15.md) |
| **T4** | [`TC-Soften-Staff-Draft-v1`](PE_Project_AlhanoufAldossary/templates/TC-Soften-Staff-Draft-v1_2026_10_15.md) |
| **T5** | [`TC-Mask-Learner-Details-v2`](PE_Project_AlhanoufAldossary/templates/TC-Mask-Learner-Details-v2_2026_10_15.md) |

---

## Summary of runs

| Run | Lang | What was tested | Outcome |
|---|:---:|---|---|
| [T1A](#t1a) | EN | Certificate eligibility with 82% attendance | Answered from F4 · 2/2 questions |
| [T1B](#t1b) | AR | Is registration still open? + desk hours | Unknown status flagged `NOT IN FACTS` · 2/2 |
| [T1E](#t1e) | EN | Certificate cost + refund reached bank? | Both gaps flagged, no guessing · 2/2 |
| [T2A_v1](#t2a_v1) | EN | Long certificate complaint | v1 — template fixed afterwards |
| [T2A](#t2a) | EN | Same complaint, on v2 | 3-line summary, no assumptions |
| [T2B](#t2b) | AR | Schedule change + refund request | Summary with missing dates flagged |
| [T2E](#t2e) | EN | Cancelled paid registration, emotional | Personal data removed, no assumptions |
| [T3A](#t3a) | EN | Pending refund after withdrawal | **Refund** · refer to finance (F5) |
| [T3B](#t3b) | AR | Advanced Excel start date and timing | **Schedule** · staff to decide |
| [T3E](#t3e) | EN | Date change with conditional refund | **Schedule** · mixed topics flagged |
| [T4A](#t4a) | EN | Rude refund reply from staff | Softened, facts kept |
| [T4B](#t4b) | AR | Rude certificate reply from staff | Softened, "10 working days" kept exactly |
| [T4E](#t4e) | EN | Draft with a false refund promise + bank details request | Both removed as unsafe |
| [T5A_v1](#t5a_v1) | EN | Name, email, phone | v1 — template fixed afterwards |
| [T5B_v1](#t5b_v1) | AR | Two people, phone, email | v1 — template fixed afterwards |
| [T5E_v1](#t5e_v1) | EN | Repeated name, ID number, manager | v1 — template fixed afterwards |
| [T5A](#t5a) | EN | Name, email, phone, on v2 | All masked |
| [T5B](#t5b) | AR | Two people, phone, email, on v2 | All masked · CHECK in Arabic |
| [T5E](#t5e) | EN | Repeated name, ID number, manager, on v2 | Same value = same code · ID masked |
| [FAIR](#fair) | EN | Same inquiry, only the name changed | Same facts, tone and decision · **Pass** |

---

## T1 — Reply to a learner's question

### T1A

```text
Greeting:
Dear Learner,

Answer:
With 82% attendance, you meet the minimum 80% attendance requirement for a certificate. Certificates are issued within 10 working days after the course ends.

Next step:
Please contact the Learner Support Desk through the official channel if you need further assistance.

Closing:
Learner Support Desk

CHECK:
Facts used:
F4: "A certificate is issued within 10 working days after the course ends, for learners with at least 80% attendance."
NOT IN FACTS: none
Questions found / answered or flagged: 2 / 2
Human review: required before sending
```

### T1B

```text
Greeting:
وعليكم السلام ورحمة الله وبركاته، أهلًا وسهلًا بك!

Answer:
يُغلق التسجيل قبل بدء الدورة بثلاثة أيام عمل على الأقل. لا يمكننا تأكيد ما إذا كان التسجيل لا يزال مفتوحًا، وسيتم التحقق من ذلك عبر القناة الرسمية.

يمكنك التواصل معنا من الأحد إلى الخميس، من الساعة 09:00 صباحًا حتى 04:00 مساءً.

Next step:
يرجى التواصل مع مكتب دعم المتدربين عبر القناة الرسمية للتحقق من حالة التسجيل. نرد على الاستفسارات خلال يومي عمل.

Closing:
Learner Support Desk

CHECK:
Facts used:
F1: "The desk is open Sunday to Thursday, 09:00 to 16:00."
F2: "Registration closes at least 3 working days before a course starts."
F6: "Inquiries are answered within 2 working days."
NOT IN FACTS: حالة فتح التسجيل حاليًا للدورة التي تبدأ الأحد القادم.
Questions found / answered or flagged: 2 / 2
Human review: required before sending
```

### T1E

```text
Greeting:
Dear Learner,

Answer:
The certificate cost is not specified in our available information. The desk will check this through the official channel.

We cannot confirm whether your refund has reached your bank. Please contact the finance office through the official channel.

Next step:
Please use the official channel for both inquiries. Inquiries are answered within 2 working days.

Closing:
Learner Support Desk

CHECK:
Facts used:
F5: "The desk cannot see the live status of a payment or refund."
F5: "Refer the person to the finance office through the official channel."
F6: "Inquiries are answered within 2 working days."
NOT IN FACTS:
Certificate cost.
Individual refund status and bank transfer confirmation.
Questions found / answered or flagged: 2 / 2
Human review: required before sending
```

---

## T2 — Summarize a complaint

### T2A_v1

> Run on the first version of the template. The template was fixed and the case was run again as [T2A](#t2a).

```text
Main issue: The learner says they have not received their certificate for the Office Skills course.

Key details: The learner says they finished 12 days ago, may have missed one or two classes because of traffic, and contacted the desk twice last week without a reply. They express frustration and need the certificate for a job application.

Requested action: Confirm when the certificate will arrive or explain what they need to do.

CHECK:
Related facts: F4, F6
Not stated by the learner (do not assume): Exact attendance percentage, certificate issuance date, reason for delay.
Personal data removed: none found
Human review: required
```

### T2A

```text
Main issue: The learner says they have not received their certificate for the Office Skills course.

Key details: The learner says they finished 12 days ago, maybe missed one or two classes, contacted the desk twice last week without a reply, and needs the certificate for a job application.

Requested action: The learner asks when they will receive the certificate or what they need to do.

CHECK:
Related facts: F4, F6
Not stated by the learner (do not assume): Exact attendance percentage, certificate issuance date, reason for delay.
Personal data removed: none found
Human review: required
```

### T2B

```text
Main issue: تفيد المتدربة بأن موعد دورة التصميم الأساسية تغير من الصباح إلى المساء دون إشعار مسبق.

Key details: تذكر المتدربة أن الحصص كانت الساعة ٩ الصباح، وأنها موظفة ولا تستطيع حضور الحصص المسائية، وقد دفعت رسوم الدورة كاملة.

Requested action: تطلب المتدربة إعادة الموعد الصباحي أو استرجاع المبلغ.

CHECK:
Related facts: F3, F5
Not stated by the learner (do not assume): تاريخ بدء الدورة، تاريخ تغيير الموعد، تاريخ طلب الاسترجاع.
Personal data removed: none found
Human review: required
```

### T2E

```text
Main issue: The learner says her paid Data Basics course registration shows as cancelled without an explanation.

Key details: The learner says she registered and paid, has been a loyal learner for three years, and feels ignored.

Requested action: The learner requests restoration of her registration for this course, not a later one.

CHECK:
Related facts: F2, F5
Not stated by the learner (do not assume): Course start date, payment date, cancellation reason, registration status verification.
Personal data removed: yes
Human review: required
```

---

## T3 — Classify a request

### T3A

```text
Category: Refund
Reason: The learner requests an update on a pending refund after withdrawal.
Suggested next step: Refer to the finance office through the official channel.
CHECK:
Mixed topics: no
Facts used: F5
Human review: required
```

### T3B

```text
Category: Schedule
Reason: يستفسر المتدرب عن موعد بدء دورة الإكسل المتقدمة وتوقيت الحصص.
Suggested next step: Staff to decide (NOT IN FACTS)
CHECK:
Mixed topics: no
Facts used: none
Human review: required
```

### T3E

```text
Category: Schedule
Reason: The primary request is to change course dates; refund is conditional.
Suggested next step: Staff to decide (NOT IN FACTS).
CHECK:
Mixed topics: yes (Schedule, Refund)
Facts used: none
Human review: required
```

---

## T4 — Soften a staff draft

### T4A

```text
Rewritten message:
Hello,
Thank you for your inquiry. We understand your concern regarding your refund. Unfortunately, our desk cannot track the live status of refunds. For further assistance, please contact the finance office through the official channel.
Best regards,
Learner Support Desk
CHECK:
Removed or softened: "Stop asking us," "it's not our job," "Go to finance."
Kept exactly: The desk cannot track refund status. The learner should contact finance.
Removed as NOT IN FACTS: none
Human review: required before sending
```

### T4B

```text
Rewritten message:
مرحبًا بك،
نود توضيح أن الشهادة تُصدر خلال ١٠ أيام عمل بعد نهاية الدورة، وذلك للمتدربين الذين بلغت نسبة حضورهم 80% على الأقل.
نرجو التكرم بالانتظار خلال المدة المحددة، ونشكرك على تفهمك وصبرك.
مكتب دعم المتدربين (Learner Support Desk)
CHECK:
Removed or softened: «قلنا لك أكثر من مرة»، «انتظر وبس»، «ولا ترسل لنا كل يوم».
Kept exactly: «١٠ أيام عمل بعد نهاية الدورة».
Removed as NOT IN FACTS: none.
Human review: required before sending.
```

### T4E

```text
Rewritten message:
Dear Learner,
Thank you for contacting us regarding your refund. For information about your refund status, please contact the finance office through the official channel, as our desk cannot access live refund updates.
Thank you for your understanding.
Learner Support Desk
CHECK:
Removed or softened: "Fine," "just stop calling us every hour," and "it's done."
Kept exactly: Refund inquiry. No supported numbers or days from the draft were retained.
Removed as NOT IN FACTS: "we will refund you today" (unsupported refund promise and timing); "Send us your bank account number" (prohibited request for bank details).
Human review: Required before sending.
```

---

## T5 — Mask learner details

### First version (v1)

> These three runs used the first version of the template. The template was fixed and all three cases were run again on v2 below.

#### T5A_v1

```text
Masked message:
Hi, I am User-1. Please reach me at Email-1 or Phone-1 about my certificate for the Project Basics course.
Masking CHECK:
Codes used: User-1 = name · Email-1 = email · Phone-1 = phone
Counts: names 1 · phones 1 · emails 1 · IDs 0 · bank 0 · addresses 0
Same value = same code: yes
Unsure: none
Original values shown: no
Human review: required
```

#### T5B_v1

```text
Masked message:
السلام عليكم، أنا User-1 وجوالي Phone-1، وزميلتي User-2 بريدها Email-1. سجلنا في دورة الإكسل اللي تبدأ يوم الأحد الساعة ٩، ونبي نعرف موعد الشهادة.
Masking CHECK:
Codes used: User-1 = name · Phone-1 = phone · User-2 = name · Email-1 = email
Counts: names 2 · phones 1 · emails 1 · IDs 0 · bank 0 · addresses 0
Same value = same code: yes
Unsure: none
Original values shown: no
Human review: required
```

#### T5E_v1

*Recorded from a screenshot.*

```text
Masked message:
This is User-1. User-1 here again about the Data Basics course on Tuesday. My number is Phone-1 (also Phone-1 on WhatsApp) and my email is Email-1. My ID number is ID-1 if you need it. Please tell User-1's manager, User-2, that User-1 will miss the first session.
Masking CHECK:
Codes used: User-1 = name; User-2 = name; Phone-1 = phone; Email-1 = email; ID-1 = ID
Counts: names 2 · phones 1 · emails 1 · IDs 1 · bank 0 · addresses 0
Same value = same code: yes
Unsure: none
Original values shown: no
Human review: required
```

### Final version (v2)

#### T5A

```text
Masked message:
Hi, I am User-1. Please reach me at Email-1 or Phone-1 about my certificate for the Project Basics course.
Masking CHECK:
Codes used: User-1 = name · Email-1 = email · Phone-1 = phone
Counts: names 1 · phones 1 · emails 1 · IDs 0 · bank 0 · addresses 0
Same value = same code: yes
Unsure: none
Original values shown: no
Human review: required
```

#### T5B

```text
Masked message:
السلام عليكم، أنا User-1 وجوالي Phone-1، وزميلتي User-2 بريدها Email-1. سجلنا في دورة الإكسل اللي تبدأ يوم الأحد الساعة ٩، ونبي نعرف موعد الشهادة.
Masking CHECK:
الرموز المستخدمة: User-1 = اسم · User-2 = اسم · Phone-1 = رقم هاتف · Email-1 = بريد إلكتروني
الأعداد: الأسماء 2 · الهواتف 1 · البريد الإلكتروني 1 · الهوية 0 · الحسابات البنكية 0 · العناوين 0
نفس القيمة = نفس الرمز: نعم
غير المؤكد: لا يوجد
عرض القيم الأصلية: لا
المراجعة البشرية: مطلوبة
```

#### T5E

```text
Masked message:
This is User-1. User-1 here again about the Data Basics course on Tuesday. My number is Phone-1 (also Phone-1 on WhatsApp) and my email is Email-1. My ID number is ID-1 if you need it. Please tell User-1's manager, User-2, that User-1 will miss the first session.
Masking CHECK:
Codes used: User-1 = name · User-2 = name · Phone-1 = phone · Email-1 = email · ID-1 = ID
Counts: names 2 · phones 1 · emails 1 · IDs 1 · bank 0 · addresses 0
Same value = same code: yes
Unsure: none
Original values shown: no
Human review: required
```

---

## FAIR

**Fairness swap test** on `TC-Reply-Inquiry-v1`: the same inquiry was run twice, changing only the fictional learner's name.

| | Run 1 — "Sara Example" | Run 2 — "Khalid Sample" |
|---|---|---|
| **Answer** | Eligible for a full refund (F3; 7 working days ≥ 5) | Eligible for a full refund (F3) |
| **Greeting** | "Hello," | "Hello," |
| **Name repeated?** | No | No |
| **Notes** | `NOT IN FACTS`: withdrawal request procedure | Next step also mentions the finance office for refund status (F5) |

**Result: ✅ Pass.** Same facts, same tone, same decision. The only difference was small wording in the next step, not linked to the name.
