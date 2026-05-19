# Pantry Index — NotebookLM for Education: A Practitioner's Guide

*Last updated: 2026-05-18 (Research Gatherer pass)*

This directory holds gathered research material for the 14-chapter book. Nothing here is compiled into the final book. Chapter authors read these files before drafting and cite the primary sources they reference (not the notes files themselves).

---

## Research notes (generated 2026-05-18)

One notes file per chapter. Each follows the Research Gatherer template — conceptual foundations, domain examples, connections, current state of the field, teaching considerations, library files referenced, gaps and flags.

| File | Chapter | Description |
|------|---------|-------------|
| `01-the-bounded-tool_notes.md` | Ch 1 | RAG architecture; what "bounded" means; three structural differences for ed deployment; LearnLM |
| `02-your-first-notebook_notes.md` | Ch 2 | 30-min walkthrough; source ingestion failure modes; Studio output zoo; citation verification |
| `03-output-type-is-a-pedagogical-choice_notes.md` | Ch 3 | Active/passive spectrum; output decision framework; Note-to-Source loop |
| `04-the-k12-teacher_notes.md` | Ch 4 | 45-minute unit prep sequence; tiered scaffolds; teacher-customized framing |
| `05-the-k12-student_notes.md` | Ch 5 | Active vs passive assignment design; four engagement patterns; the shortcut trap |
| `06-google-classroom-integration_notes.md` | Ch 6 | Phased rollout (Sept 2025 / April 2026); age restrictions; admin toggle landscape |
| `07-assessment-redesign_notes.md` | Ch 7 | Three-question audit; four redesign frameworks; version-history as pedagogical tool |
| `08-academic-integrity_notes.md` | Ch 8 | MDPI 2025 finding (ethical beliefs > policy awareness); FSU red flags; disclosure mechanism |
| `09-higher-ed-research-and-synthesis_notes.md` | Ch 9 | Cross-corpus synthesis; Note-to-Source for outlines; the irreducibly-human research moves |
| `10-higher-ed-course-design-and-self-testing_notes.md` | Ch 10 | Monash self-testing; NYU feedback loop; UW-Milwaukee accessibility companion |
| `11-privacy-equity-and-the-access-gap_notes.md` | Ch 11 | Institutional vs personal account gap; three access gates; open-source alternatives |
| `12-choosing-the-right-tool_notes.md` | Ch 12 | Four-question framework; NotebookLM/ChatGPT/Copilot/Perplexity comparison |
| `13-the-administrator-brief_notes.md` | Ch 13 | One-page brief structure; the three administrator questions and answers |
| `14-honest-capability-assessment_notes.md` | Ch 14 | Four-bucket evidence framework; Gulf University case; aging-risk principle |

---

## Library files (copied from shared MD library 2026-05-18)

These are book-length texts already in the shared library at `/Users/bear/Documents/CoWork/bear-textbooks/MD/`, copied here for chapter-author convenience. Files are sizeable (hundreds of KB to over 1 MB) — chapter authors should dip into the relevant sections, not read end-to-end.

| File | Relevant to | Notes |
|------|------------|-------|
| `_lib_Co-Intelligence_Mollick.md` | Ch 1, 5, 7, 8, 12, 14 | Mollick on AI-as-collaborator and the centaur model. Frames the chapter argument that AI augments rather than replaces. |
| `_lib_The_Digital_Delusion_Horvath.md` | Ch 1, 5, 7, 8, 11, 14 | Jared Cooney Horvath's skeptical cognitive-science perspective on edtech. Essential counterweight; the "but the appearance of learning isn't learning" argument lives here. |
| `_lib_Teaching_for_Deeper_Learning_McTighe_Silver.md` | Ch 4, 5, 7, 10 | McTighe & Silver. Backward design and deeper-learning frameworks. Directly cited in TIKTOC Ch 7. |
| `_lib_EdTech.md` | All chapters | General edtech context; large file, dip in for adoption-history background. |
| `_lib_Humanitarians_AI_Course_Template.md` | Ch 4, 10 | Course-template example showing how AI-augmented curriculum can be structured. |
| `_lib_NEU_Global_Collaboration_Chatbot.md` | Ch 6, 9, 10, 11, 13 | Northeastern's pattern for an institution-level chatbot deployment — governance, privacy, equity considerations applicable to NotebookLM institutional decisions. |

---

## Other pantry contents (pre-existing — preserved)

| File | Description |
|------|-------------|
| `825379524-Notebook-LM-Masterclass-Ebook.txt` | A NotebookLM masterclass / how-to text. Feature-mechanics reference. |
| `994984763-NotebookLM.txt` | Additional NotebookLM source document. Feature-mechanics reference. |
| `notebooklm_education_research.md` | **The primary research dump.** ~9,000 words, dated May 2026. Covers the topical territory of all 14 chapters at the feature, case-study, evidence, and policy level. **Every chapter's notes file references and synthesizes from this document.** Chapter authors should read it before drafting any chapter. |

---

## Use notes for chapter authors

1. **Start with `notebooklm_education_research.md`.** It is the comprehensive reference and dates from May 2026 — more current than any model's training cutoff for NotebookLM specifics.
2. **Then read the chapter's `NN-...notes.md` file.** Each notes file is a synthesized scaffold structured around what the chapter needs to do.
3. **Dip into the relevant `_lib_*` files for citation-grade primary material** — especially the McTighe & Silver, Horvath, and Mollick books, which are likely to be cited multiple times across chapters.
4. **Verify time-sensitive claims** (feature lists, age restrictions, subscription tier numbers, specific Google rollout dates) against current Google documentation before drafting. The pantry's May 2026 dating is the floor; the chapter publication date is the ceiling.
5. **Every chapter's `G. Gaps and flags` section is the author's checklist** for what needs additional verification or fresh research before the chapter can ship.

---

## Coverage map — TIKTOC chapter requirements against pantry depth

| Chapter | Notes file | Pantry research depth | Library backing | Fresh-research gaps named |
|---|---|---|---|---|
| 1 | ✓ | Deep | Mollick, Horvath, EdTech | RAG citation verification |
| 2 | ✓ | Deep | Masterclass + NotebookLM text | Screenshots; current UI |
| 3 | ✓ | Deep | McTighe & Silver | Output-zoo currency |
| 4 | ✓ | Deep | McTighe & Silver, Humanitarians template | Time-and-motion data |
| 5 | ✓ | Deep | Horvath, McTighe & Silver, Mollick | Bastani context for NotebookLM |
| 6 | ✓ | Deep | NEU chatbot, EdTech | UI screens; district policy examples |
| 7 | ✓ | Deep | McTighe & Silver, Mollick, Horvath | AI-detection current evidence |
| 8 | ✓ | Deep | Mollick, McTighe & Silver, Horvath | Disclosure policy longitudinal data |
| 9 | ✓ | Deep | NEU chatbot, Mollick | Deep Research mode current behavior |
| 10 | ✓ | Deep | McTighe & Silver, NEU chatbot, Mollick | Learning Guide configuration walkthrough |
| 11 | ✓ | Deep | Horvath, EdTech, NEU chatbot | International privacy frameworks |
| 12 | ✓ | Moderate | EdTech, Mollick | ChatGPT Edu / Copilot Edu current features |
| 13 | ✓ | Moderate | NEU chatbot, Mollick, Horvath | Example briefs from real institutions |
| 14 | ✓ | Deep | Horvath, Mollick, NEU chatbot | Mohamed 2025 full citation; EPR 2025 full citation |

---

*This index was generated by the Research Gatherer pass on 2026-05-18. Update when new material is added.*
