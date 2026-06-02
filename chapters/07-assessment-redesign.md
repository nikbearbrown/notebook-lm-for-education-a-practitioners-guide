# Chapter 7 — Assessment Redesign: The Part You Can't Skip

*Why the detection question is the wrong question, and what the right one produces.*

---

There is a question that, once you ask it precisely, dissolves a problem that seemed intractable.

In the fall of 2024, teachers across the country were asking a version of the same question: how do I catch students using AI? They ran submissions through detection tools. They got inconsistent verdicts. They escalated to proctored conditions, in-class writing days, surveillance regimes. By the end of the semester, most had caught no one definitively, lost weeks of instruction to enforcement, and noticed that the students they trusted most were the ones most upset by the policy.

The question *how do I catch students using AI?* has no satisfying answer. The detection tools do not work reliably enough to base policy on. A 2023 study by Liang and colleagues in *Patterns* documented that AI detectors are systematically biased against non-native English writers — the tools flag honest student work at disproportionate rates for specific student populations. OpenAI withdrew its own classifier the same year, citing low accuracy. The trajectory of evidence since then has moved toward less confidence in detection, not more.

But here is the thing about a question that has no good answer: sometimes the question is wrong. Not unanswerable — wrong. And when the question is wrong, the move is not to work harder on the answer. The move is to find the right question.

The right question is: what learning am I actually trying to assess, and does this assessment measure it?

That question has a good answer. This chapter is the answer.

---

## What the Audit Reveals

An assessment exists to produce evidence of learning. That is the entire purpose. Wiggins and McTighe's backward design framework makes this explicit: you start with the learning goal, derive the evidence you need to confirm the goal was met, and design the activity that produces the evidence. The assessment is the middle step. It is not the learning itself; it is the measurement of the learning.

When you ask "can a NotebookLM output substitute for demonstrating this learning?", you are asking a backward-design question. You are asking whether the evidence the assessment produces can be generated without the learning having occurred. If it can, the assessment is not measuring what it says it is measuring. That is a design flaw. The AI did not create the flaw. The AI exposed it.

The three-question audit makes this concrete.

**First: what is the learning goal of this assessment?** State it as a student action — something the student can *do* as a result of having learned. Not "understanding of the French Revolution." Yes: "the student constructs a defensible causal argument about a major historical event." The difference matters because the second formulation tells you what evidence you need and the first one does not.

**Second: can a NotebookLM output substitute for demonstrating that learning?** Be honest. Many assessments — a five-paragraph essay on a primary source the student has uploaded — can be substituted completely in two minutes. If the honest answer is yes, you have found a design flaw.

**Third: is the substitution the goal?** For some assessments, yes. A recognition quiz where the goal is "identify key vocabulary" doesn't require the work to be human-generated; both a student and an AI tool can demonstrate the recognition. The substitution is fine because the goal doesn't depend on the process. For most assessments where the goal includes synthesis, argument, or judgment, the answer is no — and the assessment requires redesign.

The audit's value is not its sophistication. It is its enforcement. Most assessments have never been audited this way. Running the audit on five assessments takes twenty minutes. The number that fail the second question is typically higher than expected.

<!-- → [TABLE: Four sample assessments through the three-question audit — columns: assessment type, learning goal as student action, AI substitution possible, substitution is the goal, verdict. Caption: Only assessments that fail Q2 without passing Q3 require redesign. The audit forces the backward-design question that most assessments have never faced.] -->

---

## Why Banning Doesn't Work

Before describing the redesigns, the chapter needs to address the temptation to solve this by prohibition. Ban AI. Problem solved.

Two reasons this fails, operating at different levels.

The first is enforceability. A policy that depends on detection tools that don't reliably work is not a policy. It is a posture. The detection problem is structurally hard: distinguishing AI-generated text from human-generated text in a domain where both draw on the same linguistic patterns is a statistical problem, and the margin is not wide enough for the error rates the tools currently produce. The Liang finding about non-native English writers is not an edge case — it is the central case, because the students most likely to write in ways that trigger the detectors are the students whose writing least resembles the training-data baseline for fluent native English. A ban enforced by biased tools produces disproportionate false accusations against the students with the least institutional protection. This is not a theoretical risk. It happened in 2023 and 2024, repeatedly.

The second is misalignment with learning goals. If the stated learning goal includes synthesis, evaluation, or argument construction, then the AI-assisted version of those skills is what students will exercise in professional life. Teaching students to perform synthesis without AI, then releasing them into a world where synthesis happens with AI, is the opposite of authentic assessment. The authentic question is not whether AI was used. It is whether learning occurred and whether the student can demonstrate it. An assessment that catches AI use by requiring the absence of AI may catch nothing about learning at all.

The chapter is not arguing that AI use should be required or encouraged in every assessment. It is arguing that ban-and-detect is a design choice that requires justification — and the justification requires showing that the learning goal genuinely depends on human-only production, and that the enforcement mechanism reliably distinguishes human from AI. In most contexts, neither condition holds.

<!-- → [FIGURE: Timeline of AI detection tool reliability 2022–2025 — showing tool launches, subsequent bias studies, and withdrawals or modifications. Caption: The pattern since 2022 has been consistent: new tool launches, bias studies follow, withdrawal or hedged accuracy claims replace the original ones. Designing enforcement around the assumption that detection works is fragile design.] -->

---

## The Four Redesign Frameworks

When an assessment fails the audit — when a NotebookLM output can substitute for demonstrating the stated learning goal, and the substitution is not the point — four redesign patterns recur across published faculty guidance.

**Source-verification.** The student compares the AI output against the original source materials, identifying what is missing, oversimplified, or wrong. The artifact is a critique, not a summary. A student who uploads the source and submits an AI-generated summary without reading the source cannot produce a substantive critique — the shortcut leads to an empty document. The engaged path leads to a document that demonstrates the student read and understood the source. The assessment now measures what it was supposed to measure.

**Oral defense.** The student submits the written work and defends it verbally — explaining reasoning, source choices, what they would revise. Five minutes, one-on-one with the instructor or a TA. The AI cannot show up to the defense. The cost is instructor time; for a class of thirty, that is two and a half hours. Compare that against the hours lost to detection disputes, the emotional cost to falsely accused students, and the instruction time consumed by the surveillance regime. The oral defense is not cheap. It is cheaper than the alternative.

**AI-critique.** The student is required to generate an AI output and then deconstruct it — identifying weaknesses, errors, overconfident assertions, what the source material contradicts. The artifact builds the metacognitive skill that the integrity policy was supposed to encourage anyway. A student who can identify where AI reasoning fails has demonstrated more sophisticated engagement with the material than a student who simply wrote a compliant essay.

**Process documentation.** The student submits the iteration history — drafts, dead ends, revision decisions, prompts tried. Google Docs version history makes this verifiable. The grading rubric shifts from the polish of the final product to the quality of the reasoning visible in the process. A student who revised substantively and shows it in the document history has done the cognitive work. A student whose document went from blank to finished in four minutes has not.

All four share a structural property: the AI can help with some of the work, but the work that demonstrates learning requires the student to be present and engaged. This is the correct relationship between AI and assessment. Not prohibition — design.

<!-- → [TABLE: Four redesign frameworks — columns: framework, what the student produces, what AI cannot do, instructor time cost, best fit for. Caption: The right redesign depends on context. The audit question is the same regardless of class size; the framework choice is not.] -->

---

## Google Docs Version History as a Window into Process

For assessments built on Google Docs, the auto-save revision history creates a record of how the document was produced. Large blocks of text appearing at once suggest copy-paste. Iterative typing with revisions and backtracking shows human composition under construction. The timeline shows when work was done relative to the deadline.

The chapter's position on this record is worth stating directly: revision history is feedback data, not surveillance data. The distinction is not semantic. It is a decision about what you are trying to do with the information.

Surveillance use: find students who pasted in AI text and accuse them. This use has the same problem as the detection tools — the signal is imperfect, the false-positive risk is real, and the intervention is adversarial. A student who drafts in a separate document and pastes their own work into Google Docs at the end looks identical to a student who pasted AI text. The signal does not distinguish them.

Feedback use: identify students who are struggling silently. A student who typed everything in a frantic session the night before the deadline, with no iteration, is a student who may be in trouble — not necessarily because they used AI, but because they didn't have enough time or didn't understand the assignment early enough to build toward it. The version history tells you that. The right response is to reach out and ask if they are okay. The version history is not a polygraph. It is a window into student work patterns, and work patterns are useful information for teaching.

<!-- → [FIGURE: Side-by-side comparison of the same Google Docs revision-history pattern — a blank document followed by a sudden large block of text on deadline day — interpreted under two frames: surveillance (flag for investigation) vs. support (reach out with a help question). Caption: Same data. Two interpretations. The frame you choose is a policy decision, not a technical one.] -->

This reframe — from surveillance to support — is available in any Google Docs-based course right now, without new tools or new policies. It requires only the decision to use the information that way.

---

## The Redesign in Practice

Start with the audit. Pick five assessments from your current course. For each, ask the three questions. Flag the ones where a NotebookLM output could substitute and the substitution is not the learning goal. That list is your redesign queue. Take the top item on the queue. Pick one framework. Pilot it with one class section before scaling.

Here is what that looks like for a specific case. A high school history teacher uses a 1,500-word take-home essay on the causes of the American Civil War. The audit: the goal is causal reasoning about a complex historical event. AI substitution is possible in three minutes with uploaded primary sources. Substitution is not the goal. The assessment fails.

Three plausible redesigns.

The oral defense version keeps the essay submission and adds a five-minute one-on-one. The instructor asks: what would change your argument? Why did you weight cause X above cause Y? What is the strongest objection to your thesis? Those questions cannot be answered by an AI that didn't write a specific essay about a specific argument. The student who wrote it can answer them. The student who submitted something they didn't write cannot, or answers in ways that reveal the gap immediately.

The AI-critique version requires the student to generate an AI-written essay on the same prompt and submit both, with a third document analyzing where the AI version is weaker and why — specifically, with evidence from the primary sources that the AI essay missed or misread. The three-artifact submission is harder to fake than a single essay, and the critique artifact demonstrates exactly the close-reading skill the original essay was supposed to demonstrate. To close the meta-shortcut — where a student generates both the essay and the critique with AI — add the requirement that the critique cite specific passages from the primary sources that the AI essay missed. A generated critique cannot cite passages the AI version had access to but chose not to use; only a student who read the sources can do that.

The process documentation version replaces the polished essay with an annotated revision history. The student submits two pages of annotated drafts explaining why each revision was made. The grading rubric evaluates the quality of reasoning visible in the process. Polish is no longer the metric.

None of these is perfect. The oral defense doesn't scale to 200 students without modification — small-group defenses, TA-led defenses, or randomized sampling where any student can be called. The process documentation can in principle be simulated, though producing a realistic iterative work pattern is substantially more labor than doing the work.

The honest comparison is not against a perfect redesign. It is against the alternative: a surveillance regime that doesn't work, produces false accusations at disproportionate rates against specific student populations, loses instruction time, and measures compliance rather than learning.

<!-- → [TABLE: Scale-dependent redesign recommendations — columns: class size, time available per student, primary learning goal, recommended framework, modification needed at scale. Caption: The audit question is the same at any scale. The framework and its modifications depend on the constraints.] -->

---

## What I Don't Fully Understand

There is a student the chapter has not fully accounted for: the one who used AI honestly and well, before any policy existed, and now feels mistrusted by the new regime. This student did not cheat under any definition they were given at the time. The redesign is not directed at them — it is directed at what the assessment was actually measuring — but from where they sit, it looks like a response to something they did.

I do not have a clean resolution for this. The honest response to that student involves acknowledging that the assessment design was flawed before AI arrived, that the AI exposed the flaw rather than creating it, and that the redesign is about measurement validity rather than punishment for past behavior. Whether that lands well depends on factors outside the instructor's control: the student's relationship with the institution, whether they have been falsely accused of anything, how the policy was communicated. This is a real cost of the transition, and the chapter would be dishonest if it didn't name it.

---

**LLM Exercises**

*Use a language model with access to current literature on educational assessment, academic integrity, and AI detection to complete the following.*

**1. Verify the detection evidence.** The chapter cites the Liang et al. 2023 study in *Patterns* and OpenAI's classifier withdrawal as anchors for the claim that detection tools are unreliable. Ask a language model to locate both references and confirm the key findings. Then ask it to identify any high-quality studies published since that report detection accuracy above 95% with documented false-positive rates below 1%. Report what it finds. If no such studies exist, state that as the finding.

**2. Audit a real assessment.** Take one assessment from your current course and apply the three-question audit. Ask a language model to help you state the learning goal as a student action verb — give it your current assessment description and ask it to rewrite the goal in the form "the student [action verb] [what]." Evaluate whether the rewrite captures what you actually want to measure or whether it reveals a gap between your stated goal and your real one.

**3. Framework selection.** Describe a specific assessment you want to redesign to a language model — the subject, the learning goal, the class size, the time constraints. Ask it to recommend which of the four frameworks fits best and why, and what modifications would be needed at your specific scale. Evaluate the recommendation against the chapter's logic. Where does the model's reasoning diverge from the chapter's, and which argument is stronger?

**4. The honest student problem.** Ask a language model to draft a response to the student described in the final section — a policy statement or direct explanation that is honest about the reasons for the redesign without implying that past AI use was wrong. Evaluate the draft: does it hold the tension between supporting legitimate AI use and requiring demonstrated learning, or does it collapse toward one side? Revise where it collapses.
