# Chapter 6 — Google Classroom Integration: Setup, Permissions, and Pedagogy

*The Classroom integration is where the pedagogy and the admin meet. Both have to work.*

---

Here is a failure that happens to someone the night before almost every school that tries this for the first time. You have designed the lesson. You have uploaded the materials, configured the notebook, tested the output. Everything works from your account. You log in as a test student to verify — and the NotebookLM icon is not there.

The admin enabled it for staff. Not for students. The toggle is a different toggle.

You email at 9 PM. The toggle flips at 11 AM the next morning, after first period. The lesson runs without the tool.

This chapter is about why that happens, what the underlying structure is, and how to prevent it. The failure is not bad luck. It is the predictable consequence of a permission architecture that has more moving parts than it appears to, and of the natural human tendency to assume that "it works for me" means "it works."

It does not mean that. Here is why.

---

## The permission stack

When a student opens Google Classroom and looks for NotebookLM, they are passing through a sequence of gates. Every gate has to be open. One closed gate and the icon is not there — no error message, no explanation, just absence.

The gates, in order:

The school or district must be using **Google Workspace for Education**. Not a personal Google account. Not a hybrid setup where teachers have Workspace accounts and students use personal Gmail. Workspace for Education is the institutional account type that makes the rest of the stack possible. If students are on personal accounts, the stack does not apply — and the chapter's discussion of why that matters comes later.

The IT administrator must have enabled **Gemini** for the student organizational unit. An organizational unit — OU, in the admin console's terminology — is how Google Workspace groups accounts for policy purposes. Staff are one OU. Students are typically another, sometimes broken down further by grade band. Enabling Gemini for the staff OU does not enable it for the student OU. These are separate actions.

The IT administrator must have enabled **NotebookLM** for the student OU. Gemini being on is necessary but not sufficient. NotebookLM is a separate service within the Gemini umbrella, and it has its own toggle.

If the assignment involves Classroom-integrated delivery — notebooks shared through Classroom rather than through a direct link — the administrator must also have enabled **Gemini in Classroom** for the student OU.

And finally: the student must actually be *on* the correct OU. A student who transferred mid-year, or who was initially placed in a default OU, may be on a unit where the toggles are all off — while the rest of their class has access. From the teacher's perspective, everything works for most students and inexplicably fails for one. From the admin's perspective, it is a student who was never moved to the right unit.

| Condition | Who controls it | Common failure mode |
|---|---|---|
| Google Workspace for Education account type | District IT / administrator | District uses personal Google accounts or a non-Education Workspace tier |
| Gemini enabled for student organizational unit (OU) | District IT administrator | Enabled for staff OU, left off for student OU |
| NotebookLM enabled for student OU | District IT administrator | Gemini enabled but NotebookLM specifically remains off |
| Gemini in Classroom enabled | District IT administrator | NotebookLM works in browser but not via Classroom share |
| Student assigned to correct OU | District IT / school administrator | Student transferred mid-year and remains on default OU where toggles haven't been flipped |

*Any one closed gate produces the same result: the icon doesn't appear.*
Five conditions. Any one missing and the student sees nothing. The relevant question before any lesson that depends on student access is: have I verified all five, for my students, from a test student account?

---

## Why verification requires a student account

The natural way to check whether students have access is to look at your own account. This is wrong, for the same reason that a building manager checking whether the staff entrance keycard works tells you nothing about whether the visitor entrance is unlocked.

You are on the staff OU. Your access reflects staff-OU settings. Student-OU settings are different, and you cannot see them from where you stand.

The correct verification procedure uses a test student account — an account on the student OU, with student-level permissions, logging into the student experience. Many districts maintain these specifically for teacher verification purposes. If yours does not, the admin can create one; the investment pays for itself the first time it catches a closed gate before lesson day rather than during.

The verification sequence is straightforward: log in as the test student, navigate to Classroom, look for the NotebookLM icon in the apps list or shared materials, click into a teacher-created notebook, run a query, confirm citations appear. Five steps. Roughly five minutes. The asymmetry with the alternative — discovering the failure at first period — is large enough that the only real argument against running this check is not knowing it is necessary.

This chapter exists so that you know.

![Run this the week before the lesson. Not the night before.](images/06-google-classroom-integration-fig-01.png)
*Figure 6.1 — Five-step verification checklist as a visual sequence *

If the icon is absent at step three, the diagnosis is one of the five conditions above. The most common: the admin enabled NotebookLM for staff but the student OU toggle was never touched. The email to the admin should be specific — not "NotebookLM doesn't work for students" but "the NotebookLM icon is absent in my test student account; I believe Gemini and NotebookLM need to be enabled for the [student OU name] organizational unit." Specificity converts a multi-day back-and-forth into a single round.

![Mockup of an effective admin request email naming the organizational unit by name and specifying the exact toggles to enable (Gemini, NotebookLM, Gemini in Classroom). Callouts highlight the OU name and the toggle list as the elements that resolve the request in one round.](../images/06-google-classroom-integration-fig-01.png)
*Figure 6.1 — The admin email that resolves in one round*

---

## The phased rollout and what it means for K–12

Google did not release all of NotebookLM's Classroom integration at once. It released it in phases, and the phases have different age restrictions. Understanding which phase applies to your students determines what your assignment designs can actually ask students to do.

The September 2025 phase: teachers create notebooks and share them through Classroom. Students access teacher-created notebooks. Students of all ages, with appropriate admin enablement, can view and query teacher-created notebooks. This is the foundational model — teacher produces, students consume and interact with what the teacher produced.

The April 2026 phase: students aged 18 and over can create their own class notebooks grounded in educator-provided Classroom materials. This phase explicitly excludes under-18 students. K–12 students under 18 remain in the September 2025 model: they can access teacher-created notebooks, but they cannot create independent notebooks through the Classroom integration.

The assignment-design implication is direct. Chapter 5's active-engagement patterns — source-checking, error-hunting, argument-extension — work for K–12 precisely because they use teacher-generated artifacts as the substrate. The teacher generates the Mind Map or the Briefing Doc; students interrogate it, correct it, extend it. This pattern fits the September 2025 model exactly. What would not fit is an assignment that asks under-18 students to independently generate their own notebooks from Classroom materials — that requires the April 2026 phase and the 18+ age gate.

Designing assignments that depend on student-side generation for students who cannot generate is a second version of the opening failure. The first version is an admin misconfiguration. This version is a design assumption that does not match the access model.

![Which phase applies to your students determines what your assignments can ask them to do.](images/06-google-classroom-integration-fig-02.png)
*Figure 6.2 — Timeline of NotebookLM Classroom rollout phases *

---

## Age-restricted features

The age restrictions do not stop at notebook creation. Several NotebookLM features are gated to users 18 and over regardless of admin settings.

Infographics — all ten visual styles — are restricted to 18+. Cinematic Video Overviews are restricted to 18+. Slide-deck revision via feedback is restricted to 18+. These restrictions are not misconfigurations and they will not be resolved by admin toggles. Some align with COPPA requirements for under-13 users. Others are Google's policy choice for the under-18 population.

The pedagogical structure this creates: for middle school and lower high school, NotebookLM functions as a teacher production tool whose outputs are distributed, not a student production tool. The teacher can generate an Infographic and share it. The student cannot generate one. The teacher can produce a Cinematic Video Overview and post it to Classroom. The student cannot produce one.

| Feature | Teacher (18+) | Higher-ed student (18+) | K–12 student (under 18) |
|---|---|---|---|
| Audio Overview | Available | Available | Available |
| Study Guide | Available | Available | Available |
| Mind Map | Available | Available | Available |
| Briefing Doc | Available | Available | Available |
| Flashcards | Available | Available | Available |
| Quiz | Available | Available | Available |
| Learning Guide | Available | Available | Available |
| Interactive Audio | Available | Available | Available (with institutional account configuration) |
| Slide Deck (generation) | Available | Available | Available |
| Slide Deck (revision via feedback) | Available | Available | **Not available** |
| Infographics | Available | Available | **Not available** |
| Cinematic Video Overview | Available | Available | **Not available** |
| Independent notebook creation via Classroom | Available | Available (April 2026+) | **Not available** |

*The assignment design space for under-18 students is narrower. The active-engagement patterns that work are the ones that use teacher-generated artifacts as their substrate.*
The design move that preserves active engagement within these constraints: generate the restricted artifact yourself, distribute it, and configure the assignment so that engagement with the artifact — not production of it — is the student's task. An error-hunt through a teacher-generated Infographic requires close reading and domain judgment. The student is not just consuming the Infographic; they are evaluating it. The cognitive demand is real even though the student did not generate the artifact.

---

## District policy is a different problem

There is a distinction worth making between a misconfiguration and a deliberate policy choice.

A misconfiguration is the admin who enabled NotebookLM for staff and forgot the student OU. It is the student on the wrong OU. It is Gemini enabled but Gemini in Classroom not enabled. These are fixable, and the fix is usually one email.

A deliberate policy choice is a district that has looked at the admin options, understood what they are enabling and for whom, and decided that student access is not appropriate under current conditions. Rochester Community Schools in Michigan is a documented example as of this writing: NotebookLM available to staff, explicitly not available to students. The reasoning is not stated publicly, but it is reconstructible: the productivity gain for staff in lesson preparation is real and defensible; the academic-integrity risk for students under current assessment design is harder to manage; the district is holding the line until the policy environment clarifies.

This is a defensible position. The chapter's job is not to override it but to make the conversation precise: what is being protected by the restriction, what is being given up, and who bears the cost on each side.

What is being protected: assessment integrity, data-handling compliance, the policy coherence of treating AI consistently across subjects and grade levels rather than having it available in some classrooms and not others.

What is being given up: the active-engagement patterns described in Chapter 5 — source-checking, error-hunting, argument-extension — that use NotebookLM as a substrate for student thinking rather than a replacement for it.

Who bears the cost: students in districts with more permissive policies have access to a thinking tool their peers in more restrictive districts do not. Whether this constitutes an equity gap depends on how much the active-engagement patterns actually improve learning outcomes, which is a question the research has not yet settled.

The administrator brief for making the case that student access is worth opening — including an integrity-design plan and an equity assessment — is Chapter 13. This chapter's job is to distinguish "the toggle isn't on" from "the district decided the toggle stays off." The response to each is different.

---

## The personal-account workaround

When a district restricts student access, a teacher might consider having students use their personal Gmail accounts to reach NotebookLM at home. This is a predictable response and a wrong one.

The structural problem: personal-account data is handled under Google's consumer terms of service, not its Workspace for Education terms. Consumer terms permit Google to use data to train models. Workspace for Education terms explicitly exclude that use. A student doing homework in a personal Gmail account is feeding their work into a training pipeline their school's privacy officer does not know about and has not consented to.

The compliance problem: FERPA and COPPA apply to student educational records and to services used to process them. A teacher who directs students to a personal-account tool for schoolwork has created a FERPA situation the school cannot audit and cannot correct. The student's queries about the assigned reading are educational records. They are now outside any institutional data-handling framework.

The accountability problem: if a parent or auditor asks how student data is being handled in AI-assisted assignments, the answer becomes "we don't know, we sent them to their personal accounts." That answer ends conversations badly.

The right path when district policy restricts access is not the workaround. It is the administrator brief. The workaround looks like it solves the immediate problem. It creates a larger one.

---

## What the upcoming features change

Two features are on Google's public roadmap for the Classroom integration that will change the design space when they ship.

Chat-only notebook sharing: students can query a teacher-created notebook but cannot view, edit, or copy the source files. The pedagogical use case is protecting teacher-developed materials — a teacher who has spent significant time curating a source set does not have to choose between giving students access to the notebook and giving them access to the underlying files. The student gets the query interface; the source files stay protected. For districts that currently restrict student access out of concern for intellectual property, this feature may shift the cost-benefit calculation.

Shared notebook analytics: instructors can see which source files students query most, where confusion concentrates, which questions get asked repeatedly. The pedagogical use case is formative assessment that does not require a quiz — if thirty students are asking variants of the same question about a specific section of the source, that is diagnostic information about where the material is not landing. This feature lands in Chapter 8's territory; it is mentioned here because its arrival changes what teacher dashboards can tell you about student engagement with Classroom-integrated notebooks.

Neither feature is available as of this writing. The chapter notes them because the districts and teachers who are holding on student access pending better tooling are correct to wait — and these are the tools they are waiting for.

---

## The thing that determines everything else

Admin configuration, age restrictions, district policy, feature availability — all of it sits on top of one prior question: does your district use Google Workspace for Education?

If the answer is no — if teachers have Workspace accounts and students have personal Gmail accounts, or if the district uses a different platform entirely — then this chapter's architecture does not apply to your students. The Classroom integration requires Workspace. The age-gating requires Workspace. The data-handling guarantees that distinguish the institutional account from the personal account require Workspace.

If your district is in this position, the relevant conversation is not about NotebookLM configuration. It is about whether the district's account infrastructure is appropriate for AI-assisted learning at all, and that is a conversation that starts before any tool deployment.

For everyone in a Workspace for Education environment: the permission stack is verifiable, the age restrictions are documented, the district's policy position is findable, and the workarounds are wrong. What remains is the week-before check — five minutes, a test student account, five gates, five confirmations.

The lesson that depends on student access requires that the access actually exists, in the student account, before lesson day. Everything in this chapter is in service of that sentence.

| What the teacher observes | Most likely cause | Action |
|---|---|---|
| Icon absent for all students | Admin hasn't enabled NotebookLM for the student OU | Email admin with specific OU name and request to enable Gemini + NotebookLM + Gemini in Classroom |
| Icon absent for one student | Student on wrong OU | Ask admin to move student to the correct OU |
| Icon present but notebook inaccessible | Gemini in Classroom not enabled | Email admin to enable Gemini in Classroom specifically |
| Feature absent for students | Age-restricted feature (under-18) — not fixable by admin | Redesign the assignment to use a teacher-generated version of the artifact |
| Access blocked by policy | Deliberate district decision (e.g., Rochester pattern) | Different chapter — see Chapter 13 for the administrator brief |

*The observation determines the response. Most failures resolve in one email. Some require a different chapter.*
---

## Exercises

**Warm-up**

1. *(Apply — verifying the stack)* Identify the IT administrator for your school or district. Write down their name, email address, and your best estimate of their typical response time to a non-urgent request. If you do not know who this person is, finding out is the exercise.

2. *(Apply — account type)* Confirm whether your students are on Google Workspace for Education accounts or personal Gmail accounts. If you are unsure, log in to a test student account and look at the account domain — a Workspace for Education account will show your district domain, not @gmail.com.

3. *(Apply — running the verification)* Using a test student account, run the five-step verification sequence from the chapter. Record at which step, if any, access fails. If no test student account is available, draft the request to your admin to create one.

**Application**

4. *(Analyze — age restrictions)* Review the lesson you most recently taught or are currently planning that uses NotebookLM outputs. For each output type in that lesson, classify whether your students — given their ages — can generate it themselves or whether you must generate and distribute it. Identify any design assumptions that need to be revised.

5. *(Analyze — phased rollout)* You are designing an assignment for a 10th-grade class (students aged 15–16) that asks students to create personal notebooks grounded in teacher-provided Classroom materials and share them with you for review. Explain precisely why this assignment does not work under the current access model, and describe the adaptation that would preserve the assignment's learning goal within the September 2025 model.

6. *(Apply — the specific email)* The five-step verification reveals that the NotebookLM icon is absent in your test student account. Write the email to your admin. Include the subject line, the specific toggles you believe need to be enabled, and the name of the student OU (use a placeholder if you do not know the actual OU name). Compare your draft against the specificity standard in the chapter: does your email resolve in one round?

**Synthesis**

7. *(Evaluate — misconfiguration vs. policy)* You run the verification and discover that NotebookLM is disabled for students by a district-level policy decision, not a misconfiguration. Describe in one paragraph how your response differs from the response to a misconfiguration. What is the first concrete step you would take, and what is the document you would need to produce before taking it?

8. *(Evaluate — the workaround)* A colleague tells you she has her students use their personal Gmail accounts to access NotebookLM at home because the district hasn't enabled it for students yet. Identify the three structural problems with this approach — one data-handling problem, one compliance problem, and one accountability problem — and explain each in a sentence your colleague could repeat to a parent asking about the practice.

**Challenge**

9. *(Evaluate — the cost-benefit of restriction)* Rochester Community Schools restricts student NotebookLM access entirely. Using only the framework the chapter provides — what is being protected, what is being given up, who bears the cost — write a one-paragraph analysis of whether their policy is defensible. Then identify the one piece of evidence, if it existed, that would most change your analysis.

10. *(Create — the administrator brief outline)* You teach in a district where student access is currently blocked by policy. Using Chapter 13 as the eventual destination, outline the three components an administrator brief would need to address to make the case for opening access: the integrity-design plan, the equity assessment, and the pedagogical rationale. For each component, write one sentence describing what the strongest version of that argument would claim.

## Prompts

Use these prompts with Claude to generate interactive D3 v7 versions of the
figures in this chapter. Each produces a standalone HTML file you can open
in a browser and modify freely.

**Prerequisites:** Load `brutalist/CLAUDE.md` and `brutalist/DESIGN.md` into
your Claude project context before using these prompts. They define the stack,
naming conventions, color system, and typography the figures use.

---

### Figure 6.1 — Five-step verification checklist as a visual sequence 

Create a standalone D3 v7 HTML file for Figure Five-step verification checklist as a visual sequence . Use the CDN https://cdnjs.cloudflare.com/ajax/libs/d3/7.9.0/d3.min.js, inline CSS, ResizeObserver redraw, SVG role="img", aria-labelledby, title, and desc. Build the figure from this structural brief: Five-step verification checklist as a visual sequence — Step 1: Log in as test student. Step 2: Open Classroom. Step 3: Look for NotebookLM icon. Step 4: Click into teacher-created notebook. Step 5: Run a query and confirm citations. Style: clean numbered steps, each with a one-line description. Caption: "Run this the week before the lesson. Not the night before.". Use the described data shape and labels; when exact values are not supplied, use plausible illustrative values that preserve the relationships in the brief. Use a zero baseline for bars or areas, direct labels where possible, and annotations named in the brief. Use only DESIGN.md color variables and the required serif/mono font split.

> Reference implementation: `d3/06-google-classroom-integration-fig-01.html`

---

### Figure 6.2 — Timeline of NotebookLM Classroom rollout phases 

Create a standalone D3 v7 HTML file for Figure Timeline of NotebookLM Classroom rollout phases . Use the CDN https://cdnjs.cloudflare.com/ajax/libs/d3/7.9.0/d3.min.js, inline CSS, ResizeObserver redraw, SVG role="img", aria-labelledby, title, and desc. Build the figure from this structural brief: Timeline of NotebookLM Classroom rollout phases — September 2025 and April 2026 marked on a horizontal timeline. For each phase: what became available, who it applies to (all ages / 18+ only). Annotate the gap between phases with "K–12 students remain on the September 2025 model." Caption: "Which phase applies to your students determines what your assignments can ask them to do.". Use the described data shape and labels; when exact values are not supplied, use plausible illustrative values that preserve the relationships in the brief. Use a zero baseline for bars or areas, direct labels where possible, and annotations named in the brief. Use only DESIGN.md color variables and the required serif/mono font split.

> Reference implementation: `d3/06-google-classroom-integration-fig-02.html`
