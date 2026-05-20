# Chapter 8 — Academic Integrity: The Honest Conversation

*An AI use policy that says "don't" without saying "because" will not survive the first conversation with a student who asks why.*

---

Here is a thing Florida State University noticed.

When faculty looked at students who were using AI in ways that undermined their own learning, four behavioral markers showed up reliably. Not "submitted text that sounded like a chatbot." Something more specific and more useful than that.

First: the student cannot explain the intellectual steps to a conclusion without referencing the AI. Second: the student uses the tool to generate complete responses rather than to understand the material. Third: the student relies entirely on summaries and avoids engaging with original texts. Fourth: the student experiences heightened anxiety when forced to complete work without digital assistance.

These are observable. A teacher can see them without reading anyone's mind, without running detection software, without accusing anyone of anything. And they are framed for conversation, not punishment. The right response to any of these markers is a one-on-one about the student's learning — not an honor-code filing.

What the FSU markers point toward is a policy design problem. Every one of these behaviors is *downstream* of an assignment structure that permitted it. The student who cannot explain steps to a conclusion was never required to explain them. The student who avoided original texts was never required to demonstrate engagement with the original. The anxiety student was trained, by assignment design, to rely on the tool in contexts that later disappeared.

This chapter works backward from those markers. What design makes each one more or less likely? What policy supports the conversation instead of the surveillance? And — the deeper question — why do students use AI in academically dishonest ways at all, when most of them know it's against policy?

---

## Why Policy Doesn't Work the Way We Think It Does

<!-- → [CHART: Bar chart or scatterplot visualization of MDPI 2025 finding — ethical beliefs vs. policy awareness as predictors of AI use behavior — student sample n=401] -->

In 2025, a study published in MDPI tested two variables against AI use behavior in writing assessments across 401 students at major U.S. universities. The variables were: students' *awareness* of their institution's AI policy, and students' *ethical beliefs* about whether AI use in academic work was wrong.

Policy awareness had no significant predictive effect. Ethical beliefs predicted behavior strongly.

Read that carefully. Knowing the rule didn't change what students did. Believing the behavior was wrong did.

This is uncomfortable for anyone who has spent time writing AI policies, distributing them through syllabi, posting them to course management systems, asking students to sign acknowledgment forms. All of that acts on awareness. None of it acts on belief. And belief is what controls behavior.

The implication follows directly. A policy that only states what is prohibited — without explaining *why*, without giving students the reasoning behind the prohibition, without asking students to think about what authorship and learning actually mean — is an inert policy. It may satisfy an institutional compliance requirement. It will not change what students do when the assignment text makes the shortcut available.

The policy that has a chance of working is one that treats the student as someone capable of moral reasoning and gives them something to reason about. Not "AI use is prohibited on this assignment" alone. "AI use is prohibited on this assignment *because* this assignment is designed to build the specific skill of synthesizing conflicting sources under time pressure, which you cannot build if the synthesis is done for you — and here is why that skill matters for what comes after this course." That argument can be believed or rejected. A bare prohibition cannot.

---

## What Academic Integrity Actually Protects

<!-- → [INFOGRAPHIC: Diagram showing the three parties in an academic integrity framework — student, institution, future context — and what each loses when integrity fails] -->

Let me be precise about what we are protecting, because the precision changes the policy.

Academic integrity protects three things, and they are not the same thing.

It protects the *student's own learning*. A student who uses AI to complete work they were meant to do is acquiring a credential without acquiring the underlying capability. In the short term this is a successful optimization. In the medium term — in a job, a graduate program, a professional context — the missing capability surfaces. The credential promised something that wasn't there. This is a harm to the student, even if the student doesn't experience it as one until later.

It protects *institutional credibility*. A degree or a grade is a signal to the world about what the student can do. If the signal is systematically decoupled from the capability it claims to represent, the signal degrades for everyone who holds it — including students who earned their credential honestly.

It protects the *intellectual community* of the classroom. When students are all doing the cognitive work — struggling with the same hard texts, making their own arguments, producing their own analyses — the conversation that follows is real. When some students have offloaded that work to a tool, the conversation is unequal in a way that damages it for everyone.

These three concerns don't all point to the same policy. The first suggests that integrity policy should be designed around genuine learning outcomes — and that assignment designs which permit shortcuts are as much an integrity problem as the student who takes them. The second suggests that credentialing contexts require more stringent controls than formative learning contexts. The third suggests that integrity in discussion and participation matters differently than integrity in individual written work.

A policy that treats all of these the same, with one blanket statement about prohibited AI use, is a policy that hasn't thought clearly about what it is trying to protect.

---

## NotebookLM Specifically

| Use case | Context where integrity is maintained | Context where integrity is at risk | Distinguishing factor |
|---|---|---|---|
| Generating a study guide | Student reads it as a scaffold for understanding the source before discussion | Student submits it as their own analysis | Whether the artifact is a study aid or a deliverable |
| Generating flashcards | Student uses them for self-testing; takes them multiple times | Student submits AI-generated quiz answers as their own work | Whether the cognitive work happens in the student or in the deliverable |
| Synthesis query across sources | Student verifies cells against original sources and uses verified findings in their own analysis | Student copies the synthesis into a paper without verification or transformation | Whether the student's contribution is the synthesis or only its retrieval |
| Drafting an essay outline | Student uses the outline as a starting point and revises substantially | Student fills in an AI-generated outline and submits | The depth of the student's revision and the substance of the student's contribution to the argument |
| Asking the AI to explain a concept | Student integrates the explanation with their own thinking | Student treats the explanation as their answer to the question | Whether the explanation is input to learning or output of it |
Most AI integrity discussions happen at a level of generality that makes them difficult to apply. "AI use" covers a spectrum from a student asking a general-purpose chatbot to write their essay, to a student using a source-grounded tool to navigate a difficult primary document. Those are not the same action, they don't produce the same learning outcomes, and they don't raise the same integrity concerns.

NotebookLM's source-grounding constraint is the fact that changes the integrity calculus. The tool generates outputs only from sources the user uploads. It cannot write a student's essay from thin air; it can only produce outputs grounded in what the student has given it. This means the tool's integrity risk is concentrated in specific use cases, not distributed uniformly.

The high-risk use cases are these. A student uploads a text they are supposed to read and uses the Study Guide to avoid reading it — submitting a summary that is the model's summary, not their own engagement with the source. A student uploads their own draft essay and uses NotebookLM to rewrite or extend it, submitting output they did not write as their own work. A student uses the Flashcard or Quiz function to generate a set of materials in a context where producing those materials was the assignment.

The low-risk use cases are structurally different. A student uploads a difficult primary source they are struggling with and uses the notebook's chat function to ask specific questions about passages they have already tried to read. A student uses an Audio Overview as a preview before reading, not as a replacement for reading. A student uses the notebook's citation function to check whether their interpretation of a source is supported — and reads the passage.

The distinguishing factor is not the tool or the feature. It is whether the student's intellectual contribution — their reading, their reasoning, their synthesis — is the primary labor, with the tool playing a supporting role; or whether the tool's output is the primary artifact, with the student playing a light-editing role. The first is fine. The second is the problem.

A policy that applies this distinction — rather than either banning all NotebookLM use or permitting it entirely — is a policy grounded in what the tool actually does.

---

## Writing the Policy

| Section | Example language |
|---|---|
| Statement of purpose | *"This course teaches you to construct arguments, evaluate evidence, and revise your own thinking. NotebookLM can support those activities. It can also substitute for them. This policy specifies which is which."* |
| Permitted uses | *"You may use NotebookLM to: prepare study artifacts from assigned readings; verify citations; generate diagnostic questions for self-testing; surface contradictions or tensions across multiple sources."* |
| Restricted uses | *"You may not: submit NotebookLM's analysis as your own writing; have NotebookLM generate your final essay text; use NotebookLM during in-class proctored work without explicit permission."* |
| Disclosure requirement | *"Every submitted assessment must include a one-paragraph AI use disclosure: what tools you used, what outputs you generated, what you accepted, and what you revised. Disclosure itself is not an integrity violation; failing to disclose is."* |
| Conversation clause | *"If your use of NotebookLM produces a pattern I find concerning (the four FSU red flags), I will reach out for a conversation. The conversation's purpose is to support your learning, not to discipline you. If, after conversation, the pattern continues, the course's integrity procedures apply."* |
A NotebookLM use policy has five components. Not because five is the right number for any mystical reason, but because each component addresses a different failure mode.

**Statement of purpose.** Why does academic integrity matter in this context? Not the legal boilerplate — the actual argument about learning and credentialing. This is the component that acts on belief rather than awareness. If this component is missing or generic, the policy is doing nothing the MDPI finding would predict to be effective.

**Permitted uses.** Specific. What can a student do with NotebookLM in this course, on what kinds of tasks? "Use as a reading aid to help you understand difficult passages" is specific. "Use for study" is not. The specificity matters because a student trying to comply in good faith needs to know what compliance looks like. A student trying to find the loophole will find it whether the policy is specific or general — but the specific policy makes good-faith compliance possible.

**Restricted uses.** Equally specific. What may not be submitted as the student's own work that was generated by the tool? "Submitting a NotebookLM Study Guide as your own summary of the reading" is specific. "Do not have AI do your work" is not. Again, specificity serves the student trying to comply.

**Disclosure requirement.** In contexts where AI use is permitted in some forms, require students to disclose how they used it. Not as a policing mechanism — as a norm. "I used NotebookLM to generate flashcards on chapter 4, then took the flashcards and added three of my own" is a disclosure that demonstrates exactly the kind of engagement the tool should be supporting. The act of writing the disclosure requires the student to be aware of their own process.

**Conversation clause.** "If you're unsure whether a particular use is permitted, ask me before you do it — not after." This is the FSU behavioral-marker framing applied at the policy level. The markers are for conversation, not punishment. The policy should say so explicitly.

These five components together form a policy that can survive a student asking "why." The purpose explains the why. The permitted/restricted structure explains the what. The disclosure norm builds the habit of reflection. The conversation clause keeps the policy human.

---

## The Conversation You Are Actually Designing For

<!-- → [INFOGRAPHIC: Decision tree for handling a suspected integrity violation — branching from "observable behavior" through conversation, assessment, and outcome paths] -->

Most integrity policies are written for the enforcement scenario — what happens after a violation is documented. The better design question is: what conversation do I want to be able to have with a student *before* a violation is documented?

The FSU behavioral markers are a diagnostic for that conversation. A student who cannot explain their reasoning without referencing the AI is not necessarily a student who violated a rule. They may be a student who has learned to rely on a tool as a cognitive prosthetic, which is a learning problem before it is an integrity problem. The right first move is a conversation about the student's learning — what did you understand before you used the tool? What can you explain without it? Where is the gap?

That conversation requires a teacher who has thought clearly about what the assignment was for, what capability it was meant to build, and whether the student has that capability. It does not require AI-detection software. It does not require an accusation. It requires the specific knowledge of what this assignment was supposed to produce in this student.

The policy that enables this conversation is one that has been *explained* to students in advance, so the student knows what the teacher values and why, and the teacher can refer back to that shared understanding rather than introducing a new standard after the fact. "You and I discussed at the start of this course what kind of work demonstrates genuine understanding in this subject. Let's look at this together through that lens." That conversation is possible when the policy was explained. It is not possible when the policy was only distributed.

---

## What the Detection Tools Get Wrong

<!-- → [CHART: Liang et al. 2023 finding — false positive rates for AI detection tools across native vs. non-native English writers — visualize the disparity] -->

AI detection tools deserve a specific note, because their use is spreading and their reliability is poor in ways that matter for equity.

Liang et al., in 2023, documented systematic false positive rates in AI detection tools against writing by non-native English speakers. The tools trained to identify AI-generated text had also learned, in effect, to flag certain features of non-native writing — features that correlate with how non-native writers structure sentences, choose vocabulary, and produce prose under time pressure. A student writing genuinely but writing in English as a second or third language is more likely to be flagged as having used AI than a native speaker writing at the same level of sophistication.

This is not a minor calibration problem. It is a systematic bias that would concentrate false accusations on students who are already navigating additional challenges. A policy that relies on detection tools as enforcement infrastructure is a policy that will produce unjust outcomes at a predictable rate.

The alternative is not to ignore integrity concerns. The alternative is the design-based approach the previous chapters describe — assignments that make the shortcut self-defeating, policies that act on belief rather than surveillance, conversations that diagnose learning rather than punish rule violations. These approaches do not require detection tools and do not produce the equity problem the tools introduce.

---

## What Would Change the Chapter's Position

A replication of the MDPI 2025 finding that did not hold — that found policy awareness did predict behavior in a different student population or institutional context — would complicate the chapter's central design claim. The finding is based on one study of 401 students at major U.S. universities. That is a real finding, but it is not a law. If institutional context, policy framing, or student population characteristics moderate the effect, the policy design implications would need revision.

A reliable, validated AI detection tool with documented false positive rates below a meaningful threshold — below the background rate of academic dishonesty it would be used to address — would change the chapter's position on detection tools specifically. As of writing, no such tool exists for the text modalities commonly used in K–12 and higher education. The situation is technically fluid; the equity concern remains regardless of accuracy improvements.

Three things still genuinely uncertain: whether the ethical-beliefs finding replicates across non-U.S. educational contexts where AI policy norms differ; whether the disclosure requirement norm, if widely adopted, changes student behavior by making AI use visible rather than hidden; and whether the FSU behavioral markers, while clinically useful, can be operationalized in large-enrollment courses where the one-on-one conversation they imply is not feasible at scale.

---

## LLM Exercises

1. Take your current AI use policy — or, if you don't have one, take a generic policy from your institution's current guidance — and paste it into an LLM. Ask the LLM to identify: which components act on student *awareness* of rules, and which components act on student *beliefs* about what learning and authorship mean. Ask it to rewrite the policy with the MDPI finding in mind — emphasizing the reasoning, not just the rules. Compare the rewrite against your original. Note what changed and what was lost.

2. Take the five FSU behavioral markers. Paste them into an LLM along with the description of a specific assignment in your course. Ask the LLM to identify which assignment design features make each marker more or less likely to appear. Ask it to suggest one design change per marker that would reduce the likelihood of the problematic behavior. Evaluate its suggestions against what you know about your students and context.

3. Write a one-paragraph "honest conversation" statement — the part of your policy that explains *why* integrity matters in your specific course, addressed directly to your students. Paste it into an LLM and ask it to evaluate whether a skeptical student would find the reasoning compelling, where the argument is weakest, and what objections a student might raise. Use the LLM's critique to revise the statement. Note: the goal is not a policy that is invulnerable to objection — it is a policy that has already thought about the objections and answered them honestly.

---

## Chapter Summary

You can now write an AI use policy for NotebookLM with five components: purpose, permitted uses, restricted uses, disclosure requirement, and conversation clause. You understand why the policy's purpose statement — the reasoning, not just the rules — is the component that actually acts on behavior, and why the FSU behavioral markers are a diagnostic for learning conversations rather than a trigger for enforcement. You know why detection tools introduce equity risk and why design-based approaches are the more reliable alternative.

The one idea from this chapter that matters most: policy awareness does not predict behavior. Ethical belief does. The policy that has a chance of working is the one that gives students the reasoning to form beliefs about what learning and authorship mean — not just the rules to comply with.

The common mistake: writing the policy after the course design is complete, as a final compliance step. Policy and assignment design are coupled. A policy that permits certain uses while an assignment design makes those uses invisible produces the gap everything falls through. Design first, then write the policy that reflects the design.

The Feynman test: explain to a colleague why a stricter AI policy does not solve the problem this chapter addresses. Walk them through the MDPI finding, the distinction between belief and awareness, and what the conversation clause is actually for. If you can do that — if you can explain why "don't" without "because" fails — you have the chapter.

---

## Where This Leads

You have the policy. Chapter 9 asks what happens when the policy meets an institution that has made different choices — districts that have banned AI tools entirely, institutions that have mandated them, the range of administrative contexts you may not control but have to navigate. The policy you've designed is yours. Chapter 9 is about what you do when the institutional context pushes back.

---

*The MDPI 2025 finding is current as of writing; replication studies are likely through 2026–2027. The Liang et al. 2023 detection-tool bias finding is documented; the technical landscape for detection tools is changing faster than the equity concern. Re-verify specific tool recommendations before each deployment.*
