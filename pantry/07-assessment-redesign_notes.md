# Research Notes: Chapter 7 — Assessment Redesign: The Part You Can't Skip

**Source:** TIKTOC.md chapter entry
**Notes file:** 07-assessment-redesign_notes.md
**Corresponding chapter:** chapters/07-assessment-redesign.md (not yet written)
**Generated:** 2026-05-19

---

## Chapter summary (from TIKTOC.md)

**One-line:** Any assessment a student can complete by generating a NotebookLM output and submitting it is an assessment you need to redesign.

**Problem this chapter solves:** Teachers know they need to redesign assessments for the AI era but lack a concrete framework that is more learning-aligned rather than more surveillance-intensive.

**Learning outcomes:**
1. (Evaluate) Apply the three-question audit to an existing assessment.
2. (Create) Redesign one assessment using source-verification, oral defense, or AI-critique frameworks.
3. (Analyze) Explain why timestamped version control in Google Docs is a pedagogical tool, not only a surveillance one.

**Opening:** Backward design reframe. The question is not "how do I catch students using AI?" It is "what learning am I trying to assess, and does this assessment measure it?"

---

## A. Conceptual foundations

### Concept 1 — The three-question assessment audit

The chapter's central diagnostic tool:

1. **What is the learning goal of this assessment?** (Stated as a student action, not a topic.)
2. **Can a NotebookLM output substitute for demonstrating that learning?** (Honest answer.)
3. **If yes — is that substitution the goal?** (If yes, the assessment is fine. If no, it requires redesign.)

For a take-home essay assessment with the goal "demonstrate understanding of the French Revolution," NotebookLM can produce a passable essay from uploaded primary sources — meaning the assessment fails Question 2. The student doesn't have to *understand* the Revolution; they have to *generate text* about it. Redesign is required.

For a literature comprehension quiz with the goal "recognize plot events in *To Kill a Mockingbird*," NotebookLM can answer the quiz. But if the goal is *recognition* (Bloom's Remember level), substitution doesn't matter — the student running NotebookLM has still done a recognition task. Question 3 answers "yes, that substitution is the goal." The assessment may be fine even if NotebookLM-friendly.

The audit's value is *not* its complexity; it is its enforcement. Most assessments fail Question 2 and the teacher hasn't checked.

**Source(s):** Synthesis of backward design (Wiggins & McTighe 2005) and the pantry research file "Assessment Redesign" section.

---

### Concept 2 — The four redesign frameworks

When an assessment fails the audit, the chapter offers four redesign patterns:

1. **Source-verification.** Student must compare AI output against original sources and identify what is missing, wrong, or oversimplified. The artifact is a critique, not a summary. (UIC's recommended pattern.)
2. **Oral defense.** Student submits the written work AND defends it verbally — explaining reasoning, source choices, what they would change. The AI cannot show up to the defense.
3. **AI-critique.** Student is required to generate the AI output, then deconstruct it — identifying its weaknesses, what it gets wrong, what it overconfidently asserts.
4. **Process documentation.** Student submits not the final artifact but the *iteration history* — drafts, dead ends, decisions made, prompts tried. Google Docs version history makes this verifiable.

All four put production work the AI cannot perform at the center of the assessment.

**Source(s):** pantry research file "From Lecture to Experience Design" and "Assessment Redesign" sections.

---

### Concept 3 — Why banning AI is not an assessment strategy

The temptation: solve the AI-substitution problem by banning AI use. This is not an assessment strategy for two reasons:

1. **Enforceability.** Take-home assessments cannot reliably distinguish AI-assisted from human-only work. AI-detection tools have well-documented false-positive rates that disadvantage non-native English speakers and certain writing styles. A policy that depends on enforcement that doesn't work is not a policy.
2. **Misalignment with learning goals.** If the assessment's stated learning goal includes synthesis, evaluation, or argument construction, the AI-assisted version of those skills is what students will actually use in professional life. Assessing the pure-human version while preparing students for an AI-augmented world is the opposite of authentic assessment.

The chapter's argument is *not* that AI use should be encouraged in all assessments. It is that "ban it" is a policy choice that needs the same justification as "design it in" — and most contexts can't justify the ban.

**Source(s):** MDPI 2025 (pantry research file); critical perspectives summarized in pantry research; the literature on AI-detection false positives [verify specific studies — Liang et al. 2023 on GPT detector bias is a key citation].

---

### Concept 4 — Google Docs version control as pedagogical tool

Google Docs auto-saves a granular revision history. For assessments built on Google Docs:
- Sudden large blocks of text appearing at once (copy-paste from elsewhere, possibly AI)
- Iterative typing with backspaces, edits, additions (human composition pattern)
- The timeline of when work was done relative to assignment deadline

The pedagogical (not surveillance) framing: version history lets the teacher see *the student's process*, not just the product. A student who has clearly struggled, revised, and built toward the final draft has done the cognitive work. A student whose document went from blank to finished in 4 minutes has not — regardless of whether AI was involved.

The chapter's argument: this is feedback data more than catch-the-cheater data. Use it to identify students who are struggling silently (no iteration, panic-typing on deadline day) as much as students who are taking shortcuts.

**Source(s):** pantry research file; Google Docs revision history documentation.

---

## B. Domain examples and cases

### Case 1 — The take-home essay redesign

Original assessment: 1,500-word essay on the causes of the American Civil War. Take-home, one week.

Audit:
- Goal: demonstrate causal reasoning about complex historical events.
- AI substitution possible? Yes — NotebookLM can produce a passable 1,500-word essay from uploaded primary sources.
- Is substitution the goal? No — the goal is the *student's* causal reasoning.

Redesign options:
- **Oral defense version:** Student submits the essay. In a 5-minute one-on-one with the teacher, the student is asked: "What would change your argument? Why did you weight cause X above cause Y? What's the strongest objection to your thesis?"
- **AI-critique version:** Student generates an AI-written essay AND a human-written essay. Submits both with a third document analyzing where the AI version is weaker and why.
- **Process documentation version:** Student submits draft history with annotations explaining why each revision was made.

Any of the three redesigns retains the learning goal while making AI substitution either harder to fake or built into the assignment honestly.

### Case 2 — The Monash self-testing model (applied to assessment)

(Pantry research file.) Monash University configures NotebookLM as a *self-testing companion* — students use it to quiz themselves, not to receive explanations. The assessment becomes the student's own self-assessment performance, and the teacher's role is to design diagnostic prompts that the AI delivers and the student answers. This is a Ch 10 case (higher ed) that this chapter can reference as proof-of-concept.

### Failure case — Surveillance-only redesign

A teacher responds to AI by requiring all assessments in proctored in-class conditions with no AI access. Short-term: cheating is reduced. Long-term: the assessment now measures what students can do under artificial conditions that don't match the conditions of authentic professional work. The teacher is also signaling distrust as the primary classroom relationship.

The chapter argues this is a legitimate option only for assessments where the *artificial-condition skill* is genuinely the learning goal (e.g., licensure-style exams). For most learning, it produces accurate-but-not-useful assessment data.

---

## C. Connections and dependencies

**Prerequisites:**
- Chapters 1-3 (the design principle and operational fluency)
- Chapter 5 (active-engagement assignment design; this chapter scales the same logic to summative)
- Familiarity with backward design (Wiggins & McTighe) — chapter should briefly summarize, library file provides depth

**Unlocks:**
- Chapter 8 (academic integrity policy) — assessment design is the operational version of policy
- Chapter 10 (higher-ed course design) — Monash model is the higher-ed application

**Adjacent chapter connections:**
- **Chapter 5:** Formative version of this chapter's argument
- **Chapter 8:** Integrity policy that codifies the assessment design choices made here
- **Chapter 10:** Self-testing assessment model in higher ed

---

## D. Current state of the field

**Settled:**
- AI tools can produce passable student work in most take-home text-generation assessments
- AI-detection tools have unacceptable false-positive rates for general deployment (Liang et al. 2023 on GPT detector bias; OpenAI's own classifier withdrawn in 2023)
- Backward design (Wiggins & McTighe 2005) remains the canonical framework for working from learning goal to assessment to instruction

**Contested or emerging:**
- The right *default* AI use policy in assessment (some institutions: permit with disclosure; some: prohibit; some: require)
- Whether oral defense scales: the time cost in large classes is real
- Whether process documentation produces valid assessment data when students can simulate the process

**Key references:**
1. Wiggins & McTighe, *Understanding by Design* (2005)
2. McTighe & Silver, *Teaching for Deeper Learning* (library file)
3. Liang, Yuksekgonul, Mao, Wu, Zou, "GPT detectors are biased against non-native English writers," *Patterns* (2023)
4. pantry research file "Assessment Redesign" section
5. Monash University Learning Guide documentation

**Recent developments:**
- 2024-2025 — major US universities (Harvard, MIT, Penn, others) issued explicit AI assessment guidance documents; these are now reference templates
- 2025 — wave of K-12 districts updating academic integrity policies to address AI specifically

---

## E. Teaching considerations

**Where readers get stuck:**
- Believing redesign means more surveillance. The chapter's central reframe: redesign means *more authentic assessment*, where AI use is either irrelevant (because the goal is fine with substitution) or designed-in honestly.
- Believing redesign requires a new assessment for every existing assignment. False — many assessments pass the audit unchanged. Audit first; redesign only what fails.
- Believing oral defense is the only honest answer. It's one of four; pick the one that fits the course's logistics.

**Analogies that work:**
- The home repair analogy: don't replace the whole roof because one shingle is loose. Audit the assessment portfolio; redesign the failures; leave the passes alone.

**Exercises:**
- Evaluate level: Run the three-question audit on 5 current assessments. Flag the ones that fail.
- Create level: Take one failed assessment. Redesign it using one of the four frameworks.
- Analyze level: Examine the Google Docs revision history of one of your students' previous submissions. What does the timeline tell you about how they worked?

---

## F. Library files relevant to this chapter

- `_lib_Teaching_for_Deeper_Learning_McTighe_Silver.md` — Backward design as the structural foundation. Direct reading for this chapter's spine.
- `_lib_Co-Intelligence_Mollick.md` — On "what the AI changes about authentic assessment" — Mollick's frame on the centaur model is consistent with the chapter's design-in logic.
- `_lib_The_Digital_Delusion_Horvath.md` — The skeptical view; useful for the chapter's counter-argument against banning.

---

## G. Gaps and flags

- **FLAG:** AI-detection tool reliability and bias are a moving target. The Liang et al. 2023 finding is canonical now, but new detector generations claim better performance. Verify current evidence before publication.
- **GAP:** The chapter would benefit from 2-3 worked examples of process-documentation assessments in different disciplines. Pantry doesn't have these explicitly; author may need to construct them.
- **GAP:** Oral defense at scale (large classes) is a real logistical problem the chapter should address — even briefly. The Monash and NYU models in pantry are partial answers; full treatment would need author judgment on what works in a 200-student section.
- **FLAG:** "Banning AI is not an assessment strategy" is a deliberately contestable claim that some faculty will dispute. Chapter should explicitly note the disagreement and provide the strongest counter-argument before the rebuttal.
