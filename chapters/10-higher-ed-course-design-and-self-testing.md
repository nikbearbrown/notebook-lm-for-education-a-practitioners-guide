# Chapter 10 — Higher Education: Course Design and the Self-Testing Model

*The Monash model — configure NotebookLM to quiz the learner, not explain to them — is the highest-leverage use case for undergraduate course integration.*

---

Here is a puzzle worth sitting with.

Two universities deploy NotebookLM in undergraduate courses. Both deployments work. The design principles behind them are almost opposite.

At UW-Milwaukee, a teaching consultant named Ed Price was working with a remedial math course — students who arrived with genuine math anxiety, the kind that shuts down cognition before the problem is half-read. He generated podcast-style Audio Overviews of the mathematical units and embedded them in Canvas as optional resources with closed captions. Students who chose to listen reported feeling more comfortable during in-person problem-solving sessions. Price's conclusion was careful: the tool works as a supplementary companion to dense material, not as a replacement for active study.

At Monash University, the deployment looks nothing like this. Monash configures Learning Guide as a self-testing companion — not a tool that explains things to students, but a tool that asks students diagnostic questions, waits for their answers, and evaluates before offering feedback. The tool is the assignment. Engagement is not optional. The design is retrieval-practice from the first moment.

Both of these are right. They are right for different reasons, and mixing the reasons produces failures that are entirely predictable once you see what each design principle actually is.

UW-Milwaukee is running *accessibility plus optionality*. The resource is there for students who benefit; the rest of the class is not required to use it; the audio does not replace any required work. Monash is running *retrieval-practice integration*. The tool is the required cognitive event — not a supplement to learning but the mechanism that produces it.

A faculty member who doesn't know which principle they are deploying will end up with something that is neither. They'll make the audio required and high-stakes, which is the wrong design for an accessibility resource. Or they'll make the self-testing optional and ungraded, which is the wrong design for a retrieval-practice tool. The chapter's job is to make the distinction clear enough that you cannot mix them by accident.

---

## Why Retrieval Practice Is the Right Frame for Learning Guide

![Learning curve comparison ](images/10-higher-ed-course-design-and-self-testing-fig-01.png)
*Figure 10.1 — Learning curve comparison *

The pedagogical foundation for the Monash model is decades old and unusually solid. Karpicke and Roediger, writing in *Science* in 2008, showed that retrieval practice — being asked to recall information from memory, rather than re-reading or re-listening — produces dramatically more durable learning. The finding has replicated. It holds across subjects, ages, and content types with enough consistency to call it one of the most reliable results in educational psychology.

Here is the mechanism, stated plainly. When you encounter new information and then retrieve it — try to recall it, attempt to produce it, answer a question about it — you strengthen the memory trace in a way that passive re-exposure does not. The effort of retrieval is not a side effect. It is the event that produces learning. A tool that bypasses that effort, by explaining rather than testing, removes the cognitive event you actually needed.

This is why the default tutoring pattern — student asks a question, tool provides an explanation — is the least efficient use of a learning tool that is capable of doing something more demanding. The explanation feels useful. It is comfortable. The student finishes feeling like they understood. But the understanding is fragile in a way that retrieved understanding is not, because the retrieval event never happened.

The Monash configuration inverts this. Instead of the student asking *"explain X,"* the student invokes Learning Guide with *"test me on chapter 4."* The tool generates diagnostic questions one at a time. The student attempts each one. The tool evaluates and provides feedback only after the student has tried. The discomfort is the point. The effort of trying and being wrong before seeing the correct framing is exactly what produces learning that sticks.

![Diagram ](images/10-higher-ed-course-design-and-self-testing-fig-02.png)
*Figure 10.2 — Diagram *

There is a timing detail here that matters and that most deployments miss. Learning Guide is most powerful during *initial learning* — as the encoding event, the first time the student works through the material. Most faculty deploy self-testing tools as review, after the fact, as a check that learning happened. That is less than half the leverage. Used before the student has consolidated the material, the tool is forcing the retrieval attempt that produces the encoding. Used after, it is measuring what the encoding produced. Both have value; the first has more.

---

## The Configuration That Produces This

| Configuration approach | Default student behavior | What changes with explicit prompt | Pedagogical effect |
|---|---|---|---|
| No configuration (default invocation) | Student asks the tool to explain; tool delivers an explanation | — | Tutoring-by-explanation; minimal retrieval practice; comprehension feeling but limited durable learning |
| Quiz-me-on-X prompt | Tool generates diagnostic questions one at a time | Student answers before tool evaluates | Retrieval practice; durable learning per Karpicke & Roediger 2008 |
| Test-then-explain prompt | Tool tests first; only after student attempts does it explain | Forced retrieval as encoding event | Strongest learning effect — failed retrievals still strengthen subsequent learning (the "desirable difficulty" finding) |
| Discipline-specific configuration via teacher Note | Tool's diagnostic questions are tuned to the course's framing, level, and prior knowledge | Teacher's pedagogical content knowledge enters the corpus | Question quality and contextual relevance rise; tool becomes course-specific rather than generic |
The Monash model requires explicit configuration, and that configuration has to be taught to students. Students who are handed a notebook without instructions will do what comes naturally: they will ask the tool to explain things. The tool will oblige. The retrieval event will not occur. The deployment will look fine and produce less than it could.

The configuration is not complicated. It is a matter of what the student types.

Default behavior: *"Explain regression to the mean."* Tool response: two paragraphs of explanation, source-grounded. Student learns something; student doesn't retain it as well as they would have with a retrieval attempt.

Monash configuration: *"Test me on chapter 4. Ask me one diagnostic question at a time. Do not give me the answer until I have attempted. If I am wrong, give me a more scaffolded question rather than explaining."* Tool response: a diagnostic question. Student attempts. Tool evaluates. If wrong, another question. The explanation arrives only after effort.

The difference is entirely in how the student invokes the tool. This means the teacher's job at deployment is to write that configuration prompt into the student-facing instructions — not as an optional suggestion, but as the assignment itself. *Before our Friday session, open the class notebook and invoke Learning Guide with the prompt "Test me on chapter 4 applications." Work through at least three diagnostic questions. Bring to class: one question you struggled with, one question that made the concept click.*

Two things make this work that would otherwise break it. First, the student-facing instructions must be specific about the invocation prompt, not just about the goal. "Use Learning Guide to study chapter 4" produces explanation-seeking. "Invoke Learning Guide with this exact prompt" produces self-testing. The specificity is not pedantic; it is the mechanism.

Second, the teacher should generate the question set themselves before deploying to students. Learning Guide's diagnostic questions are good enough to be useful and inconsistent enough to require review. Some questions are sharp, well-targeted, testing exactly the concept you want tested. Some are formulaic, pattern-matching on textbook phrasing without testing actual understanding. Some are ambiguous. Five minutes of question review per assignment — generating the set yourself, identifying the weak ones, cutting or flagging them — is cheap relative to the cost of deploying weak questions to 200 students who will form wrong impressions of what they're supposed to understand.

---

## The NYU Feedback Loop

![NYU feedback-loop workflow ](images/10-higher-ed-course-design-and-self-testing-fig-03.png)
*Figure 10.3 — NYU feedback-loop workflow *

At NYU's October 2025 Teaching and Learning with Generative AI symposium, an instructor showed a use case that looks nothing like either the UW-Milwaukee or Monash models, but is worth understanding because it demonstrates the bounded-tool framework applied in a direction most faculty don't consider.

The context: a large introductory programming course. Mid-semester student feedback, grading patterns from assignments, polling responses from in-class sessions. The instructor's question: *where are students actually stuck?*

The workflow was this. Collect the feedback data — surveys, confusion patterns from grading, polling responses. Upload that data to NotebookLM as a source. Query: *"Based on this feedback, what three concepts are students most struggling with? Generate a formative assessment activity targeting each."* Deploy the activities through the LMS and polling tools.

What is happening here is different from content generation for students. NotebookLM is functioning as a *teaching analytics instrument* — the input is student data, the output is insight and response that the *teacher* then acts on. The tool is not in the student-facing workflow at all. It is in the faculty workflow, processing information about students to improve the course while it is running.

| | UW-Milwaukee accessibility | Monash self-testing | NYU feedback loop |
|---|---|---|---|
| Who interacts with the tool | Individual student (optional) | Individual student (required) | Instructor |
| What the input is | Course readings (instructor-uploaded) | Course readings (instructor-uploaded) | Student feedback data + assessment results |
| What the output is | Audio Overview as supplementary on-ramp | Diagnostic questions for self-testing | Identified concepts students struggle with + targeted formative activities |
| Who acts on the output | Student (uses it to engage with the material) | Student (answers, receives feedback) | Instructor (designs targeted intervention) |
| Design principle | Accessibility + optionality | Retrieval-practice integration | Teaching-analytics from student data |
This matters because it reveals a deployment pattern that works even for faculty who are uncertain about putting AI tools directly in students' hands. The question *"is NotebookLM appropriate for student use in my course?"* is separate from *"can I use NotebookLM to improve how I teach this course?"* The NYU case answers the second question affirmatively without touching the first.

The limitation worth noting: the NYU feedback-loop pattern benefits from data volume. A large lecture generates enough feedback signal that the analysis produces genuinely useful patterns. In a seminar of twelve students, you may already know where everyone is stuck, and the analysis step adds overhead without insight. The tool generalizes to the problem of knowing where a crowd is confused; it does not generalize to the problem of knowing where a specific student is confused, which remains a human judgment.

---

## What Changed in April 2026

![Timeline of NotebookLM access expansion ](images/10-higher-ed-course-design-and-self-testing-fig-04.png)
*Figure 10.4 — Timeline of NotebookLM access expansion *

A higher-education-specific operational fact: as of April 2026, students aged 18 and older can create personal class notebooks grounded in educator-provided Classroom materials. This is the operational unlock the Monash model was waiting for at scale.

Before this expansion, the fully individualized self-testing deployment — each student with their own notebook, their own diagnostic history, their own Learning Guide session — required either institutional provisioning or workarounds. After it, a faculty member can design assignments that depend on individual student notebooks rather than shared class notebooks, and students who have institutional Google Workspace accounts can instantiate those notebooks themselves.

The practical constraint that remains: institutional Workspace settings vary. Some institutions enabled the feature; others have not configured it. Confirm before designing assignments that depend on individual student notebook creation. The design assumption that students can do this is safe to make; the deployment assumption requires verification with your institution's IT or academic technology office.

The pedagogical implication of the expansion is worth stating directly. The Monash model at scale requires students to build their own notebooks from course materials — not to consume a teacher-built notebook, but to instantiate their own retrieval-practice environment from the sources the teacher provides. That design was possible before April 2026 with enough configuration overhead to make it impractical for large courses. It is now a routine assignment design choice.

---

## Accessibility as a Legitimate Deployment Frame

The UW-Milwaukee case is worth examining more carefully than it usually gets, because "optional audio resource" sounds like a minimal intervention and is sometimes dismissed as not really deploying AI in a pedagogically serious way.

That framing misses what the deployment was actually for. Ed Price was working with students whose math anxiety was a genuine cognitive barrier — not a motivation problem, not a laziness problem, a barrier that prevented engagement with the material before the problem-solving work could even begin. The Audio Overview served as an anxiety-reducing on-ramp. Students who would otherwise disengage from a dense chapter entirely were instead arriving to in-person sessions with enough familiarity with the material to participate.

The pedagogical bar for an accessibility resource is not *did this student do the work in the canonical way?* It is *did this student end up able to do the work?* By that bar, the UW-Milwaukee deployment worked.

NotebookLM provides specific accessibility affordances that matter at the undergraduate scale: closed captions on all Audio and Video Overview outputs, multilingual output for some output types (expanding through 2026), multimodal review for students with reading-comprehension difficulties or visual-processing differences. These affordances do not make the retrieval-practice framework inapplicable — they make it accessible to students who would otherwise be excluded from the framework before reaching the cognitive work that matters.

The design rule that follows: accessibility deployments should be optional and not high-stakes. Required high-stakes use of an Audio Overview is the wrong design for an accessibility resource, for the same reason that making accommodations mandatory is the wrong design for accommodations. The resource serves students who need it when it is available but not required. It stops serving them when the course is structured to punish non-use.

---

## What Would Change the Chapter's Position

The Educational Psychology Review published findings in 2025 suggesting that AI-generated quiz questions can match teacher-created materials for self-assessment use. If a controlled comparison study of Learning-Guide-configured self-testing against instructor-designed self-testing showed equivalent or worse learning outcomes for the AI version at the same student time investment, the chapter's central recommendation would require revision. The retrieval-practice mechanism is robust; whether AI-generated questions are good enough to produce that mechanism reliably is the empirical question the chapter bets on.

Three things still genuinely uncertain. Whether Learning Guide's question quality varies enough across disciplines — humanities, STEM, professional fields — to require discipline-specific configuration guidance that doesn't exist yet. Whether the NYU feedback-loop pattern generalizes to small-class settings or requires the data volume of a large lecture course. And what the long-term effect of habitual AI-scaffolded self-testing is on student metacognition — whether it builds the capacity to self-test independently, or whether it creates a dependency on the structured framework that disappears when the tool does.

That last question is the one I find hardest to answer. The retrieval-practice literature is clear that retrieving builds the capability to retrieve. Whether that generalizes across the AI scaffold is a genuinely open empirical question.

---

## LLM Exercises

1. Take the Learning Guide configuration prompt from this chapter — *"Test me on [topic]. Ask me one diagnostic question at a time. Do not give me the answer until I have attempted. If I am wrong, give me a more scaffolded question rather than explaining."* — and paste it into an LLM along with a brief description of a course topic you teach. Ask the LLM to simulate three rounds of the diagnostic sequence. Evaluate the questions it generates: are they testing the concept you care about, or are they pattern-matching on surface features of the topic? What would you change in the configuration prompt to get better questions?

2. Take the NYU feedback-loop pattern and apply it to a course you are currently teaching or have recently taught. Collect whatever student-confusion signal you have available — assignment feedback notes, common errors, student questions. Paste that data into an LLM and ask it to identify three concepts where the confusion is concentrated and to generate one formative assessment activity for each. Evaluate the activities against your own knowledge of where students are actually stuck. Where did the LLM identify real confusion? Where did it miss?

3. The chapter claims that Learning Guide is most powerful during initial learning, not review. Ask an LLM to construct the strongest counter-argument: why might spaced retrieval after encoding be more practically useful in an undergraduate course context than retrieval during initial exposure? Evaluate the argument. Does it identify constraints — course structure, student preparation, contact-hour limits — that the chapter's framing doesn't account for? Use whatever is valid in the counter-argument to qualify your own deployment design.

---

## Chapter Summary

You can now distinguish the accessibility-plus-optionality and retrieval-practice-integration design principles, and you know what goes wrong when they are mixed. You can configure Learning Guide for self-testing rather than explanation, write the student-facing instructions that produce the configuration, and review the question quality before deployment. You understand the NYU feedback-loop pattern as a faculty-facing use of the tool distinct from student-facing use. You know what the April 2026 expansion unlocks for individual-notebook assignment design.

The one idea from this chapter that matters most: retrieval practice is the mechanism that produces durable learning, and Learning Guide is powerful precisely because it can force that mechanism rather than bypass it. The default tutoring pattern bypasses it. The Monash configuration preserves it. The difference is what the student types.

The common mistake: deploying the self-testing model as a review tool rather than an encoding tool. Used after the fact, it measures learning. Used during initial engagement with the material, it produces it. The timing is the leverage.

The Feynman test: explain to a colleague why a tool that explains things to students is less pedagogically valuable than the same tool configured to ask students questions. If you can walk them through the retrieval-practice mechanism — what the encoding event is, why effort before feedback matters, why comfortable re-reading produces less retention than uncomfortable retrieval — you have the chapter.

---

## Where This Leads

Both the K–12 and higher-education deployment paths converge here. Chapter 11 addresses what comes next for all contexts: equitable institutional deployment, the administrative and policy layer that sits above individual course design, and what it means for an institution to deploy a tool like this fairly across the full range of students it serves.

---

*Learning Guide's configuration interface and specific feature set are evolving. The retrieval-practice mechanism it leverages is not — the Karpicke and Roediger finding has been stable for nearly two decades. Re-verify the specific UI configuration steps before each reprint; the underlying argument can be re-issued unchanged.*

## Prompts

Use these prompts with Claude to generate interactive D3 v7 versions of the
figures in this chapter. Each produces a standalone HTML file you can open
in a browser and modify freely.

**Prerequisites:** Load `brutalist/CLAUDE.md` and `brutalist/DESIGN.md` into
your Claude project context before using these prompts. They define the stack,
naming conventions, color system, and typography the figures use.

---

### Figure 10.1 — Learning curve comparison 

Create a standalone D3 v7 HTML file for Figure Learning curve comparison . Use the CDN https://cdnjs.cloudflare.com/ajax/libs/d3/7.9.0/d3.min.js, inline CSS, ResizeObserver redraw, SVG role="img", aria-labelledby, title, and desc. Build the figure from this structural brief: Learning curve comparison — retrieval practice vs. re-reading/re-listening — data from Karpicke & Roediger 2008, showing durable retention gap over time. Use the described data shape and labels; when exact values are not supplied, use plausible illustrative values that preserve the relationships in the brief. Use a zero baseline for bars or areas, direct labels where possible, and annotations named in the brief. Use only DESIGN.md color variables and the required serif/mono font split.

> Reference implementation: `d3/10-higher-ed-course-design-and-self-testing-fig-01.html`

---

### Figure 10.2 — Diagram 

Create a standalone D3 v7 HTML file for Figure Diagram . Use the CDN https://cdnjs.cloudflare.com/ajax/libs/d3/7.9.0/d3.min.js, inline CSS, ResizeObserver redraw, SVG role="img", aria-labelledby, title, and desc. Build the figure from this structural brief: Side-by-side diagram — default tutoring pattern (student asks → tool explains) vs. Monash retrieval pattern (tool asks → student attempts → tool evaluates) — annotated with where the learning-producing event occurs in each. Use the described data shape and labels; when exact values are not supplied, use plausible illustrative values that preserve the relationships in the brief. Use a zero baseline for bars or areas, direct labels where possible, and annotations named in the brief. Use only DESIGN.md color variables and the required serif/mono font split.

> Reference implementation: `d3/10-higher-ed-course-design-and-self-testing-fig-02.html`

---

### Figure 10.3 — NYU feedback-loop workflow 

Create a standalone D3 v7 HTML file for Figure NYU feedback-loop workflow . Use the CDN https://cdnjs.cloudflare.com/ajax/libs/d3/7.9.0/d3.min.js, inline CSS, ResizeObserver redraw, SVG role="img", aria-labelledby, title, and desc. Build the figure from this structural brief: NYU feedback-loop workflow — data collection → NotebookLM analysis → formative activity generation → LMS deployment → cycle back to data collection. Use the described data shape and labels; when exact values are not supplied, use plausible illustrative values that preserve the relationships in the brief. Use a zero baseline for bars or areas, direct labels where possible, and annotations named in the brief. Use only DESIGN.md color variables and the required serif/mono font split.

> Reference implementation: `d3/10-higher-ed-course-design-and-self-testing-fig-03.html`

---

### Figure 10.4 — Timeline of NotebookLM access expansion 

Create a standalone D3 v7 HTML file for Figure Timeline of NotebookLM access expansion . Use the CDN https://cdnjs.cloudflare.com/ajax/libs/d3/7.9.0/d3.min.js, inline CSS, ResizeObserver redraw, SVG role="img", aria-labelledby, title, and desc. Build the figure from this structural brief: Timeline of NotebookLM access expansion — K-12 supervised model, 18+ personal notebook creation, institutional Workspace configuration. Use the described data shape and labels; when exact values are not supplied, use plausible illustrative values that preserve the relationships in the brief. Use a zero baseline for bars or areas, direct labels where possible, and annotations named in the brief. Use only DESIGN.md color variables and the required serif/mono font split.

> Reference implementation: `d3/10-higher-ed-course-design-and-self-testing-fig-04.html`
