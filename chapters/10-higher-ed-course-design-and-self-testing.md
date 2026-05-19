# Chapter 10 — Higher Education: Course Design and the Self-Testing Model

> *The Monash model — configure NotebookLM to quiz the learner, not explain to them — is the highest-leverage use case for undergraduate course integration.*

---

## Problem this chapter solves

University faculty face the same passive/active problem as K–12 teachers, amplified by the absence of Google Classroom's supervised notebook model. This chapter teaches the highest-leverage configurations for undergraduate course integration: Monash-style self-testing and NYU-style feedback loops.

## Learning outcomes

1. *(Create)* Design a NotebookLM-integrated assignment that uses Learning Guide as a self-testing companion rather than a summary generator.
2. *(Apply)* Configure a notebook for an undergraduate course and verify student access through institutional Workspace accounts.
3. *(Evaluate)* Assess the NYU faculty feedback-loop use case for applicability in your own course context.

## Prerequisites

- Chapters 1–3 (design principle, operational fluency).
- Chapter 5 (active-engagement framework — same logic, undergraduate population).
- An upcoming undergraduate course where NotebookLM integration is being considered.

---

## Opening case — Two correct deployments, different design principles

**Case A: UW-Milwaukee Math 94.** Ed Price, Teaching, Learning, and Technology Consultant at UW-Milwaukee, addressed student math anxiety in a remedial math course by generating podcast-style Audio Overviews of mathematical units. The audios were embedded in Canvas via MyMedia with closed captions and made *optional*. Students who chose to listen reported greater comfort during in-person problem-solving sessions. Price's conclusion: the tool works as a *supplementary companion* to dense readings, not as a replacement for active study.

**Case B: Monash University.** Monash configures NotebookLM's Learning Guide as a *self-testing study companion* that asks students diagnostic questions, adapts to their answers, and supports formative self-testing rather than giving direct answers. The deployment is *active and integrated* — the tool is the assignment, not a supplement to one.

Both cases are correct. The reason each is correct is a different design principle:

- Case A: *accessibility plus optionality.* The audio is there for students who benefit; the rest of the class is not penalized for skipping it. The audio does not replace any required work.
- Case B: *retrieval-practice integration.* The tool is the assignment; engagement is required by design.

The chapter's argument: a faculty member must know *which principle they are deploying*. Mixing them — making the audio required and high-stakes, or making the self-testing optional and ungraded — produces the failure modes Chapter 5 named.

---

## Core concept 1 — The Monash self-testing configuration

Monash configures Learning Guide to *quiz the learner, not explain to them*. This inverts the default tutoring pattern (student asks → tool answers) into a retrieval-practice pattern (tool asks → student answers → tool evaluates).

The pedagogical rationale is decades old. Retrieval practice produces durable learning (Karpicke & Roediger, *Science* 2008). A tutoring tool that bypasses retrieval — by explaining instead of testing — removes the cognitive event that produces learning. A tutoring tool configured to *force retrieval before explanation* preserves it.

**Configuration walkthrough.** A student loads a notebook with the week's assigned readings. They invoke Learning Guide. Instead of asking *"explain X,"* they say: *"Test me on chapter 4."* The tool generates diagnostic questions one at a time. The student answers each. The tool evaluates and provides feedback only after the student attempts.

The crucial design detail: this configuration must be *taught*. Students who haven't been told to use Learning Guide this way will default to asking it for explanations. The teacher's job is to make the configuration explicit — *here is how to use this tool. Here is why.*

**When it works best.** During *initial learning*, not review. As the encoding event, not as a check after the fact. Used after, it's a quiz; used during, it's the mechanism that produces the learning the quiz would later measure.

---

## Core concept 2 — The NYU faculty feedback loop

At NYU's October 2025 Teaching & Learning with Generative AI symposium, an instructor demonstrated a different use case: using NotebookLM to analyze student-feedback data from a large introductory programming course to create formative assessment activities, integrated with Brightspace and Poll Everywhere.

The structure:

1. Collect student feedback (mid-semester surveys, common confusions from assignment grading, polling responses).
2. Upload the feedback data to NotebookLM as a source.
3. Query: *"Based on this feedback, what three concepts are students most struggling with? Generate a formative assessment activity targeting each."*
4. Deploy the activities through the LMS and polling tool.

What's interesting about this case: NotebookLM is functioning as a *teaching analytics* tool — not generating content for students, but generating insight from student data that the teacher then acts on. It demonstrates the bounded-tool framework applied to course-improvement work, not just content production.

---

## Core concept 3 — The April 2026 student notebook expansion

A higher-ed-specific operational fact: as of April 2026, higher-education students aged 18+ can create *personal class notebooks* grounded in educator-provided Classroom materials. This is the operational unlock for the Monash model at scale — students need to instantiate their own notebooks from teacher-provided sources, not just consume teacher-built ones.

The pedagogical implication: undergraduate faculty can now design assignments that depend on individual student notebooks, not just shared class notebooks. This expands the design space beyond what was possible in K–12 (where individual student notebook creation is still gated for under-18 students).

The practical step: confirm institutional Workspace settings allow student notebook creation before designing assignments that require it. Some institutions enabled the feature; others have not.

---

## Core concept 4 — Accessibility uses

Beyond the active-engagement and feedback-loop deployments, NotebookLM provides accessibility affordances that matter at the undergraduate scale:

- **Closed captions** on all Audio and Video Overview outputs.
- **Multilingual output** for some output types (expanding through 2026).
- **Audio Overviews as anxiety-reducing on-ramps** for high-anxiety subjects (UW-Milwaukee Math 94 case).
- **Multimodal review** for students with reading-comprehension difficulties or visual-processing differences.

The chapter's framing: these are *legitimate uses* even when the active-engagement and retrieval-practice frameworks do not formally apply. A student who would otherwise disengage from dense reading entirely is better served by a tool-mediated entry point than by no engagement at all. The pedagogical bar is *did this student end up doing the work?*, not *did this student do the work in the canonical way?*

---

## Mid-chapter checkpoint

Before continuing:
- Can you state the two opening-case design principles and the deployment failures that result from mixing them?
- Can you describe the Monash configuration in operational terms (what the student types, what the tool does)?
- Can you name three higher-ed-specific affordances that change what NotebookLM is good for at this level?

---

## Worked workflow — Configuring Learning Guide for self-testing

For an upcoming undergraduate class session.

**Step 1 — Define the learning goal.** *Students will be able to apply the central concept of chapter 4 (e.g., regression to the mean) to a new case, identifying when the concept applies and when it doesn't.*

**Step 2 — Build the notebook.** Upload the chapter, any supplementary readings, and a Note from you specifying the kinds of questions you want Learning Guide to ask: *"Ask diagnostic questions that require the student to apply regression to the mean to a case they have not seen in the reading. Do not give the answer until the student has attempted. After their attempt, evaluate against the source and provide specific feedback. If they are wrong, ask a more scaffolded question rather than explaining."*

**Step 3 — Write the student-facing instructions.** *Before our Friday session, open the class notebook and invoke Learning Guide with the prompt 'Test me on chapter 4 applications.' Work through at least three diagnostic questions. Bring to class: one question you struggled with, one question that made the concept click for you.*

**Step 4 — Pilot with one or two students before deploying.** Their experience reveals configuration problems before you deploy to the full class.

**Step 5 — Verify the question quality after deployment.** Generate the question set yourself. Identify any questions that are weak, ambiguous, or testing the wrong thing. Cut them — the AI's diagnostic generation, like its other outputs, requires teacher review.

---

## What can go wrong

- **Learning Guide explains rather than tests.** The student didn't configure the prompt to force retrieval. The default mode is tutoring-by-explanation; the self-testing mode requires the explicit configuration. Re-verify the student-facing instructions emphasize the configuration step.

- **The AI's diagnostic questions are weak.** Pattern-matching on textbook-style questions; some are genuinely good, some are formulaic, some test the wrong concept. The teacher's review step (Step 5) is what filters them. Five minutes of question review per assignment is cheap; deploying weak questions to 200 students is expensive.

- **Students treat the optional self-testing as ungraded busywork.** If the deployment is *active and integrated* (Case B), the work needs to be tied to a graded outcome — even if the tie is light (participation credit for showing up Friday with the two questions). If it's *supplementary and accessibility-focused* (Case A), let it be optional and stop worrying about uptake.

---

## Common misconceptions

> **"Learning Guide is for review."**
> Most powerful during initial learning. The encoding moment, not the post-encoding check.

> **"AI tutoring matches human tutoring."**
> Educational Psychology Review (2025) found AI-generated quiz questions can match teacher-created materials *for self-assessment use*. The evidence is weaker for open-ended tutoring. Use the configurations the evidence supports.

> **"If students don't use the optional resource, the deployment failed."**
> Not necessarily. Optional accessibility resources have value if even a subset of students benefits. The success metric depends on which deployment design you chose.

---

## Exercises

1. *(Create)* Identify one undergraduate course where the self-testing model is applicable. Design the notebook, write the Learning Guide configuration prompt, and draft the student-facing instructions.

2. *(Apply)* Configure Learning Guide for one upcoming class session. Pilot with two students before assigning to the full class. Document one configuration adjustment you made based on the pilot.

3. *(Evaluate)* Compare the question quality of an AI-generated diagnostic set against your own instructor-designed set on the same material. Identify which questions you would keep, modify, or cut. What does the pattern tell you about where AI question generation is reliable and where it isn't?

---

## What would change my mind

A controlled comparison study of Learning-Guide-configured self-testing against instructor-designed self-testing showing equivalent or worse learning outcomes for the AI version (at the same student time investment) would weaken the chapter's central recommendation. The Educational Psychology Review 2025 finding suggests parity for the specific self-assessment use case; expansion of that evidence to the configured-tutoring use case is the relevant near-term research question.

## Still puzzling

- Whether Learning Guide's question quality varies enough across disciplines (humanities vs. STEM vs. professional fields) to require discipline-specific configuration libraries.
- Whether the NYU feedback-loop pattern generalizes to small-class settings or requires the data volume of a large lecture.
- What the long-term effect of habitual self-testing with AI is on student metacognition — does it build the skill, or does it create a dependency on the structured framework?

---

## Chapter summary

You can now:
- Distinguish the *accessibility-plus-optionality* and *retrieval-practice-integration* design principles.
- Configure Learning Guide for self-testing rather than explanation.
- Apply the NYU faculty feedback-loop pattern to extract teaching-improvement signal from student data.
- Use higher-ed-specific accessibility affordances where the canonical engagement frameworks don't directly apply.

## Key terms

- **Monash self-testing model** — Learning Guide configured to ask diagnostic questions and force retrieval before explanation.
- **NYU feedback loop** — NotebookLM as teaching-analytics tool, applied to student-feedback data.
- **April 2026 expansion** — 18+ higher-ed students can create personal class notebooks from teacher-provided sources.
- **Accessibility-plus-optionality** vs. **retrieval-practice-integration** — Two valid design principles; mixing them produces failures.

## Bridge question

Both K-12 and higher-ed paths have reached Chapter 11. **The remaining chapters address institutional deployment for all contexts. What does equitable deployment actually require?** Chapter 11.

## Further reading

- Karpicke & Roediger, *Science* (2008) — Retrieval-practice foundation.
- Educational Psychology Review (2025) — AI-generated quiz/flashcard finding. [verify exact citation]
- Monash University NotebookLM teaching guidance. [verify URL]
- *Pantry research file*, "Self-Regulated Study" and "Faculty Feedback Loops" sections.
- McTighe & Silver, *Teaching for Deeper Learning* (pantry library file) — Formative assessment context.

## Quick-start card

> **The Monash self-testing pattern**
>
> 1. Define the learning goal as a verb (apply, evaluate, construct).
> 2. Upload sources + a Note specifying *test, do not explain*.
> 3. Student-facing prompt: *"Test me on [topic]."*
> 4. Tool asks diagnostic questions; student answers; tool evaluates.
> 5. Tie the work to a low-stakes graded outcome.

## Aging note

Learning Guide's configuration interface and the specific feature set are evolving. The retrieval-practice mechanism it leverages is stable (decades of evidence). Re-verify the specific UI before reprint; the underlying argument can be re-issued unchanged.
