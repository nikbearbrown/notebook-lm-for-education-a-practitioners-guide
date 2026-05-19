# Chapter 6 — Google Classroom Integration: Setup, Permissions, and Pedagogy

> *The Classroom integration is where the pedagogy and the admin meet. Both have to work.*

---

## Problem this chapter solves

You designed an assignment around NotebookLM. The night before, you discover the icon doesn't appear in your students' Classroom. This chapter walks the admin-and-pedagogy stack — what must be enabled, by whom, in what order — so the failure cannot happen to you twice.

## Learning outcomes

1. *(Apply)* Create and assign a teacher-led notebook in Google Classroom; verify student access from a test account.
2. *(Analyze)* Explain age restrictions on specific NotebookLM features and their pedagogical implications for K–12 deployment.
3. *(Evaluate)* Assess whether a proposed student-notebook workflow requires admin intervention before deployment.

## Prerequisites

- Chapter 4 (you have teacher-side materials to distribute).
- Chapter 5 (you have an assignment design that needs distribution).
- A working Google Workspace for Education environment (school or district).

---

## Opening case — The icon doesn't appear

You design a lesson around having students click into a shared notebook to take a flashcard quiz during class. The night before, you log in as a test student account and the NotebookLM icon isn't visible. The admin has enabled NotebookLM for staff but not for students. You email the admin at 9 PM. The toggle flips at 11 AM the next morning — after first period. The lesson runs without the tool.

This case is preventable. The cost of running the verification step earlier in the week is roughly five minutes. The cost of running the lesson without the tool is sixty minutes plus the loss of the lesson's design rationale. The asymmetry favors verification.

---

## Core concept 1 — The phased Classroom rollout

The Google Classroom + NotebookLM integration rolled out in defined phases:

**September 2025.** Teachers create notebooks and share them within Classroom as view-only resources or assignment attachments. Students of all ages can access teacher-vetted notebooks under structured lesson designs.

**April 2026.** Higher-education students aged 18+ can create personal class notebooks grounded in educator-provided Classroom materials. Mobile support follows the web rollout. Under-18 students remain restricted to teacher-created, view-only notebooks.

**Upcoming.** Chat-only notebook sharing (students query but cannot view, edit, or copy raw source files — protecting teacher intellectual property) and shared notebook analytics (instructors see which files students query most, where confusion concentrates).

For K-12 as of writing, the September 2025 model is operative: teachers create, students consume. The chapter's assignment-design implications follow from this — Chapter 5's active-engagement patterns must be configured by the teacher, since K-12 students cannot generate their own notebooks independently.

---

## Core concept 2 — The admin toggle landscape

For NotebookLM in Classroom to work for your students, all of these must be true:

1. The district uses Google Workspace for Education (not a personal Google account workflow).
2. The IT administrator has enabled **Gemini** for the student organizational unit (OU).
3. The IT administrator has enabled **NotebookLM** for the student OU.
4. The IT administrator has enabled **Gemini in Classroom** if Classroom integration is desired.
5. The student is on the correct OU — not a default OU where the toggle hasn't been flipped.

Any one missing means the student sees no icon. The diagnostic walkthrough below assumes you have admin contact information; if you don't, getting it is the first step.

---

## Core concept 3 — Age-restricted features

Even within Education accounts and with NotebookLM enabled, several features are gated to users 18 and over:

- **Infographics** (10 visual styles) — 18+ only.
- **Cinematic Video Overviews** — 18+ only.
- **Slide-deck revision via feedback** — 18+ only.
- **Independent notebook creation via Classroom** — 18+ only (April 2026 rollout).

Teachers can generate these features for class use and distribute the output to younger students. What younger students cannot do is generate them themselves.

The pedagogical implication: for middle school and lower high school, NotebookLM functions as a **teacher production tool whose outputs are distributed**, not a **student production tool**. This narrows the assignment-design space — Chapter 5's error-hunt and source-check patterns work, since they use teacher-generated outputs as the substrate. Argument-extension patterns that depend on students generating Mind Maps or Briefing Docs themselves need to be adapted; the teacher generates the artifact, students extend it.

---

## Core concept 4 — District policy is its own gate

Even when admin toggles are technically possible, districts vary widely in policy choices. The pantry research file's example: Rochester Community Schools (Michigan) lists NotebookLM as available to staff members and explicitly states students are not able to use it.

This is not a misconfiguration. It is a deliberate policy. The district's reasoning, reconstructed: the productivity gain for staff (lesson prep) is real; the academic-integrity risk for students under current assessment design is unmanageable; the technology will mature; until then, hold the line.

The chapter's position: this is a defensible policy choice. The book's job is not to override it — it is to make the conversation precise. *What is being protected by the restriction? What is being given up? Who bears the cost on each side?* If the answer to those questions justifies opening student access, Chapter 13's administrator brief is how you make the case.

---

## Mid-chapter checkpoint

Before continuing:
- Can you list all five conditions that must be true for a K-12 student to use NotebookLM in Classroom?
- Can you identify three features your under-18 students cannot generate themselves?
- Can you name what your district's current policy is on student NotebookLM access?

If the third answer is "I don't know," that is the first thing to find out.

---

## Worked workflow — Verifying student access before lesson day

**Step 1 — Identify your admin.** Find the IT administrator for your school or district. Get their name, email, response-time expectation.

**Step 2 — Borrow or create a test student account.** Many districts maintain test accounts for teachers to verify student experiences. If yours does not, ask the admin to set one up; it pays for itself in a single avoided lesson-day failure.

**Step 3 — Log in as the test student.** Navigate to classroom.google.com. Open a class. Look for NotebookLM in the apps list or shared materials. If absent, NotebookLM is not enabled for the student OU.

**Step 4 — If absent, email your admin with specifics.** Subject: *"Enable NotebookLM for [student OU name]"*. Body: *"I'm planning a lesson [date] using NotebookLM. The icon doesn't appear in my test student account. Could you enable: Gemini, NotebookLM, and Gemini in Classroom for [student OU name]?"* Specificity reduces admin back-and-forth from days to one round.

**Step 5 — Once enabled, verify a second time.** Log back in as the test student. Confirm the icon appears. Click into a teacher-created notebook. Run one query. Confirm the citation function works.

This sequence happens *the week before* the lesson, not the night before. If you can do nothing else from this chapter, do this.

---

## What can go wrong

- **Admin enables NotebookLM but not Gemini in Classroom.** The student sees NotebookLM in the apps list but cannot access shared notebooks through Classroom. Both toggles need to be on.
- **Student is on the wrong OU.** A student transferred mid-year may be on a default OU rather than their grade-level OU. The grade-level OU has the toggle on; the default does not.
- **Admin enables for staff but not students.** The teacher's experience works fine; students see nothing. This is the most common version of the opening case.

---

## Core concept 5 — Why the personal-account workaround is wrong

A teacher in a district that does not enable NotebookLM for students may be tempted to have students use their personal Gmail accounts at home. The pantry research and Chapter 11 detail why this is structurally wrong:

- Personal-account data may be used to train Google's models. Workspace for Education accounts are explicitly excluded from training.
- Personal accounts lack FERPA/COPPA compliance.
- The school's IT and data-privacy officers have no visibility into the use.
- If a parent or auditor asks how student data is being handled, the school's answer is "we don't know."

The chapter must make this uncomfortable enough that teachers do not recommend the workaround without seeing what it means. The right path when district policy restricts access is Chapter 13 (the administrator brief), not the workaround.

---

## Common misconceptions

> **"My Google access means my students' access."**
> No. Admin toggles are per-OU. Staff and students are different OUs.

> **"Workspace for Education means NotebookLM is available."**
> No. Workspace for Education is the *prerequisite*, not the enabling toggle. The admin still has to opt in for the student OU.

> **"Age restrictions are a bug; they'll go away."**
> Some align with COPPA and won't change. Others are Google's policy choice and may evolve. Either way, design around current restrictions and verify before deployment.

---

## Exercises

1. *(Apply)* Identify your district's IT administrator. Confirm whether NotebookLM is enabled for the student OU. If not, draft the email requesting it.

2. *(Analyze)* For each output type you might assign to under-18 students, classify whether students can generate it themselves or whether you must generate and distribute.

3. *(Evaluate)* If your district blocks student NotebookLM access entirely, write a one-paragraph case for opening it. Include the integrity-design plan (Chapter 7), the equity assessment (Chapter 11), and the pedagogical rationale. (This is a draft for the Chapter 13 brief.)

---

## What would change my mind

If Google added a *visible* admin-status indicator in NotebookLM's Classroom integration UI showing teachers which student-side toggles are on, the verification workflow would shorten from five steps to one. As of writing, no such indicator exists at the user level.

## Still puzzling

- The chat-only notebook sharing model (upcoming) — will it satisfy districts that currently block student access entirely?
- Whether districts that restrict student access converge or diverge over the next two years.
- How shared notebook analytics (upcoming) will reshape what teacher dashboards can tell you about student engagement.

---

## Chapter summary

You can now:
- Verify NotebookLM availability for your students before lesson day, using a test student account.
- Diagnose which of the five enabling conditions has failed when the icon doesn't appear.
- Anticipate which assignment designs require admin intervention because of age restrictions.
- Distinguish a district's deliberate restriction policy from a misconfiguration, and respond appropriately to each.

## Key terms

- **Organizational unit (OU)** — Google Workspace administrative grouping. Toggles are per-OU.
- **Phased rollout** — Google's pattern of releasing NotebookLM features in stages, with age and account restrictions per phase.
- **Personal-account workaround** — Using personal Gmail to access NotebookLM; structurally wrong for student-data handling.

## Bridge question

The distribution mechanism works. **What happens to your assessments?** Chapter 7 addresses the part you cannot skip: redesigning assessments for an AI-augmented learning environment.

## Further reading

- Google Workspace for Education NotebookLM admin documentation. [verify URLs at draft time]
- Google Classroom + NotebookLM partnership announcements (Sept 2025; April 2026). [verify]
- *Pantry research file*, "Google Classroom Integration" and "Administrative requirements" sections.

## Quick-start card

> **Verifying student access**
>
> 1. Find your admin (name, email).
> 2. Get or borrow a test student account.
> 3. Log in as test student. Look for NotebookLM icon.
> 4. If absent, email admin (specific OU name, specific toggles).
> 5. Verify again after the enable.
>
> Do this the week before the lesson, not the night before.

## Aging note

**This chapter ages fastest in the book.** Admin console paths, age thresholds, the specific set of feature gates, the Classroom integration UI — all are moving. Re-verify against current Google documentation before each reprint. Plan a 6-10 figure budget for screenshots; the screenshots will need to be re-captured at each revision.
