# Chapter 7 — Assessment Redesign: The Part You Can't Skip

*Why the detection question is the wrong question, and what the right one produces.*

---

There is a question that, once you ask it precisely, dissolves a problem that seemed intractable.

In the fall of 2024, teachers across the country were asking a version of the same question: *how do I catch students using AI?* They ran submissions through detection tools. They got inconsistent verdicts. They escalated to proctored conditions, in-class writing days, surveillance regimes. By the end of the semester, most of them had caught no one definitively, lost weeks of instruction to enforcement, and noticed that the students they trusted most were the ones most upset by the policy.

The question *how do I catch students using AI?* has no satisfying answer. The detection tools don't work reliably enough to base policy on. The 2023 study by Liang and colleagues in *Patterns* documented that AI detectors are systematically biased against non-native English writers — the tools flag honest student work at disproportionate rates for specific student populations. OpenAI withdrew its own classifier the same year, citing low accuracy. The trajectory of evidence since then has been toward *less* confidence in detection, not more.

But here is the thing about a question that has no good answer: sometimes the question is wrong. Not unanswerable — wrong. And when the question is wrong, the move is not to work harder on the answer. The move is to find the right question.

The right question is: *what learning am I actually trying to assess, and does this assessment measure it?*

That question has a good answer. This chapter is the answer.

---

## What the audit reveals

An assessment exists to produce evidence of learning. That is the entire purpose. Wiggins and McTighe's backward design framework — which most teachers have encountered in some form — makes this explicit: you start with the learning goal, derive the evidence you need to confirm the goal was met, and then design the activity that produces the evidence. The assessment is the middle step. It is not the learning itself; it is the measurement of the learning.

When you ask *can a NotebookLM output substitute for demonstrating this learning?*, you are asking a backward-design question. You are asking whether the evidence the assessment produces can be generated without the learning having occurred. If it can, the assessment is not measuring what it says it's measuring. That is a design flaw. The AI did not create the flaw. The AI exposed it.

The three-question audit makes this concrete:

**First: what is the learning goal of this assessment?** State it as a student action — something the student can *do* as a result of having learned. Not "understanding of the French Revolution." Yes: "the student constructs a defensible causal argument about a major historical event." The difference matters because the second formulation tells you what evidence you need, and the first one doesn't.

**Second: can a NotebookLM output substitute for demonstrating that learning?** Be honest. Many assessments — a five-paragraph essay on a primary source the student has uploaded — can be substituted, completely, in two minutes. If the honest answer is yes, you have found a design flaw.

**Third: is the substitution the goal?** For some assessments, yes. A recognition quiz where the goal is *identify key vocabulary* doesn't require the work to be human-generated; both a student and an AI tool can demonstrate the recognition. The substitution is fine because the goal doesn't depend on the process. For most assessments where the goal includes synthesis, argument, or judgment, the answer is no — and the assessment requires redesign.

The audit's value is not its sophistication. It is its enforcement. Most assessments have never been audited this way. Running the audit on five assessments takes twenty minutes. The number that fail Question 2 is typically higher than expected.

| Assessment | Learning goal (as student action) | AI substitution possible? | Substitution is the goal? | Verdict |
|---|---|---|---|---|
| Five-paragraph essay on primary source | Construct an argument with evidence from the source | Yes — NotebookLM can produce a passable essay in two minutes | No — the student's reasoning is what's being assessed | **Redesign required** |
| Take-home reading quiz | Recognize key terms and recall facts | Yes — open-book recognition is the AI's strongest mode | Yes — if the goal is genuinely recognition, AI assistance doesn't undermine it | **Audit passes; no redesign needed** |
| Oral thesis defense | Defend reasoning under live questioning | No — the AI cannot show up to defend an essay | No — the goal is the student's reasoning under pressure | **Audit passes; format is already redesign-equivalent** |
| Process-documented research draft | Iterate, revise, and ground claims in source material | Substitution produces a worse artifact — finished text without revision history reveals absence of work | No — the goal is the process | **Audit passes; the documentation IS the redesign** |

*The audit forces the backward-design question that most assessments have never faced. Only assessments that fail Q2 without passing Q3 require redesign.*
---

## Why banning doesn't work

Before describing the redesigns, the chapter needs to address the temptation to solve this by prohibition. Ban AI. Problem solved.

Two reasons this fails, and they operate at different levels.

The first is enforceability. A policy that depends on detection tools that don't reliably work is not a policy. It is a posture. The detection problem is structurally hard: distinguishing AI-generated text from human-generated text in a domain where both draw on the same linguistic patterns is a statistical problem, and the margin is not wide enough for the error rates the tools currently produce. The Liang finding about non-native English writers is not an edge case — it is the central case, because the students most likely to write in ways that trigger the detectors are the students whose writing least resembles the training-data baseline for fluent native English. A ban enforced by biased tools produces disproportionate false accusations against the students with the least institutional protection. This is not a theoretical risk. It happened in 2023 and 2024, repeatedly.

The second is misalignment with learning goals. If the stated learning goal includes synthesis, evaluation, or argument construction, then the AI-assisted version of those skills is what students will exercise in professional life. Teaching students to perform synthesis without AI, then releasing them into a world where synthesis happens with AI, is the opposite of authentic assessment. The authentic question is not whether AI was used. It is whether learning occurred and whether the student can demonstrate it. An assessment that catches AI use by requiring the absence of AI may catch nothing about learning at all.

The chapter is not arguing that AI use should be required or encouraged in every assessment. It is arguing that ban-and-detect is a design choice that requires justification — and the justification requires showing that the learning goal genuinely depends on human-only production, and that the enforcement mechanism reliably distinguishes human from AI. In most contexts, neither condition holds.

![Timeline of AI detection tool reliability 2022–2025 ](images/07-assessment-redesign-fig-01.png)
*Figure 7.1 — Timeline of AI detection tool reliability 2022–2025 *

---

## The four redesign frameworks

When an assessment fails the audit — when a NotebookLM output can substitute for demonstrating the stated learning goal, and the substitution is not the point — four redesign patterns recur across published faculty guidance.

**Source-verification.** The student compares the AI output against the original source materials, identifying what is missing, oversimplified, or wrong. The artifact is a *critique*, not a *summary*. A student who uploads the source and submits an AI-generated summary without reading the source cannot produce a substantive critique — the shortcut leads to an empty document. The engaged path leads to a document that demonstrates the student read and understood the source. The assessment now measures what it was supposed to measure.

**Oral defense.** The student submits the written work and defends it verbally — explaining reasoning, source choices, what they would revise. Five minutes, one-on-one with the instructor or a TA. The AI cannot show up to the defense. The cost is instructor time; for a class of thirty, that is two and a half hours. Compare that against the hours lost to detection disputes, the emotional cost to falsely accused students, and the instruction time consumed by the surveillance regime. The oral defense is not cheap. It is cheaper than the alternative.

**AI-critique.** The student is required to generate an AI output and then deconstruct it — identifying weaknesses, errors, overconfident assertions, what the source material contradicts. The artifact builds the metacognitive skill that the integrity policy was supposed to encourage anyway. The student who can identify where AI reasoning fails has demonstrated more sophisticated engagement with the material than the student who simply wrote a compliant essay.

**Process documentation.** The student submits the iteration history — drafts, dead ends, revision decisions, prompts tried. Google Docs version history makes this verifiable. The grading rubric shifts from the polish of the final product to the quality of the reasoning visible in the process. A student who revised substantively and shows it in the document history has done the cognitive work. A student whose document went from blank to finished in four minutes has not.

| Framework | What the student produces | What AI cannot do | Instructor time cost | Best fit for |
|---|---|---|---|---|
| Source-verification | Critique of AI output identifying what is missing, oversimplified, or wrong | Identify what was omitted from itself | Standard grading — no extra | Reading-heavy courses; humanities; any context where source-text is the spine |
| Oral defense | Verbal answers to instructor questions about reasoning, source choices, what they would change | Show up to the defense | High — 5 min × student count | Small seminars; capstone projects; high-stakes summative assessment |
| AI-critique | Both an AI-generated artifact and a student deconstruction of its weaknesses | Critique itself with domain knowledge it doesn't have | Standard grading | Courses that already include AI literacy; advanced students |
| Process documentation | Iteration history (drafts, revisions, decision notes) submitted alongside the final artifact | Simulate iterative process at scale | Light — Google Docs revision history is auto-captured | Writing-intensive courses; any context where the process is the learning |
All four share a structural property: the AI can help with some of the work, but the work that demonstrates learning requires the student to be present and engaged. This is the correct relationship between AI and assessment. Not prohibition — design.

---

## Google Docs version history as a window into process

For assessments built on Google Docs, the auto-save revision history creates a record of how the document was produced. Large blocks of text appearing at once suggest copy-paste. Iterative typing with revisions and backtracking shows human composition under construction. The timeline shows when work was done relative to the deadline.

The chapter's position on this record — and it is worth stating directly — is that revision history is feedback data, not surveillance data. The distinction is not semantic. It is a decision about what you are trying to do with the information.

Surveillance use: find students who pasted in AI text and accuse them. This use has the same problem as the detection tools — the signal is imperfect, the false-positive risk is real, and the intervention is adversarial.

Feedback use: identify students who are struggling silently. A student who typed everything in a frantic session the night before the deadline, with no iteration, is a student who may be in trouble — not necessarily because they used AI, but because they didn't have enough time or didn't understand the assignment early enough to build toward it. The version history tells you that. The right response is to reach out and ask if they are okay. The version history is not a polygraph. It is a window into student work patterns, and work patterns are useful information for teaching.

This reframe — from surveillance to support — is available in any Google Docs-based course right now, without new tools or new policies. It requires only the decision to use the information that way.

![Side-by-side comparison of the same Google Docs revision-history pattern (a blank document followed by a sudden large block of text on deadline day) interpreted under two frames: surveillance (flag for investigation) and support (reach out with help question).](../images/07-assessment-redesign-fig-01.png)
*Figure 7.1 — Same data. Two interpretations.*

---

## The redesign in practice

Start with the audit. Pick five assessments from your current course. For each, ask the three questions. Flag the ones where a NotebookLM output could substitute and the substitution is not the learning goal. That list is your redesign queue.

Take the top item on the queue. Pick one framework. Pilot it with one class section before scaling.

Here is what that looks like for a specific case. A high school history teacher uses a 1,500-word take-home essay on the causes of the American Civil War. The audit: the goal is causal reasoning about a complex historical event. AI substitution is possible in three minutes with uploaded primary sources. Substitution is not the goal. The assessment fails.

Three plausible redesigns:

The oral defense version keeps the essay submission and adds a five-minute one-on-one. The instructor asks: *"What would change your argument? Why did you weight cause X above cause Y? What is the strongest objection to your thesis?"* Those questions cannot be answered by an AI that didn't write a specific essay. The student who wrote it can answer them. The student who submitted something they didn't write cannot, or answers in ways that reveal the gap.

The AI-critique version requires the student to generate an AI-written essay on the same prompt and submit both, with a third document analyzing where the AI version is weaker and why — specifically, with evidence from the primary sources that the AI essay missed or misread. The three-artifact submission is harder to fake than a single essay, and the critique artifact demonstrates exactly the close-reading skill the original essay was supposed to demonstrate.

The process documentation version replaces the polished essay with an annotated revision history. The student submits two pages of annotated drafts explaining why each revision was made. The grading rubric evaluates the quality of the reasoning visible in the process. Polish is no longer the metric.

None of these is perfect. The oral defense doesn't scale to 200 students without modification — small-group defenses, TA-led defenses, or randomized sampling where any student can be called. The AI-critique can be meta-shorted (student generates both the essay and the critique with AI), which requires adding a source-grounding check: the critique must cite specific passages from the primary sources that the AI essay missed. The process documentation can in principle be faked, though simulating a realistic iterative work pattern is substantially more labor than doing the work.

The honest comparison is not against a perfect redesign. It is against the alternative: a surveillance regime that doesn't work, produces false accusations at disproportionate rates against specific student populations, loses instruction time, and measures compliance rather than learning.

| Class size | Time available per student | Primary learning goal | Recommended framework | Modification needed at scale |
|---|---|---|---|---|
| Small seminar (≤25) | 5+ min per student | Reasoning, argument, judgment | Oral defense | None — runs at native scale |
| Medium lecture (25–100) | 1–3 min per student | Synthesis, argument | Source-verification or AI-critique | TA-graded with sampled instructor review |
| Large lecture (100+) | <1 min per student | Recognition, application | Process documentation + auto-checked quizzes | Revision-history sampling; randomized oral-defense calls for a subset |

*The right redesign depends on context. The audit question is the same regardless of class size; the framework choice is not.*
---

## What this chapter established

The question *how do I catch students using AI?* is wrong. The right question is *what learning am I trying to assess, and does this assessment measure it?* The three-question audit applies that question to any existing assessment. Most assessments have never faced it. Many fail.

When an assessment fails, four redesign frameworks put work the AI cannot perform at the center of the assessment: source-verification, oral defense, AI-critique, and process documentation. All four are gradable. None requires detection software. Google Docs version history is useful as feedback data — a window into student work patterns for supportive intervention — and corrosive as surveillance data. The ban-and-detect posture depends on tools that don't work reliably enough to build policy on.

Chapter 8 is about writing the academic integrity policy that the redesigned assessment framework implies — one that is defensible to students, parents, and administrators, and honest about what the evidence actually supports.

---

## Key terms

- **Three-question audit** — Goal stated as student action? AI substitution possible? Substitution is the goal? The audit before every assessment.
- **Source-verification** — Redesign framework where the student critiques an AI output against the original source. Artifact is a critique.
- **Oral defense** — Student submits written work and defends it verbally. AI cannot attend the defense.
- **AI-critique** — Student generates and deconstructs the AI output, identifying failures and gaps against the source material.
- **Process documentation** — Student submits iteration history with annotations. Grading shifts from product polish to reasoning quality.
- **Detection-based policy** — A policy whose enforcement depends on tools with unacceptable false-positive rates. A posture, not a strategy.
- **Backward design** — Wiggins and McTighe's framework: start from the learning goal, derive the evidence, design the activity. The structural lever for all four redesigns.

---

## LLM Exercises

*Use a language model with access to current literature on educational assessment, academic integrity, and AI detection to complete the following.*

**Warm-up**

1. *(Verify the detection evidence)* The chapter cites the Liang et al. 2023 study in *Patterns* and OpenAI's classifier withdrawal as anchors for the claim that detection tools are unreliable. Ask a language model to locate both references and confirm the key findings. Then ask it to identify any high-quality studies published since that report detection accuracy above 95% with documented false-positive rates below 1%. Report what it finds. If no such studies exist, state that as the finding.

2. *(Audit a real assessment)* Take one assessment from your current course and apply the three-question audit. Ask a language model to help you state the learning goal as a student action verb — give it your current assessment description and ask it to rewrite the goal in the form "the student [action verb] [what]." Evaluate whether the rewrite captures what you actually want to measure or whether it reveals a gap between your stated goal and your real one.

**Application**

3. *(Framework selection)* Describe a specific assessment you want to redesign to a language model — the subject, the learning goal, the class size, the time constraints. Ask it to recommend which of the four frameworks fits best and why, and what modifications would be needed at your specific scale. Evaluate the recommendation against the chapter's decision matrix. Where does the model's reasoning diverge from the chapter's, and which argument is stronger?

4. *(Meta-shortcut stress test)* The chapter notes that each redesign framework has a meta-shortcut — a way students could attempt to complete the redesigned assessment without doing the intended work. Ask a language model to identify the most plausible meta-shortcut for each of the four frameworks, then design one additional requirement for each that would close the shortcut. Evaluate whether the additional requirement changes the nature of the assessment or only its integrity properties.

**Synthesis**

5. *(Backward design audit at scale)* Ask a language model to generate five sample assessments across different subjects and grade levels, then apply the three-question audit to each. For each one that fails, ask the model to propose a redesign using the most appropriate framework. Then evaluate: which redesigns required the most instructor judgment that the model couldn't supply? What does that tell you about the limits of AI assistance in assessment design itself?

**Challenge**

6. *(The honest student problem)* The chapter ends with an unresolved question: how do you handle the student who used AI honestly and well, before any policy existed, and now feels mistrusted by the new regime? Ask a language model to draft a response to that student — a policy statement or a direct explanation — that is honest about the reasons for the redesign without implying that past AI use was wrong. Evaluate the draft: does it hold the tension between supporting legitimate AI use and requiring demonstrated learning, or does it collapse toward one side? Revise where it collapses.

---

## Aging note

AI-detection tool reliability claims will continue to evolve. The pattern since 2022 — new tool launches, bias studies follow, modifications or withdrawal — has been consistent. Re-verify the Liang et al. citation and look for high-*N* evidence before reprint. The structural argument is stable: designing assessments around the assumption that detection works is fragile design, and the fragility is a property of the detection problem, not of any particular tool.

## Prompts

Use these prompts with Claude to generate interactive D3 v7 versions of the
figures in this chapter. Each produces a standalone HTML file you can open
in a browser and modify freely.

**Prerequisites:** Load `brutalist/CLAUDE.md` and `brutalist/DESIGN.md` into
your Claude project context before using these prompts. They define the stack,
naming conventions, color system, and typography the figures use.

---

### Figure 7.1 — Timeline of AI detection tool reliability 2022–2025 

Create a standalone D3 v7 HTML file for Figure Timeline of AI detection tool reliability 2022–2025 . Use the CDN https://cdnjs.cloudflare.com/ajax/libs/d3/7.9.0/d3.min.js, inline CSS, ResizeObserver redraw, SVG role="img", aria-labelledby, title, and desc. Build the figure from this structural brief: Timeline of AI detection tool reliability 2022–2025 — horizontal axis: date; vertical axis: confidence in tool accuracy (qualitative). Key events marked: GPTZero launch (Jan 2023), Liang et al. bias study in Patterns (Jul 2023), OpenAI classifier withdrawal (Jul 2023), Turnitin AI detection launch and subsequent accuracy disputes (2023–2024), continued bias findings (2024–2025). Trend line slopes downward. Caption: Each cycle follows the same pattern — launch, bias finding, modification or withdrawal. The trajectory of evidence has been toward less confidence, not more.. Use the described data shape and labels; when exact values are not supplied, use plausible illustrative values that preserve the relationships in the brief. Use a zero baseline for bars or areas, direct labels where possible, and annotations named in the brief. Use only DESIGN.md color variables and the required serif/

> Reference implementation: `d3/07-assessment-redesign-fig-01.html`
