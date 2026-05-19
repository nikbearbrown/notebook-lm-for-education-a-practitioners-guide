# Research Notes: Chapter 10 — Higher Education: Course Design and the Self-Testing Model

**Source:** TIKTOC.md chapter entry
**Notes file:** 10-higher-ed-course-design-and-self-testing_notes.md
**Corresponding chapter:** chapters/10-higher-ed-course-design-and-self-testing.md (not yet written)
**Generated:** 2026-05-19

---

## Chapter summary (from TIKTOC.md)

**One-line:** The Monash model — configure NotebookLM to quiz the learner, not explain to them — is the highest-leverage use case for undergraduate course integration.

**Problem this chapter solves:** University faculty face the same passive/active problem as K–12 teachers, amplified by the absence of Classroom's supervised notebook model.

**Learning outcomes:**
1. (Create) Design a NotebookLM-integrated assignment using Learning Guide as a self-testing companion.
2. (Apply) Configure a notebook for an undergraduate course and verify student access.
3. (Evaluate) Assess the NYU faculty feedback-loop use case for applicability.

**Opening:** Two university use cases side by side — UW-Milwaukee Math 94 audio (supplementary, low-stakes) vs. Monash self-testing companion (active, diagnostic). Both correct.

---

## A. Conceptual foundations

### Concept 1 — The Monash self-testing model

Monash University configures NotebookLM's Learning Guide as a *self-testing companion* — the tool asks diagnostic questions and the student answers; the tool does not give the answer until the student has attempted it. This inverts the default tutoring pattern (student asks, tool answers) into a retrieval-practice pattern (tool asks, student answers, tool evaluates).

The pedagogical rationale: retrieval practice produces durable learning (Karpicke & Roediger 2008; Cepeda et al. 2008). A tutoring tool that bypasses retrieval — by explaining instead of testing — removes the cognitive event that produces learning. A tutoring tool configured to *force retrieval before explanation* preserves it.

**Worked example:** Student loads a notebook with the week's assigned readings. They invoke Learning Guide. Instead of asking "explain X," they say "test me on chapter 4." The tool generates diagnostic questions one at a time. The student answers each. The tool evaluates and provides feedback only after the student attempts.

**Common misconception:** "Learning Guide is for review of already-known material." It is most powerful when used during initial learning — *as the encoding event*, not after. Used after, it's a check; used during, it's the mechanism.

**Source(s):** pantry/notebooklm_education_research.md "Self-Regulated Study" and "Assessment Redesign" sections.

---

### Concept 2 — The NYU faculty feedback loop

At NYU's October 2025 Teaching & Learning with Generative AI symposium, an instructor demonstrated using NotebookLM to analyze student-feedback data from a large introductory programming course to create formative assessment activities, integrated with Brightspace and Poll Everywhere.

The structure:
1. Collect student feedback (mid-semester surveys, common confusions from assignment grading, polling responses)
2. Upload the feedback data to NotebookLM as a source
3. Query: "Based on this feedback, what three concepts are students most struggling with? Generate a formative assessment activity targeting each."
4. Deploy the activities through the LMS and polling tool

This is NotebookLM as a *teaching analytics* tool — not generating content for students, but generating insight from student data that the teacher then acts on. It demonstrates the bounded-tool framework applied to course-improvement work, not just content production.

**Source(s):** pantry research file "Faculty Feedback Loops" section.

---

### Concept 3 — Two valid use cases, two different design principles

The chapter's opening case is structurally important: it shows two different higher-ed deployments that are both *correct* but for *different reasons*:

- **UW-Milwaukee Math 94 audio:** supplementary, opt-in, low-stakes. The design principle is *accessibility plus optionality* — the audio is there for students who benefit from it; the rest of the class is not penalized for skipping it. The audio does not replace any required work.
- **Monash self-testing:** active, diagnostic, formative. The design principle is *retrieval-practice integration* — the tool is the assignment, not a supplement to one. Engagement is required by design.

A faculty member needs to know which principle they are deploying. Mixing them — making the audio required and high-stakes, or making the self-testing optional — produces the failure modes Ch 5 named.

**Source(s):** pantry research file "Lecture Preparation and Accessibility" and "Self-Regulated Study" sections.

---

### Concept 4 — The April 2026 student notebook expansion (higher ed)

A higher-ed-specific operational fact: as of April 2026, higher-education students aged 18+ can create personal class notebooks grounded in educator-provided Classroom materials. This is the operational unlock for the Monash model to work at scale — students need to be able to instantiate their own notebooks from teacher-provided sources, not just consume teacher-built ones.

The pedagogical implication: undergraduate faculty can now design assignments that depend on individual student notebooks, not just shared class notebooks. This expands the design space beyond what was possible in K-12 (where individual student notebook creation is still gated).

**Source(s):** pantry research file "Google Classroom Integration" section.

---

## B. Domain examples and cases

### Case 1 — UW-Milwaukee Math 94 (accessibility companion)

Ed Price, TLT Consultant at UW-Milwaukee, generated podcast-style Audio Overviews of mathematical units, embedded them in Canvas via MyMedia with closed captions, made them optional. Students who listened reported greater comfort in high-stakes in-person sessions. Price's conclusion: works as a supplementary companion, not a replacement.

This case shows the *optional + accessibility-focused* design pattern. The audio is a *bridge* for students who otherwise would not engage with the dense materials. The rest of the class is unaffected.

### Case 2 — Monash self-testing companion (active design)

Monash configures Learning Guide as a self-testing study companion. Students load a notebook with course materials, invoke Learning Guide, answer diagnostic questions, receive feedback. The student is doing the work; the tool is the framework that structures the work.

This case shows the *active + integrated* design pattern. The tool is the assignment, not an addendum.

### Case 3 — NYU formative assessment feedback loop

(As described in concept 2 above.) NotebookLM analyzes student-feedback data, surfaces the three concepts students struggle with, generates formative assessment activities. The tool is used by the *instructor* on *student-generated data* to inform *future teaching*. Different again from the first two cases.

### Failure case — The default Audio Overview as undergraduate replacement

A faculty member assigns an Audio Overview of the reading and treats it as equivalent to the reading. Students who only listen score lower on subsequent assessments. The instructor concludes "NotebookLM doesn't work for college students." The actual failure: the assignment treated Audio Overview as substitution for reading. Same as the Ch 5 K-12 failure pattern, scaled up.

---

## C. Connections and dependencies

**Prerequisites:**
- Chapters 1-3 (design principle and operational fluency)
- Chapter 9 (research-style notebook for graduate students; complementary)
- Higher-ed teaching context: an upcoming undergraduate course

**Unlocks:**
- Chapter 11 (privacy and equity): higher-ed considerations differ from K-12
- Chapter 13 (administrator brief): the institutional deployment case for higher ed

**Adjacent chapter connections:**
- **Chapter 4:** K-12 teacher's analog of this chapter
- **Chapter 5:** Same active-engagement framework applied to higher-ed students
- **Chapter 9:** Research workflow; many graduate students span this chapter and Ch 9

---

## D. Current state of the field

**Settled:**
- Retrieval practice produces durable learning (Karpicke & Roediger 2008; Cepeda et al. 2008)
- Spaced repetition + retrieval practice via flashcards has empirical support (Karpicke & Bauernschmidt 2011)
- Higher-ed instructors are widely experimenting with AI-tool integration; institutional guidance is rapidly evolving

**Contested or emerging:**
- Whether AI-augmented self-testing produces equivalent or better outcomes than instructor-designed self-testing
- Whether Learning Guide's diagnostic question quality varies enough across disciplines to require discipline-specific configuration

**Key references:**
1. Karpicke & Roediger, *Science* (2008) — retrieval-practice foundation
2. Karpicke & Bauernschmidt, *Journal of Experimental Psychology: Learning, Memory, and Cognition* (2011) — spaced retrieval practice
3. pantry research file "Self-Regulated Study"
4. Monash University NotebookLM teaching guidance [verify URL]
5. NYU Teaching & Learning with Generative AI symposium materials (Oct 2025) [verify recordings or proceedings]

**Recent developments:**
- April 2026 student personal notebook expansion (higher ed)
- Shared notebook analytics (upcoming) — instructors see which files students query most

---

## E. Teaching considerations

**Where readers get stuck:**
- They invoke Learning Guide and let it explain rather than test. The configuration step ("test me on X, don't answer until I attempt") is what flips the mode.
- They mix design principles (optional+accessibility-focused with active+integrated). The chapter's two-case opening exists to keep these distinct.
- They expect AI-generated diagnostic questions to be uniformly high quality. They aren't — verification of the question set before assignment is still required.

**Analogies that work:**
- The athletic coach analogy: the coach doesn't perform the workout; the coach designs the workout and pushes the athlete to perform it. Learning Guide configured for self-testing is the coach mode.

**Exercises:**
- Create level: Identify one course where the self-testing model is applicable. Design the notebook, Learning Guide configuration, and student-facing instructions.
- Apply level: Configure Learning Guide for one upcoming class session. Pilot with one or two students before assigning to the full class.
- Evaluate level: Compare the question quality of an AI-generated diagnostic set against your own instructor-designed set. Identify which questions you would keep, modify, or cut.

---

## F. Library files relevant to this chapter

- `_lib_Teaching_for_Deeper_Learning_McTighe_Silver.md` — Backward design and formative assessment.
- `_lib_NEU_Global_Collaboration_Chatbot.md` — Pattern for higher-ed institutional AI deployment.
- `_lib_Humanitarians_AI_Course_Template.md` — Course-template pattern for the kind of structured curriculum that integrates NotebookLM well.
- `_lib_Co-Intelligence_Mollick.md` — Mollick's faculty-facing framing for AI use in teaching.

---

## G. Gaps and flags

- **FLAG:** The NYU faculty feedback loop case is described in pantry but the specific implementation details (which polling tool, what query template, how often refreshed) should be verified against the symposium materials before chapter publication.
- **GAP:** No controlled comparison yet of AI-self-testing vs. instructor-self-testing for the same course at the undergraduate level. The chapter argues from the underlying cognitive-science finding (retrieval-practice strength) plus the Monash exemplar.
- **GAP:** The chapter would benefit from a worked Learning Guide configuration example — the actual prompt sequence a faculty member uses to set up the self-testing mode. Pantry has the principle; the operational walkthrough is the chapter author's work.
