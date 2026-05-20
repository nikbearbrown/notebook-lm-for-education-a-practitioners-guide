# Chapter 14 — Honest Capability Assessment: What the Evidence Shows

*How to say what you actually know, and nothing more.*

---

There is a habit of mind that is harder than it sounds, and it is the one this chapter is about. The habit is this: when you know something, say what you know. When you don't know something, say that too. Don't let enthusiasm fill in the gaps. Don't let skepticism close them off. Say exactly what the evidence supports and exactly where it runs out.

This sounds like the obvious thing to do. It is not what most people do when evaluating a new tool. What most people do is start with a conclusion — the tool works, or the tool doesn't — and then recruit evidence to support it. The enthusiasm version: find the positive case studies, cite the engagement numbers, describe the transformed classroom. The skepticism version: find the thin evidence base, cite the methodological limitations, describe the surveillance risks. Both versions are built from the same evidence. The difference is what each leaves out.

The chapter is about a third version. Not enthusiasm, not skepticism — assessment. The discipline of stating claims at exactly the level of specificity the evidence supports, no more and no less.

This is the book's terminal chapter for a reason. Everything before it was operational — how to configure the tool, how to design assignments, how to redesign assessments, how to choose among tools. This chapter asks a different question: given everything you have learned and done, what can you honestly say about whether it works?

---

## The strongest available evidence

In 2025, researcher Ammar Mohamed published a mixed-methods study at Gulf University in Bahrain. Five undergraduate communication and media courses. 102 students. Reported findings: improvements in engagement, comprehension, and analytical rigor in written submissions when students used NotebookLM in the course design.

This is the strongest single piece of evidence currently available for NotebookLM's educational impact. The chapter opens with it because what follows is a precise account of what that evidence does and does not establish — and working through that account is the entire skill.

What the Mohamed study establishes: in this specific context, with this specific instructor and these specific students, NotebookLM use was associated with reported gains. The pattern is real for this case.

What it does not establish: generalizability to other disciplines, institutions, or student populations. Causal attribution to NotebookLM specifically, as distinct from the assignment-design changes that accompanied it. Long-term retention or transfer outcomes. Comparison against a well-designed control condition using different tools or no AI.

One study. One institution. 102 students. No comparison group. The reported gains may be genuine. They may reflect the Hawthorne effect — the students performed better because they were being studied, not because of the tool. They may reflect the novelty effect — engagement was higher because the tool was new. The study cannot distinguish among these. It is not designed to.

This is the strongest evidence. A tool whose strongest evidence is one 102-student mixed-methods study with no comparison group has a thin evidence base. That is not a critique of the tool. It is an honest description of where the field stands in mid-2026. The critique would be claiming otherwise.

---

## The four-bucket framework

Every claim about NotebookLM's educational impact can be located in one of four evidence buckets. Locating the claim before repeating it is the discipline.

**Institutional exemplars.** Specific deployments at specific institutions — the Monash self-testing configuration, the UW-Milwaukee Math 94 audio case, the UIC research workflow, the NYU formative feedback loop. These show that educators have found configurations that work in their contexts. They establish workflow and engagement patterns. They do not establish causal effects on learning outcomes across other contexts. The Monash model shows that retrieval-practice-configured Learning Guide produces high engagement at Monash. It does not show that it will produce the same engagement at your institution, with your students, for your subject.

**Conference and review papers.** Argumentative pieces framing NotebookLM as supporting cognitive engagement, self-directed learning, accessibility, or specific pedagogical frameworks. The 2025 AACE/eLearn paper is a representative example. These are critical overviews — they synthesize what's known, identify research directions, and make theoretical arguments for why the tool should work. They are not efficacy trials. "NotebookLM is consistent with self-directed learning principles" is a theoretical argument. "NotebookLM improves self-directed learning outcomes" is an empirical claim. The conference papers support the first; the evidence does not yet support the second.

**Emerging case studies.** Mixed-methods studies at single institutions: Mohamed 2025. Suggestive. The pattern may generalize. It hasn't been tested for generalization. The disciplined version of using this evidence: "one mixed-methods study found X; the finding is plausible and worth replication; it should not be cited as established."

**Learning-science plausibility.** Mappings from NotebookLM features to documented cognitive-science findings. Flashcards map to retrieval practice (Karpicke and Roediger 2008). Spaced quiz generation maps to the spacing effect. Learning Guide's diagnostic questioning maps to the testing effect and formative assessment literature. These are theoretical predictions of what *should* work based on mechanisms that have been studied in other contexts. They are not demonstrations that the mechanism operates as predicted when mediated by this specific tool. The plausibility is real. The empirical demonstration is still pending.

The framework's use: before citing a claim about NotebookLM, place it in its bucket and ask whether you are citing it as if it belonged in a higher-confidence bucket. Most enthusiasm-mode claims do exactly this — they cite an institutional exemplar as if it were a controlled study, or cite learning-science plausibility as if it were demonstrated outcome data.

| Bucket | What it shows | What it does *not* show | Example from this chapter |
|---|---|---|---|
| Institutional exemplars | Workflow and engagement patterns at specific institutions | Causal effects on learning; generalizability beyond the institution | Monash self-testing; UW-Milwaukee Math 94 audio; NYU formative feedback loop |
| Conference / review papers | Theoretical arguments for why the tool *should* work | Empirical efficacy under controlled conditions | 2025 AACE eLearn critical overview paper |
| Emerging case studies | A suggestive pattern at one institution under mixed-methods study | Generalizable findings; causal attribution; comparison against control | Mohamed (2025) — 102 students, five courses at Gulf University |
| Learning-science plausibility | Predictions from cognitive science that the tool's features instantiate | Demonstrated learning outcomes specifically via this tool | Retrieval-practice (Karpicke & Roediger 2008) mapping to flashcards/Learning Guide; Educational Psychology Review 2025 finding on AI-generated quiz/flashcard parity |

*Place the claim in its bucket before citing it. Most overstated claims are bucket-confusion errors.*
---

## The methodologically strongest finding

There is one finding that clears a higher evidentiary bar than the Mohamed study, and it is worth treating separately because it changes what can be said carefully.

Educational Psychology Review published a finding in 2025 reporting that AI-generated quiz questions and flashcards can match teacher-created materials for learning outcomes when used for self-assessment and repeated practice. This is closer to a controlled efficacy finding for AI-generated learning materials, and it has the specific property that makes it most useful: it names the mechanism. The AI-generated materials work when the learning mechanism is retrieval practice — when the student attempts to recall, checks their answer, and repeats. They do not appear to be categorically worse than teacher-created materials for this specific use.

What this establishes: the retrieval-practice mechanism operates when the material is AI-generated rather than human-generated. The learning event that matters is the retrieval attempt, and AI-generated prompts can trigger it as effectively as human-generated ones. This is the evidentiary basis for the Monash configuration described in Chapter 10 — and it is a meaningful finding.

What it does not establish: that AI-generated materials are better than teacher-created ones. That AI-generated open-ended tutoring (explanation mode, not retrieval mode) matches teacher-led tutoring. That the finding extends beyond self-assessment use to other learning contexts. The finding is specific to structured self-assessment with repeated practice. Using it to support claims about AI tutoring in general is a bucket-confusion error of the kind the framework is designed to catch.

<!-- → [CHART: Evidence confidence spectrum — horizontal axis from "lowest confidence" to "highest confidence," four points plotted: Learning-science plausibility / Conference papers / Emerging case studies (Mohamed 2025) / EPR 2025 controlled finding. Each point annotated with what kind of claim it supports. Caption: The EPR 2025 finding sits meaningfully higher than the Mohamed study, but still below multi-site controlled trials. Readers should see the gap between "what we have" and "what we'd need."] -->

---

## Three overstated claims

The chapter names three claims that are currently circulating about NotebookLM and corrects each to the level of specificity the evidence supports. These are not strawmen — they are claims the author has encountered in faculty discussions, marketing materials, and institutional presentations.

**"NotebookLM improves learning outcomes."**

The evidence shows engagement gains, workflow efficiency, and reported satisfaction. It does not yet show durable learning-outcome improvement in controlled conditions. The Mohamed study shows improvement in written submissions; it cannot attribute that improvement to NotebookLM rather than to the assignment redesign that accompanied it, the Hawthorne effect, or the instructor's increased attention to the subject during the study period.

The careful version: NotebookLM-supported assignments, when designed for active engagement using the configurations described in this book, produce workflow and engagement patterns that cognitive science predicts should support durable learning. Direct causal evidence of learning-outcome improvement is currently limited to one small mixed-methods study without a control condition.

**"Source-grounding eliminates hallucination."**

The evidence shows source-grounding reduces hallucination substantially — from roughly 40% in open-loop chatbots to roughly 13% in the comparative study cited in Chapter 1. It does not eliminate it. The residual 13% is misinterpretation, not fabrication — the model misreads the source, overgeneralizes a finding, or drops a qualification — and misinterpretation requires a different verification discipline than fabrication does.

The careful version: source-grounding meaningfully reduces fabrication by making claims traceable to a source. It does not eliminate misinterpretation, oversimplification, or weak quiz-question generation. The citation is an audit trail, not a guarantee. The verification step — clicking the citation, reading the passage, checking the framing — is still required.

**"NotebookLM is safer for students than other AI tools."**

On certain dimensions, it is more defensible. The citation architecture makes fabrication auditable. Institutional Workspace for Education accounts have FERPA/COPPA compliance and training-data exclusions that personal accounts do not. These are real advantages.

On other dimensions, the safety question is the same as for any AI tool. The substitution problem — students using AI output instead of engaging with the material — is not solved by source-grounding. The equity problem — unequal access to the tool, unequal digital literacy, institutional deployment that benefits some students more than others — is not solved by source-grounding. The integrity climate problem — what happens to academic honesty norms when AI-generated work is routine — is not solved by source-grounding.

The careful version: NotebookLM is more defensible than open-loop chatbots on fabrication and on data governance when used through institutional accounts. On substitution, equity, and integrity climate, it raises the same questions as any AI tool, and those questions are answered by assignment design and institutional policy, not by the tool's architecture.

| Overstated claim | What the evidence actually shows | What evidence would be needed to support the stronger claim | Careful-version replacement |
|---|---|---|---|
| "NotebookLM improves learning outcomes" | Engagement and reported satisfaction at scale; one mixed-methods study (Mohamed 2025) at one institution shows reported comprehension and analytical-rigor gains; Educational Psychology Review 2025 supports AI-quiz parity for self-testing | Controlled multi-institution efficacy trial with comparison condition and durable-learning outcome measures | "NotebookLM-supported assignments, when designed for active engagement, can support workflow and engagement patterns consistent with durable learning. Direct causal evidence of learning-outcome improvement is currently limited; the Google research-partnership program (Purdue, UAB, UC Riverside) is expected to produce stronger evidence later in 2026." |
| "Source-grounding eliminates hallucination" | Hallucination rate reduced ~40% → ~13% in one comparative study against general-purpose chatbots | A study showing the residual 13% can be driven to zero via the source-grounding mechanism itself (not via prompt engineering or instructor review) | "Source-grounding meaningfully reduces fabrication. Misinterpretation, oversimplification, and bad quiz-question generation remain — at lower rates than open-loop chatbots but at rates that require active verification by the educator." |
| "NotebookLM is safer for students than other AI tools" | More defensible on citation auditing and on Workspace-for-Education governance; not measurably safer on student-substitution risk or assignment-design integrity questions | Comparison studies of integrity outcomes across tools under controlled conditions | "NotebookLM is safer than open-loop chatbots on fabrication and on data governance when used through institutional accounts. It is no safer than any other AI tool on student substitution, equity, or institutional integrity climate — those depend on assignment design and policy." |

*The careful version is not weaker; it is defensible. Overstated claims collapse on contact with skeptical administrators or methodologically literate colleagues.*
---

## The aging-risk problem

This chapter has an unusual property: it will be outdated faster than the others. The feature lists in Chapter 3 will change. The workflow descriptions in Chapters 4 and 10 will be affected by interface updates. But those changes are incremental — a new output type, a revised tier limit. This chapter will need substantive revision when the evidence base changes, and the evidence base is actively changing.

The Google research partnership announced in May 2026 — involving Purdue, UAB, and UC Riverside — is designed to produce the kind of outcome data that the Mohamed study lacks: controlled conditions, multiple institutions, rigorous causal attribution. If that research produces strong positive findings, the "thin evidence" framing of this chapter will need to be revised. If it produces null or mixed findings, the careful claims the chapter defends will be strengthened. Either way, the chapter's current framing is a snapshot of the evidence as it stood in mid-2026, and it should be clearly dated as such.

The principle for writing a capability assessment that ages well: separate what the chapter calls the stable core from the current state. The stable core is the set of claims that hold regardless of what specific feature is in which tier, or which study was just published. Source-grounding reduces fabrication by making claims traceable to a source — that is a structural property of the RAG architecture, and it is stable. The specific fabrication-reduction number (40% → 13%) is a current-state detail — it comes from one comparative study, and future studies may revise it.

An honest capability assessment built on stable-core claims can be re-issued when the evidence changes by updating the current-state details while leaving the core argument intact. An assessment built on current-state details cannot — it has to be rewritten from scratch when the features change or the evidence moves.

<!-- → [INFOGRAPHIC: Stable core vs. current state — two-column layout. Left: "Stable Core" with checkmark: structural claims that hold across tool versions and studies (e.g., "source-grounding makes fabrication traceable"). Right: "Current State" with refresh icon: specific numbers and named studies that require re-verification at each reprint (e.g., "40% → 13% fabrication reduction"). Caption: Build your assessment on the left column. Annotate the right column with a date. When the evidence moves, update the right column without rewriting the left.] -->

---

## The one-page assessment

The book's terminal deliverable is not a worked example — it is a template that forces the discipline the chapter has been building toward. Five sections. Total length: one page. Every sentence earns its place by being specific, evidence-grounded, and honest about what it doesn't know.

**Context.** Two or three sentences: who is being served, what subject, what educational level. The specificity here is what makes the rest defensible — a capability assessment for "education" is not defensible because the claims that are true for one context are not true for all contexts.

**What NotebookLM does well here.** One paragraph. Specific to the subject and mode. Each claim tied to either a learning-science finding (bucket 4) or a documented institutional exemplar that is genuinely analogous to the context (bucket 1). Use careful-version claims. The section's purpose is not to make the strongest possible case for the tool — it is to identify the uses where the evidence, however thin, points in the right direction.

**What it does not yet do well, or is not yet shown to do well.** One paragraph. Named gaps. If the deployment context includes open-ended reasoning tasks, those are outside the bounded architecture's strength. If the students are from populations underrepresented in the existing exemplar literature (the exemplars are mostly research universities and suburban high schools), say so. If the subject has characteristics that make the source-grounding approach less useful (subjects where the authoritative source is the student's own original analysis rather than an assigned corpus), say that.

**What the evidence shows.** One paragraph. Locate the central claims in their evidence buckets. Name the buckets. State what evidence would be needed to support the stronger claims — which is the single most important sentence in the assessment, because it converts "we don't know" from a gap into a research question.

**What is still uncertain.** Two or three sentences. Named gaps. Named research that would resolve them. The Google partnership outputs are a near-term named answer for the learning-outcomes question. For context-specific questions — does this configuration work for this population — the named answer is: pilot it, measure it, report it.

This document replaces the vague *"NotebookLM works for our students"* claim with a specific, evidence-grounded, revisable position. The position is what survives contact with skeptical administrators. It is what survives your own re-reading two years from now when the deployment has produced outcomes you didn't predict.

<!-- → [INFOGRAPHIC: One-page honest capability assessment template — five labeled sections with sentence-count guidance: Context (2-3 sentences), What works here (1 paragraph, cite evidence bucket), What doesn't / isn't shown (1 paragraph, named gaps), What the evidence shows (1 paragraph, name the buckets), What is still uncertain (2-3 sentences, name the research). Annotation pointing to each section: what kind of claim goes here, what kind of claim does NOT go here. Caption: The template is a discipline, not a form. Every sentence should be specific enough to be falsified.] -->

---

## What this chapter established

The evidence base for NotebookLM's educational impact is thin. The strongest single study is one 102-student mixed-methods case without a control condition. The strongest controlled finding establishes parity between AI-generated and teacher-created materials for self-assessment use — not superiority, and not extension to other use cases. Three claims currently circulating about the tool are overstated, each in a specific and correctable way. The four-bucket framework makes the correction discipline explicit and repeatable.

This is not a negative verdict on the tool. The thin evidence is not evidence of ineffectiveness — it is evidence that the controlled studies haven't been done yet. The path from here is not to wait for the evidence before deploying, but to deploy in ways that are honest about what is and isn't established, design assessments that serve the uses the evidence does support, and contribute to the evidence base by observing and reporting what happens in your own context.

The Purdue / UAB / UC Riverside partnership is the named next step for the field. This chapter's framing is explicitly held as revisable when that work is published.

---

## Key terms

- **Four-bucket framework** — Institutional exemplars, conference and review papers, emerging case studies, learning-science plausibility. The structure for locating evidence claims before repeating them.
- **Bucket-confusion error** — Citing evidence from a lower-confidence bucket as if it belonged in a higher one. The most common form of overclaiming.
- **Thin evidence base** — Not absence of evidence, but evidence that is limited in methodological rigor, scope, or generalizability. The current state for NotebookLM learning-outcome claims.
- **Stable core vs. current state** — The principle for writing capability assessments that age well. Stable-core claims hold across tool versions; current-state claims need re-verification at each reprint.
- **Honest framing** — Stating claims at exactly the level of specificity the evidence supports. The chapter's structural alternative to enthusiasm or skepticism.

---

## Aging note

**This chapter ages fastest of the substantive content.** The Mohamed 2025 study and the Educational Psychology Review 2025 finding are current best evidence; by late 2026 the Google research-partnership outputs should produce something more rigorous. The author commits to revising the "thin evidence" framing when that research is published, in either direction. Re-check the overstated/careful-version claim pairings against new evidence at every reprint. The four-bucket framework and the stable-core/current-state principle are stable; the specific evidence claims are explicitly time-stamped.

---

## Exercises

### Warm-up

**1.** A colleague tells you: "I read that AI tools improve student engagement, so we should adopt NotebookLM." Using the four-bucket framework, identify which bucket this claim is likely drawn from. What additional information would you need to place it more precisely?
*Tests: four-bucket framework, claim location. Difficulty: low.*

**2.** Reread the three "overstated claims" in this chapter. For one of them, write the careful-version replacement in your own words — without looking back at the chapter's version. Then compare. What did you capture? What did you miss?
*Tests: careful-version construction, honest framing. Difficulty: low.*

**3.** The Mohamed 2025 study is described as the "strongest single piece of evidence" for NotebookLM's educational impact. List three specific things the study cannot establish and explain why each is beyond what its design can show.
*Tests: evidence interpretation, limits of single-institution mixed-methods studies. Difficulty: low.*

### Application

**4.** You are writing a capability assessment for a community college developmental math course where students will use NotebookLM's quiz generation for self-testing. The institutional exemplars in this chapter come from research universities and suburban high schools. Write the "What it does not yet do well, or is not yet shown to do well" section of the one-page assessment template for this specific context. One paragraph. Cite the evidence gap precisely.
*Tests: one-page assessment template, context-specific gap identification, bucket-confusion avoidance. Difficulty: medium.*

**5.** A department chair asks you to produce a two-sentence summary of what the research shows about NotebookLM for an accreditation document. Draft two versions: one that a careful reader would accept as honest, and one that overstates. Then annotate each — what makes the first defensible and the second not?
*Tests: careful-version construction, honest framing under institutional pressure. Difficulty: medium.*

**6.** The EPR 2025 finding establishes that AI-generated flashcards and quiz questions can match teacher-created materials for learning outcomes in self-assessment contexts. A colleague cites this finding to support adopting NotebookLM's open-ended tutoring features. Identify the bucket-confusion error and write the correction.
*Tests: bucket-confusion identification, mechanism specificity. Difficulty: medium.*

**7.** Apply the stable-core / current-state distinction to the following three claims. For each, say which category it belongs in and why: (a) source-grounding makes fabrication traceable to a source; (b) source-grounding reduces fabrication from roughly 40% to roughly 13%; (c) retrieval practice improves long-term retention.
*Tests: stable core vs. current state, aging-risk principle. Difficulty: medium.*

### Synthesis

**8.** Using the one-page assessment template, write a complete honest capability assessment for a specific context of your choosing: name the course, the student population, and the intended NotebookLM use. Every claim must be located in an evidence bucket. The "what the evidence shows" section must include the sentence naming what evidence would be needed to support the stronger claim.
*Tests: full template application, bucket framework, honest framing, stable-core claims. Difficulty: high.*

**9.** This chapter argues that an honest capability assessment built on stable-core claims "can be re-issued when the evidence changes by updating the current-state details while leaving the core argument intact." Draft a revised version of the chapter's central assessment paragraph — the one beginning "The evidence base for NotebookLM's educational impact is thin" — as it might read if the Google research partnership produced strong positive findings. What changes? What stays the same? What does that tell you about which claims were stable-core and which were current-state?
*Tests: stable core vs. current state, honest framing under new evidence, aging-risk principle. Difficulty: high.*

### Challenge

**10.** The chapter's four-bucket framework is designed for evaluating evidence about a specific tool. Consider whether the same framework applies to evaluating evidence about a pedagogical practice — say, active learning or flipped classrooms. Where does the analogy hold? Where does it break down? What would need to change in the framework to handle pedagogical-practice evidence, and what does that tell you about what the framework is actually doing?
*Tests: framework extension, limits of analogy, meta-level thinking about evidence standards. Difficulty: open-ended.*

---

*This is the end of the book's main content. Appendix A — The Fundamental Themes is the theoretical upstream for readers who want the broader argument the chapters were built inside.*
