# Chapter 10 — Higher Education: Course Design and the Self-Testing Model

*The Monash model — configure NotebookLM to quiz the learner, not explain to them — is the highest-leverage use case for undergraduate course integration.*

---

Here is a puzzle worth sitting with.

Two universities deploy NotebookLM in undergraduate courses. Both deployments work. The design principles behind them are almost opposite.

At UW-Milwaukee, a teaching consultant named Ed Price was working with a remedial math course — students who arrived with genuine math anxiety, the kind that shuts down cognition before the problem is half-read. He generated podcast-style Audio Overviews of the mathematical units and embedded them in Canvas as optional resources with closed captions. Students who chose to listen reported feeling more comfortable during in-person problem-solving sessions. Price's conclusion was careful: the tool works as a supplementary companion to dense material, not as a replacement for active study.

At Monash University, the deployment looks nothing like this. Monash configures Learning Guide as a self-testing companion — not a tool that explains things to students, but a tool that asks students diagnostic questions, waits for their answers, and evaluates before offering feedback. The tool is the assignment. Engagement is not optional. The design is retrieval practice from the first moment.

Both of these are right. They are right for different reasons, and mixing the reasons produces failures that are entirely predictable once you see what each design principle actually is.

UW-Milwaukee is running accessibility plus optionality. The resource is there for students who benefit; the rest of the class is not required to use it; the audio does not replace any required work. Monash is running retrieval-practice integration. The tool is the required cognitive event — not a supplement to learning but the mechanism that produces it. A faculty member who doesn't know which principle they are deploying will end up with something that is neither. They'll make the audio required and high-stakes, which is the wrong design for an accessibility resource. Or they'll make the self-testing optional and ungraded, which is the wrong design for a retrieval-practice tool.

The chapter's job is to make the distinction clear enough that you cannot mix them by accident.

---

## Why Retrieval Practice Is the Right Frame for Learning Guide

The pedagogical foundation for the Monash model is decades old and unusually solid. Karpicke and Roediger, writing in *Science* in 2008, showed that retrieval practice — being asked to recall information from memory, rather than re-reading or re-listening — produces dramatically more durable learning. The finding has replicated. It holds across subjects, ages, and content types with enough consistency to call it one of the most reliable results in educational psychology.

The mechanism, stated plainly: when you encounter new information and then retrieve it — try to recall it, attempt to produce it, answer a question about it — you strengthen the memory trace in a way that passive re-exposure does not. The effort of retrieval is not a side effect. It is the event that produces learning. A tool that bypasses that effort, by explaining rather than testing, removes the cognitive event you actually needed.

This is why the default tutoring pattern — student asks a question, tool provides an explanation — is the least efficient use of a learning tool that is capable of doing something more demanding. The explanation feels useful. It is comfortable. The student finishes feeling like they understood. But the understanding is fragile in a way that retrieved understanding is not, because the retrieval event never happened.

The Monash configuration inverts this. Instead of the student asking "explain X," the student invokes Learning Guide with "test me on chapter 4." The tool generates diagnostic questions one at a time. The student attempts each one. The tool evaluates and provides feedback only after the student has tried. The discomfort is the point. The effort of trying and being wrong before seeing the correct framing is exactly what produces learning that sticks.

<!-- → [FIGURE: Learning curve comparison — two lines over time: passive re-reading (initial retention high, rapid decay) vs. retrieval practice (lower initial confidence, slower decay, higher long-term retention). Caption: The effort that makes retrieval practice feel harder is the same effort that makes it work. Comfortable re-reading produces less retention, not more.] -->

There is a timing detail here that matters and that most deployments miss. Learning Guide is most powerful during *initial learning* — as the encoding event, the first time the student works through the material. Most faculty deploy self-testing tools as review, after the fact, as a check that learning happened. That is less than half the leverage. Used before the student has consolidated the material, the tool is forcing the retrieval attempt that produces the encoding. Used after, it is measuring what the encoding produced. Both have value; the first has substantially more.

---

## The Configuration That Produces This

The Monash model requires explicit configuration, and that configuration has to be taught to students. Students who are handed a notebook without instructions will do what comes naturally: they will ask the tool to explain things. The tool will oblige. The retrieval event will not occur. The deployment will look fine and produce less than it could.

The configuration is not complicated. It is entirely a matter of what the student types.

Default behavior: "Explain regression to the mean." Tool response: two paragraphs of explanation, source-grounded. Student reads it, feels like they understand, retains less than they would have with a retrieval attempt.

Monash configuration: "Test me on chapter 4. Ask me one diagnostic question at a time. Do not give me the answer until I have attempted. If I am wrong, give me a more scaffolded question rather than explaining." Tool response: a diagnostic question. Student attempts. Tool evaluates. If wrong, another question. The explanation arrives only after effort.

The difference is entirely in how the student invokes the tool. This means the teacher's job at deployment is to write that configuration prompt into the student-facing instructions — not as an optional suggestion, but as the assignment itself. A concrete example: *Before our Friday session, open the class notebook and invoke Learning Guide with this exact prompt: "Test me on chapter 4 applications." Work through at least three diagnostic questions. Bring to class: one question you struggled with, one question that made the concept click.*

Two things make this work that would otherwise break it.

First, the student-facing instructions must specify the invocation prompt, not just the goal. "Use Learning Guide to study chapter 4" produces explanation-seeking. "Invoke Learning Guide with this exact prompt" produces self-testing. The specificity is not pedantic; it is the mechanism.

Second, the teacher should generate the question set themselves before deploying to students. Learning Guide's diagnostic questions are good enough to be useful and inconsistent enough to require review. Some questions are sharp, well-targeted, testing exactly the concept you want tested. Some are formulaic, pattern-matching on textbook phrasing without testing actual understanding. Some are ambiguous. Five minutes of question review per assignment — generating the set yourself, identifying the weak ones, cutting or flagging them — is cheap relative to the cost of deploying weak questions to two hundred students who will form wrong impressions of what they are supposed to understand.

<!-- → [TABLE: Four configuration approaches — columns: approach, default student behavior, what changes with explicit prompt, pedagogical effect. Rows: no configuration (default invocation), quiz-me-on-X prompt, test-then-explain prompt, discipline-specific configuration via teacher Note. Caption: The configuration determines whether the tool produces tutoring-by-explanation or retrieval practice. The difference is entirely in what the student types.] -->

---

## The NYU Feedback Loop

At NYU's October 2025 Teaching and Learning with Generative AI symposium, an instructor demonstrated a use case that looks nothing like either the UW-Milwaukee or Monash models, but is worth understanding because it demonstrates the bounded-tool framework applied in a direction most faculty don't consider.

The context: a large introductory programming course. Mid-semester student feedback, grading patterns from assignments, polling responses from in-class sessions. The instructor's question: where are students actually stuck?

The workflow: collect the feedback data — surveys, confusion patterns from grading, polling responses. Upload that data to NotebookLM as a source. Query: "Based on this feedback, what three concepts are students most struggling with? Generate a formative assessment activity targeting each." Deploy the activities through the LMS.

What is happening here is different from content generation for students. NotebookLM is functioning as a teaching-analytics instrument — the input is student data, the output is insight and response that the teacher then acts on. The tool is not in the student-facing workflow at all. It is in the faculty workflow, processing information about students to improve the course while it is running.

This matters because it reveals a deployment pattern that works even for faculty who are uncertain about putting AI tools directly in students' hands. The question "is NotebookLM appropriate for student use in my course?" is separate from "can I use NotebookLM to improve how I teach this course?" The NYU case answers the second question affirmatively without touching the first.

<!-- → [TABLE: Three deployment models compared — columns: UW-Milwaukee accessibility, Monash self-testing, NYU feedback loop. Rows: who interacts with the tool, what the input is, what the output is, who acts on the output, design principle. Caption: The three models are not points on a spectrum — they are different tools for different problems sharing the same interface.] -->

The limitation worth naming: the NYU feedback-loop pattern benefits from data volume. A large lecture generates enough feedback signal that the analysis produces genuinely useful patterns. In a seminar of twelve students, you may already know where everyone is stuck, and the analysis step adds overhead without insight. The tool generalizes to the problem of knowing where a crowd is confused. It does not generalize to the problem of knowing where a specific student is confused, which remains a human judgment.

---

## What Changed in April 2026

A higher-education-specific operational fact: as of April 2026, students aged 18 and older can create personal class notebooks grounded in educator-provided Classroom materials. This is the operational unlock the Monash model was waiting for at scale.

Before this expansion, the fully individualized self-testing deployment — each student with their own notebook, their own diagnostic history, their own Learning Guide session — required either institutional provisioning or workarounds. After it, a faculty member can design assignments that depend on individual student notebooks, and students with institutional Google Workspace accounts can instantiate those notebooks themselves.

The practical constraint that remains: institutional Workspace settings vary. Some institutions enabled the feature; others have not configured it. Confirm before designing assignments that depend on individual student notebook creation.

The pedagogical implication of the expansion is worth stating directly. The Monash model at scale requires students to build their own notebooks from course materials — not to consume a teacher-built notebook, but to instantiate their own retrieval-practice environment from the sources the teacher provides. That design was possible before April 2026 with enough configuration overhead to make it impractical for large courses. It is now a routine assignment design choice.

---

## Accessibility as a Legitimate Deployment Frame

The UW-Milwaukee case is worth examining more carefully than it usually gets, because "optional audio resource" sounds like a minimal intervention and is sometimes dismissed as not really deploying AI in a pedagogically serious way.

That framing misses what the deployment was actually for. Ed Price was working with students whose math anxiety was a genuine cognitive barrier — not a motivation problem, not a laziness problem, a barrier that prevented engagement with the material before the problem-solving work could even begin. The Audio Overview served as an anxiety-reducing on-ramp. Students who would otherwise disengage from a dense chapter entirely were arriving to in-person sessions with enough familiarity to participate.

The pedagogical bar for an accessibility resource is not "did this student do the work in the canonical way?" It is "did this student end up able to do the work?" By that bar, the UW-Milwaukee deployment worked.

NotebookLM provides specific accessibility affordances that matter at the undergraduate scale: closed captions on all Audio and Video Overview outputs, multilingual output for some output types, multimodal review for students with reading-comprehension difficulties. These affordances do not make the retrieval-practice framework inapplicable — they make it accessible to students who would otherwise be excluded from the framework before reaching the cognitive work that matters.

The design rule that follows: accessibility deployments should be optional and not high-stakes. Required high-stakes use of an Audio Overview is the wrong design for an accessibility resource, for the same reason that making accommodations mandatory is the wrong design for accommodations.

---

## What I Don't Fully Understand

The last question in this chapter is the one I find hardest to answer. The retrieval-practice literature is clear that retrieving builds the capability to retrieve. What is not clear is whether that generalizes across an AI scaffold.

Specifically: does habitual AI-scaffolded self-testing build the student's independent capacity to self-test, or does it create a dependency on the structured framework that disappears when the tool is not available? A student who has spent a semester using Learning Guide's "ask me one question at a time" configuration may or may not have developed the metacognitive habit of self-quizzing without the scaffold. The retrieval events happened. Whether they transferred to the habit of generating retrieval events independently is an open empirical question.

Three things remain genuinely uncertain to me. Whether Learning Guide's question quality varies enough across disciplines — humanities, STEM, professional fields — to require discipline-specific configuration guidance that does not yet exist. Whether the NYU feedback-loop pattern generalizes to small-class settings or requires the data volume of a large lecture. And whether the most powerful deployment is during initial learning, as the chapter argues, or whether spacing effects — returning to material after a gap — actually dominate in typical undergraduate course structures where students do not control their own study schedules in the way the research assumes.

The retrieval-practice mechanism is robust. Whether AI-generated questions are good enough to reliably produce it, across all the contexts faculty deploy them, is the empirical bet this chapter makes.

---

**LLM Exercises**

*Use a language model to complete the following.*

**1. Generate and examine.** Take the Learning Guide configuration prompt from this chapter — "Test me on [topic]. Ask me one diagnostic question at a time. Do not give me the answer until I have attempted. If I am wrong, give me a more scaffolded question rather than explaining." — and paste it into an LLM along with a brief description of a course topic you teach. Ask the LLM to simulate three rounds of the diagnostic sequence. Evaluate the questions it generates: are they testing the concept you care about, or are they pattern-matching on surface features of the topic? What would you change in the configuration prompt to get better questions?

**2. Apply to known context.** Take the NYU feedback-loop pattern and apply it to a course you are currently teaching or have recently taught. Collect whatever student-confusion signal you have available — assignment feedback notes, common errors, student questions. Paste that data into an LLM and ask it to identify three concepts where confusion is concentrated and to generate one formative assessment activity for each. Evaluate the activities against your own knowledge of where students are actually stuck. Where did the LLM identify real confusion? Where did it miss?

**3. Stress-test a specific claim.** The chapter claims that Learning Guide is most powerful during initial learning, not review. Ask an LLM to construct the strongest counterargument: why might spaced retrieval after encoding be more practically useful in an undergraduate course context than retrieval during initial exposure? Evaluate the argument. Does it identify constraints — course structure, student preparation, contact-hour limits — that the chapter's framing doesn't account for? Use whatever is valid in the counterargument to qualify your own deployment design.

**4. Draft or audit a professional deliverable.** Write the student-facing instructions for a Learning Guide self-testing assignment in a course you teach — including the specific configuration prompt students should use, what they should bring to class afterward, and how the assignment will be assessed. Ask an LLM to critique the instructions for clarity and for whether they will reliably produce retrieval-practice behavior rather than explanation-seeking. Revise based on the critique.
