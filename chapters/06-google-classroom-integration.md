# Chapter 6 — Google Classroom Integration: Setup, Permissions, and Pedagogy

*The toggle exists. It is a different toggle.*

Here is a failure that happens to someone the night before almost every school that tries this for the first time. You have designed the lesson. You have uploaded the materials, configured the notebook, tested the output. Everything works from your account. You log in as a test student to verify — and the NotebookLM icon is not there.

The admin enabled it for staff. Not for students. The toggle is a different toggle.

You email at 9 PM. The toggle flips at 11 AM the next morning, after first period. The lesson runs without the tool.

This chapter is about why that happens and how to prevent it. The failure is not bad luck. It is the predictable consequence of a permission architecture that has more moving parts than it appears to, and of the natural human tendency to assume that "it works for me" means "it works." It does not mean that. Here is why.

---

When a student opens Google Classroom and looks for NotebookLM, they are passing through a sequence of gates. Every gate has to be open. One closed gate and the icon is not there — no error message, no explanation, just absence.

The first gate: the school or district must be using Google Workspace for Education. Not a personal Google account. Not a hybrid setup where teachers have Workspace accounts and students use personal Gmail. Workspace for Education is the institutional account type that makes the rest of the stack possible. If students are on personal accounts, the stack does not apply — and the implications of that are serious enough that I address them separately below.

The second gate: the IT administrator must have enabled Gemini for the student organizational unit. An organizational unit — OU, in the admin console's terminology — is how Google Workspace groups accounts for policy purposes. Staff are one OU. Students are typically another, sometimes broken further by grade band. Enabling Gemini for the staff OU does not enable it for the student OU. These are separate actions.

The third gate: the IT administrator must have enabled NotebookLM for the student OU. Gemini being on is necessary but not sufficient. NotebookLM is a separate service within the Gemini umbrella, and it has its own toggle.

The fourth gate: if the assignment involves Classroom-integrated delivery — notebooks shared through Classroom rather than through a direct link — the administrator must also have enabled Gemini in Classroom for the student OU.

The fifth gate: the student must be on the correct OU. A student who transferred mid-year, or who was placed initially in a default OU, may be on a unit where the toggles are all off while the rest of their class has access. From the teacher's perspective, everything works for most students and inexplicably fails for one. From the admin's perspective, it is a student who was never moved to the right unit.

<!-- → [TABLE: Five-gate permission stack — columns: Condition, Who controls it, Common failure mode. Rows: Workspace for Education account type / Gemini enabled for student OU / NotebookLM enabled for student OU / Gemini in Classroom enabled / Student on correct OU. Note at bottom: any one closed gate produces the same result — the icon doesn't appear.] -->

Five conditions. Any one missing and the student sees nothing. The question before any lesson that depends on student access is not "does it work?" — it is "have I verified all five, for my students, from a test student account?"

---

The natural way to check whether students have access is to look at your own account. This is wrong, for the same reason that a building manager checking whether the staff entrance keycard works tells you nothing about whether the visitor entrance is unlocked.

You are on the staff OU. Your access reflects staff-OU settings. Student-OU settings are different, and you cannot see them from where you stand.

The correct verification uses a test student account — an account on the student OU, with student-level permissions, logging into the student experience. Many districts maintain these specifically for teacher verification. If yours does not, the admin can create one; the investment pays for itself the first time it catches a closed gate before lesson day rather than during.

The sequence: log in as the test student, navigate to Classroom, look for the NotebookLM icon in the apps list or shared materials, click into a teacher-created notebook, run a query, confirm citations appear. Five steps, roughly five minutes. The asymmetry with the alternative — discovering the failure at first period — is large enough that the only real argument against running this check is not knowing it is necessary.

![Run this the week before the lesson. Not the night before.](images/06-google-classroom-integration-fig-01.png)
*Figure 6.1 — Five-step verification checklist as a visual sequence*

If the icon is absent at step three, the diagnosis is one of the five conditions above. The email to the admin should be specific — not "NotebookLM doesn't work for students" but "the NotebookLM icon is absent in my test student account; I believe Gemini and NotebookLM need to be enabled for the [student OU name] organizational unit, and Gemini in Classroom may also need to be enabled." Specificity converts a multi-day back-and-forth into a single round.

<!-- → [TABLE: Observation-to-action diagnostic — columns: What the teacher observes, Most likely cause, Action. Rows: Icon absent for all students / Icon absent for one student / Icon present but notebook inaccessible / Feature absent for students / Access blocked by policy.] -->

---

Google did not release the Classroom integration all at once. It released it in phases, and the phases have different age restrictions. Understanding which phase applies to your students determines what your assignment designs can actually ask students to do.

The September 2025 phase: teachers create notebooks and share them through Classroom. Students access teacher-created notebooks. Students of all ages — with appropriate admin enablement — can view and query teacher-created notebooks. This is the foundational model: the teacher produces, students consume and interact with what the teacher produced.

The April 2026 phase: students aged 18 and over can create their own class notebooks grounded in educator-provided Classroom materials. This phase explicitly excludes under-18 students. K–12 students under 18 remain in the September 2025 model: they can access teacher-created notebooks, but they cannot create independent notebooks through the Classroom integration.

The assignment-design implication is direct. The active-engagement patterns from Chapter 5 — source-checking, error-hunting, argument-extension — work for K–12 precisely because they use teacher-generated artifacts as the substrate. The teacher generates the Mind Map or the Briefing Doc; students interrogate it, correct it, extend it. This pattern fits the September 2025 model exactly. What would not fit is an assignment asking under-18 students to independently generate their own notebooks from Classroom materials — that requires the April 2026 phase and the 18+ age gate.

Designing assignments that depend on student-side generation for students who cannot generate is a second version of the opening failure. The first version is an admin misconfiguration. This version is a design assumption that does not match the access model. Both produce the same outcome: the lesson does not work.

<!-- → [FIGURE: Timeline of NotebookLM Classroom rollout phases — September 2025 (teacher-created notebooks, all ages) and April 2026 (student-created notebooks, 18+ only). Annotate which student populations fall into each phase.] -->

---

The age restrictions do not stop at notebook creation. Several NotebookLM features are gated to users 18 and over regardless of admin settings.

Infographics — all ten visual styles — are restricted to 18+. Cinematic Video Overviews are restricted to 18+. Slide-deck revision via feedback is restricted to 18+. These restrictions are not misconfigurations and will not be resolved by admin toggles. Some align with COPPA requirements for under-13 users. Others are Google's policy choice for the under-18 population.

The structure this creates: for middle school and lower high school, NotebookLM functions as a teacher production tool whose outputs are distributed, not a student production tool. The teacher can generate an Infographic and share it. The student cannot generate one. The teacher can produce a Cinematic Video Overview and post it to Classroom. The student cannot produce one.

<!-- → [TABLE: Feature availability by user type — columns: Feature, Teacher (18+), Higher-ed student (18+), K–12 student (under 18). Rows covering all major output types. Flag Infographics, Cinematic Video, Slide Deck revision via feedback, and independent notebook creation as Not available for K–12. Note at bottom: the active-engagement patterns that work for K–12 are the ones that use teacher-generated artifacts as substrate.] -->

The design move that preserves active engagement within these constraints: generate the restricted artifact yourself, distribute it, and configure the assignment so that engagement with the artifact — not production of it — is the student's task. An error-hunt through a teacher-generated Infographic requires close reading and domain judgment. The student is not just consuming the Infographic; they are evaluating it. The cognitive demand is real even though the student did not generate the artifact.

This is not a workaround. It is a coherent instructional pattern — and the one that fits the pedagogical argument of Chapter 3. The output type is the teacher's tool for shaping cognitive demand. Under the K–12 access model, that is literally true: the teacher controls which artifacts exist, which means the teacher is making every output-type decision. The constraint makes the pedagogy visible.

---

There is a distinction worth making between a misconfiguration and a deliberate policy choice, because the response to each is different.

A misconfiguration is the admin who enabled NotebookLM for staff and forgot the student OU. It is the student on the wrong OU. It is Gemini enabled but Gemini in Classroom not enabled. These are fixable, and the fix is usually one email — provided the email is specific.

A deliberate policy choice is a district that has looked at the admin options, understood what they are enabling and for whom, and decided that student access is not appropriate under current conditions. Rochester Community Schools in Michigan is a documented example as of this writing: NotebookLM available to staff, explicitly not available to students. The reasoning is not stated publicly, but it is reconstructible. The productivity gain for staff in lesson preparation is real and defensible. The academic-integrity risk for students under current assessment design is harder to manage. The district is holding the line until the policy environment clarifies.

This is a defensible position. What is being protected: assessment integrity, data-handling compliance, the policy coherence of treating AI consistently across subjects and grade levels rather than having it available in some classrooms and not others. What is being given up: the active-engagement patterns that use NotebookLM as a substrate for student thinking rather than a replacement for it. Who bears the cost: students in districts with more permissive policies have access to a thinking tool their peers in more restrictive districts do not.

Whether that constitutes an equity gap depends on how much the active-engagement patterns actually improve learning outcomes — a question the research has not yet settled. The administrator brief for making the case that student access is worth opening is Chapter 13. This chapter's job is to distinguish "the toggle isn't on" from "the district decided the toggle stays off." The response to each is different, and confusing them wastes time in the wrong direction.

---

When a district restricts student access, a teacher might consider having students use their personal Gmail accounts to reach NotebookLM at home. This is a predictable response. It is also wrong.

The structural problem: personal-account data is handled under Google's consumer terms of service, not its Workspace for Education terms. Consumer terms permit Google to use data to train models. Workspace for Education terms explicitly exclude that use. A student doing homework on a personal Gmail account is feeding their work into a training pipeline their school's privacy officer does not know about and has not consented to.

The compliance problem: FERPA and COPPA apply to student educational records and to services used to process them. A teacher who directs students to a personal-account tool for schoolwork has created a FERPA situation the school cannot audit and cannot correct. The student's queries about the assigned reading are educational records. They are now outside any institutional data-handling framework.

The accountability problem: if a parent or auditor asks how student data is being handled in AI-assisted assignments, the answer becomes "we don't know, we sent them to their personal accounts." That answer ends conversations badly.

The right path when district policy restricts access is not the workaround. It is the administrator brief. The workaround looks like it solves the immediate problem. It creates a larger one.

---

Two features on Google's public roadmap for the Classroom integration will change the design space when they ship.

Chat-only notebook sharing: students can query a teacher-created notebook but cannot view, edit, or copy the source files. The pedagogical use case is protecting teacher-developed materials — a teacher who has spent significant time curating a source set does not have to choose between giving students access to the notebook and giving them access to the underlying files. The student gets the query interface; the source files stay protected. For districts that currently restrict student access out of concern for intellectual property, this feature may shift the cost-benefit calculation.

Shared notebook analytics: instructors can see which source files students query most, where confusion concentrates, which questions get asked repeatedly. The pedagogical use case is formative assessment that does not require a quiz — if thirty students are asking variants of the same question about a specific section of a source, that is diagnostic information about where the material is not landing. This feature is mentioned here because its arrival changes what teacher dashboards can tell you about student engagement with Classroom-integrated notebooks; it gets its full treatment in Chapter 8.

Neither feature is available as of this writing. The districts holding on student access pending better tooling are correct to wait — and these are the tools they are waiting for.

---

Every layer of this chapter — the permission stack, the age gates, the phased rollout, the policy distinction — sits on top of one prior question: does your district use Google Workspace for Education?

If the answer is no — if teachers have Workspace accounts and students have personal Gmail accounts, or if the district uses a different platform entirely — then this chapter's architecture does not apply to your students. The Classroom integration requires Workspace. The age-gating requires Workspace. The data-handling guarantees that distinguish the institutional account from the personal account require Workspace.

If your district is in this position, the relevant conversation is not about NotebookLM configuration. It is about whether the district's account infrastructure is appropriate for AI-assisted learning at all — and that is a conversation that starts before any tool deployment.

For everyone in a Workspace for Education environment: the permission stack is verifiable, the age restrictions are documented, the district's policy position is findable, and the workarounds are wrong. What remains is the week-before check. Five minutes. A test student account. Five gates. Five confirmations.

The lesson that depends on student access requires that the access actually exists, in the student account, before lesson day. Everything in this chapter is in service of that sentence.

---

## LLM Exercises

These exercises use a language model as a thinking partner. For each, paste the specified prompt into a separate AI session (not NotebookLM) and engage with the output as a draft to interrogate, not a conclusion to accept.

**Exercise 1 — Map your own permission stack**

*Prompt:* "I am a teacher at [school/district type] using Google Workspace for Education. My students are in grades [X–Y], which means they are approximately [age range] years old. Walk me through the five-gate permission stack for NotebookLM Classroom access and, for each gate, generate the most likely failure mode given my institutional context. Then generate the specific email I should send to my IT administrator to verify or establish each condition — including the subject line and the exact toggle names to reference."

Interrogate the response: Does the AI's failure-mode prediction match your actual institutional situation? Did it name your student OU correctly, or did it leave a placeholder you need to fill in from real knowledge?

**Exercise 2 — Audit an assignment for access-model fit**

*Prompt:* "I am designing an assignment for students aged [X] using NotebookLM through Google Classroom. The assignment asks students to [describe the assignment]. Evaluate whether this assignment fits the current NotebookLM Classroom access model for students of this age. Identify any features or actions in the assignment that are age-restricted or unavailable under the September 2025 rollout phase. Then propose an adaptation that preserves the learning goal within the constraints that actually apply."

Use this before finalizing any assignment that asks students to generate NotebookLM outputs.

**Exercise 3 — Draft the administrator brief outline**

*Prompt:* "My district currently restricts student access to NotebookLM by policy, not by misconfiguration. I want to make the case for opening access. Help me outline an administrator brief that addresses three components: an integrity-design plan (how assessment design prevents the tool from substituting for student thinking), an equity assessment (who gains and who loses under the current restriction, and what the evidence says about learning-outcome impact), and a pedagogical rationale (what specific active-engagement patterns become possible with student access that are not possible without it). For each component, write the strongest single paragraph the brief would contain."

After generating the outline, evaluate it: Is the integrity-design plan specific enough to be operationalizable, or does it stay at the level of intention? What would a skeptical principal push back on?

---

## Bridge

The permission architecture determines what is possible. Chapter 7 moves to what is practical — how to design the Classroom notebook structure itself: which materials to upload, how to configure shared access, and how the teacher-notebook model becomes a weekly workflow rather than a one-time setup. The gates are open. Now you build what goes inside them.

---

## Further Reading

- Google Workspace for Education documentation — *NotebookLM for Education: Setup and Administration* (current release notes). The primary source for OU configuration and toggle locations. Check for updates when new output types ship.
- Google Workspace for Education documentation — *Gemini in Classroom: Administrator Guide.* Covers the Gemini in Classroom toggle as distinct from the Gemini toggle — the most commonly missed gate.
- Future of Privacy Forum, *Student Privacy and AI: A Guide for K–12 Administrators* (2024) — The FERPA and COPPA framework behind the personal-account problem. Useful background for the administrator brief.
- Mollick, *Co-Intelligence* (2024) — The labor-separation framework that informs how teacher-side generation and student-side engagement are treated as distinct roles throughout this chapter.
