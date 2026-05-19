# Research Notes: Chapter 12 — Choosing the Right Tool: NotebookLM, ChatGPT, Copilot, Perplexity

**Source:** TIKTOC.md chapter entry
**Notes file:** 12-choosing-the-right-tool_notes.md
**Corresponding chapter:** chapters/12-choosing-the-right-tool.md (not yet written)
**Generated:** 2026-05-19

---

## Chapter summary (from TIKTOC.md)

**One-line:** The right tool is the one whose design constraint matches your learning goal. For "understand these assigned sources," that tool is usually NotebookLM. For everything else, check.

**Problem this chapter solves:** Educators face tool proliferation and need a decision framework that is specific enough to be useful without aging out in six months.

**Learning outcomes:**
1. (Analyze) Apply the four-question tool selection framework.
2. (Evaluate) Identify educational tasks for which NotebookLM is NOT the best tool.
3. (Create) Produce a tool selection guide for a department or grade team.

**Opening:** Same learning goal — "prepare students to discuss this article" — served by four different tools. The chapter works through why each tool's design makes it more or less appropriate.

---

## A. Conceptual foundations

### Concept 1 — The four-question tool selection framework

The chapter's central decision tool:

1. **What is the learning goal?** State as a verb (understand, evaluate, generate, defend).
2. **Is the source set defined and uploadable?** If yes → bounded tool likely fits. If no → open-loop tool likely fits.
3. **Is citation back to sources a requirement?** If yes → NotebookLM or Perplexity. If no → range expands.
4. **Is privacy a constraint?** Student data, institutional data, regulated data. If yes → institutional-account tools and / or local-deployment alternatives.

The framework is deliberately decision-tree shaped. Each question narrows the candidate set. By the fourth question, usually 1-2 tools remain and the educator chooses among them.

**Common misconception:** "The same tool is always the right tool." Tool selection should be re-asked per task. The educator who defaults to one tool for everything is matching tool capability to convenience, not to learning goal.

**Source(s):** Synthesis of pantry research file "Comparison to Competing Tools" + practitioner sources.

---

### Concept 2 — The four-tool comparison

| Tool | Best fit | Strength | Weakness |
|---|---|---|---|
| **NotebookLM** | Course-material study, teacher-curated notebooks, reading synthesis, multimodal study aids | Source-grounded; strong for "understand this assigned packet" | Less flexible than general chat; quality depends heavily on uploaded sources |
| **ChatGPT / ChatGPT Edu** | Tutoring, writing support, coding, brainstorming, custom GPTs, multimodal reasoning | Broadest general-purpose capability; ChatGPT Edu offers university deployment, GPT-4o, vision, data analysis | Less inherently bounded to course materials unless carefully configured |
| **Microsoft Copilot** | Schools already in Microsoft 365; Word, PowerPoint, Teams, OneNote, Outlook workflows | Deep M365 integration; enterprise controls; Study and Teach modes are education-specific | Strongest inside Microsoft ecosystem; less "course packet as notebook" than NotebookLM |
| **Perplexity AI** | Research discovery, current web search, source-backed quick investigation | Strong for up-to-date web answers with citations | More search engine than learning environment; weak LMS integration |

(Reproduced from pantry research file; the comparison table is the chapter's reference artifact.)

**Source(s):** pantry research file "Comparison to Competing Tools" section.

---

### Concept 3 — When ChatGPT/ChatGPT Edu is the better choice

- **Tutoring on material not pre-uploaded.** A student wrestling with calculus needs a tutor that can produce worked examples for any problem, not just the assigned ones.
- **Custom GPTs.** Faculty building course-specific GPT assistants — these are configurable beyond NotebookLM's current customization layer.
- **Code generation and debugging.** ChatGPT's coding capability is currently stronger than NotebookLM's for this use case.
- **Open-ended brainstorming.** When the goal is generation from a wide associative space rather than synthesis from a curated source set.

**Source(s):** Practitioner observation; OpenAI's published ChatGPT Edu materials [verify current URL].

---

### Concept 4 — When Copilot is the better choice

- **Schools deeply embedded in Microsoft 365.** The integration into Word, Teams, Outlook is operational, not just additive.
- **Document-centric workflows where the document is already in M365.** Drafting in Word with Copilot is faster than uploading to NotebookLM.
- **Enterprise data governance requirements that align with M365 architecture.** Some institutional contexts have already negotiated M365 data terms; replicating with Google would require separate negotiation.

**Source(s):** Microsoft's published Copilot for Education materials [verify URLs].

---

### Concept 5 — When Perplexity is the better choice

- **Up-to-date web research.** Perplexity searches the live web and returns cited answers. NotebookLM stays in your sources unless Deep Research is invoked.
- **Quick fact-finding tasks where citation-back-to-source matters.** Perplexity returns more compact citations than the in-doc passages NotebookLM provides.
- **Research framing before deep reading.** Perplexity can help identify which sources to read; NotebookLM is for working with sources after that decision.

**Source(s):** Perplexity AI published materials and practitioner observation.

---

## B. Domain examples and cases

### Case 1 — Same learning goal, four tools (chapter opening)

Learning goal: "prepare students to discuss next class's article on cognitive bias."

- **NotebookLM:** Upload the article. Generate Study Guide, Audio Overview, flashcards. Students engage with the assigned material.
- **ChatGPT:** Ask "explain cognitive bias to a college sophomore." Generates a tutorial. Students may or may not read the actual article.
- **Copilot:** If the article is in a OneDrive folder, Copilot can summarize it within Word. Students get a summary inside their workflow.
- **Perplexity:** Search "cognitive bias 2025 research." Get a tour of the broader literature. The assigned article may or may not appear.

Three of these are wrong for the stated goal. Only NotebookLM is bounded to the assigned source. The others may be useful for adjacent goals — but they don't serve *this* goal.

### Case 2 — When NotebookLM is wrong

A student is debugging a Python script for a class project. The script's behavior depends on a library version the student doesn't have documentation for. NotebookLM cannot help — there is no curated source set. ChatGPT can help — it has read documentation across the open web. This is the case where defaulting to NotebookLM is the wrong choice.

### Failure case — Tool monoculture

A faculty member commits to "I will always use NotebookLM" and uses it for tasks where it doesn't fit (open-ended generation, tutoring on unanticipated material, debugging). The work gets worse than it would have with the right tool. The lesson: tool selection should be task-specific, not allegiance-based.

---

## C. Connections and dependencies

**Prerequisites:**
- Chapters 1-3 (operational fluency with NotebookLM)
- General awareness that other AI tools exist

**Unlocks:**
- Chapter 13 (administrator brief) — selection rationale supports the deployment case
- Chapter 14 (honest capability assessment) — fits NotebookLM's claims into the broader tool landscape

**Adjacent chapter connections:**
- **Chapter 3:** Output-type selection within NotebookLM; this chapter is tool selection across tools
- **Chapter 13:** The brief should justify why NotebookLM is the chosen tool when other tools exist
- **Chapter 14:** Honest assessment requires knowing when NotebookLM isn't the right choice

---

## D. Current state of the field

**Settled:**
- The four-tool comparison space is the operating set for most US educational institutions through 2026
- Tool choice should be task-specific; tool monoculture produces predictable failures
- Citation-grounded outputs (NotebookLM, Perplexity) are structurally different from open-loop outputs (ChatGPT, Copilot in default mode)

**Contested or emerging:**
- Whether the four-tool comparison will hold or whether one tool will consolidate dominance in education
- Whether educational institutions should adopt one tool (consistency) or multiple (specialization)

**Key references:**
1. pantry research file "Comparison to Competing Tools"
2. Google NotebookLM, OpenAI ChatGPT Edu, Microsoft Copilot for Education, Perplexity AI published materials
3. EDUCAUSE Horizon Report (annual) on edtech tool landscape

**Recent developments:**
- ChatGPT Edu rollouts at major universities (2024-2025)
- Microsoft Copilot Edu integration expansion through M365
- Perplexity educational pricing and partnerships (2025-2026)

---

## E. Teaching considerations

**Where readers get stuck:**
- They want a single tool recommendation. The chapter resists: the right tool depends on the task.
- They treat the comparison table as a ranking rather than a fit-finder.
- They underestimate how task-specific the tool choice is.

**Analogies that work:**
- The kitchen-tools analogy: a chef does not use the same knife for everything. A chef's knife is general-purpose; a paring knife, a bread knife, a fillet knife each have specific fit. NotebookLM is a particular knife. Use it for what it's for.

**Exercises:**
- Analyze level: Take three recent educational tasks. Apply the four-question framework. Identify whether you used the right tool.
- Create level: Produce a one-page tool selection guide for your department, with 3-5 task patterns and the recommended tool for each.

---

## F. Library files relevant to this chapter

- `_lib_EdTech.md` — Adoption context and tool landscape.
- `_lib_Co-Intelligence_Mollick.md` — Mollick's tool-agnostic framing of AI augmentation.

---

## G. Gaps and flags

- **FLAG:** Tool feature sets evolve quickly. The comparison table is May-2026-accurate; specific feature claims should be re-verified before chapter publication.
- **GAP:** The chapter could benefit from worked-example dialogs showing the four-question framework in action across diverse educational tasks. Pantry has the principle; the dialogs are author's work.
- **FLAG:** ChatGPT Edu pricing and feature differentiation vs. ChatGPT Plus may change; the chapter should be specific about which tier the analysis assumes.
