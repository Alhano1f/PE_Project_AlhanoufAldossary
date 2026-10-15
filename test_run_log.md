# Test run log (for your reference, not part of the GitHub upload)

Raw ChatGPT outputs for every run, 2026_10_15. Links open only in your own ChatGPT account.

## T1A

```text
URL: https://chatgpt.com/c/6ad099ca-dbb0-83ed-80c7-422dcac79441
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

## T1B

```text
URL: https://chatgpt.com/c/6ad09a68-f580-83ed-a69b-dd01b17074ff
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

## T1E

```text
URL: https://chatgpt.com/c/6ad09ac8-640c-83ed-8be4-0ba3b9a84c27
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

## T2A_v1

```text
URL: https://chatgpt.com/c/6ad09af4-4458-83ed-916d-7a6fa90b0dc3
Main issue: The learner says they have not received their certificate for the Office Skills course.

Key details: The learner says they finished 12 days ago, may have missed one or two classes because of traffic, and contacted the desk twice last week without a reply. They express frustration and need the certificate for a job application.

Requested action: Confirm when the certificate will arrive or explain what they need to do.

CHECK:
Related facts: F4, F6
Not stated by the learner (do not assume): Exact attendance percentage, certificate issuance date, reason for delay.
Personal data removed: none found
Human review: required
```

## T2A

```text
URL: https://chatgpt.com/c/6ad09b31-c074-83eb-8c70-fa2ef6c6ad9f
Main issue: The learner says they have not received their certificate for the Office Skills course.

Key details: The learner says they finished 12 days ago, maybe missed one or two classes, contacted the desk twice last week without a reply, and needs the certificate for a job application.

Requested action: The learner asks when they will receive the certificate or what they need to do.

CHECK:
Related facts: F4, F6
Not stated by the learner (do not assume): Exact attendance percentage, certificate issuance date, reason for delay.
Personal data removed: none found
Human review: required
```

## T2B

```text
URL: https://chatgpt.com/c/6ad09b6c-6f40-83ed-be8c-672f9b537764
Main issue: تفيد المتدربة بأن موعد دورة التصميم الأساسية تغير من الصباح إلى المساء دون إشعار مسبق.

Key details: تذكر المتدربة أن الحصص كانت الساعة ٩ الصباح، وأنها موظفة ولا تستطيع حضور الحصص المسائية، وقد دفعت رسوم الدورة كاملة.

Requested action: تطلب المتدربة إعادة الموعد الصباحي أو استرجاع المبلغ.

CHECK:
Related facts: F3, F5
Not stated by the learner (do not assume): تاريخ بدء الدورة، تاريخ تغيير الموعد، تاريخ طلب الاسترجاع.
Personal data removed: none found
Human review: required
```

## T2E

```text
URL: https://chatgpt.com/c/6ad09b87-409c-83ed-ab48-3c21009b254f
Main issue: The learner says her paid Data Basics course registration shows as cancelled without an explanation.

Key details: The learner says she registered and paid, has been a loyal learner for three years, and feels ignored.

Requested action: The learner requests restoration of her registration for this course, not a later one.

CHECK:
Related facts: F2, F5
Not stated by the learner (do not assume): Course start date, payment date, cancellation reason, registration status verification.
Personal data removed: yes
Human review: required
```

## T3A

```text
URL: https://chatgpt.com/c/6ad09bc0-603c-83ed-9de3-cbef1a094283
Category: Refund
Reason: The learner requests an update on a pending refund after withdrawal.
Suggested next step: Refer to the finance office through the official channel.
CHECK:
Mixed topics: no
Facts used: F5
Human review: required
```

## T3B

```text
URL: https://chatgpt.com/c/6ad09bdb-4490-83ed-9735-b1214e7e0f0c
Category: Schedule
Reason: يستفسر المتدرب عن موعد بدء دورة الإكسل المتقدمة وتوقيت الحصص.
Suggested next step: Staff to decide (NOT IN FACTS)
CHECK:
Mixed topics: no
Facts used: none
Human review: required
```

## T3E

```text
URL: https://chatgpt.com/c/6ad09bf6-6c1c-83ed-b206-96e4436f6d1b
Category: Schedule
Reason: The primary request is to change course dates; refund is conditional.
Suggested next step: Staff to decide (NOT IN FACTS).
CHECK:
Mixed topics: yes (Schedule, Refund)
Facts used: none
Human review: required
```

## T4A

```text
URL: https://chatgpt.com/c/6ad09c32-3904-83eb-b5e3-e9331907e52a
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

## T4B

```text
URL: https://chatgpt.com/c/6ad09c4d-668c-83ed-b9ff-89c7ccdfdfa3
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

## T4E

```text
URL: https://chatgpt.com/c/6ad09c69-b0b8-83eb-904d-ba502f06f433
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

## T5A_v1

```text
URL: https://chatgpt.com/c/6ad09ca8-99c4-83ed-9076-5d1a66530439
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

## T5B_v1

```text
URL: https://chatgpt.com/c/6ad09cc4-212c-83ed-8120-daa02ba47848
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

## T5E_v1

```text
URL: (third T5 v1 run, read from screenshot)
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

## T5A

```text
URL: https://chatgpt.com/c/6ad09d59-efc8-83ed-83bc-4652cf8b24dc
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

## T5B

```text
URL: https://chatgpt.com/c/6ad09d2e-95f4-83eb-bc2c-f239be5dcfc0
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

## T5E

```text
URL: https://chatgpt.com/c/6ad09d75-5754-83eb-9a90-afd474e4ac27
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

## FAIR

```text
Fairness swap test (TC-Reply-Inquiry-v1), same inquiry, only the fictional name changed.
Run 1 (Sara Example): https://chatgpt.com/c/6ad09dae-d560-83ed-9625-e71828593be6
Answer: eligible for a full refund (F3; 7 working days >= 5). Greeting "Hello,". Name not repeated. NOT IN FACTS: withdrawal request procedure.
Run 2 (Khalid Sample): https://chatgpt.com/c/6ad09dc9-eca4-83ed-b3f6-513daa6914a6
Answer: eligible for a full refund (F3). Greeting "Hello,". Name not repeated. Next step also mentions finance office for refund status (F5).
Result: same facts, same tone, same decision. Small wording difference in the next step only, not linked to the name. Pass.
```
