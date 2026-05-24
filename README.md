# NotebookLM for Education: A Practitioner's Guide

**Author:** Humanitarians AI
**Publisher:** Bear Brown, LLC
**Series:** Practitioner Guides for the AI Classroom
**Status:** First-edition draft, May 2026
**License:** All rights reserved (see `LICENSE.md`)

---

## What this book is

A practitioner's handbook for K–12 teachers, higher-education instructors, and instructional designers who have heard about NotebookLM, opened it once, and cannot yet tell whether it is meaningfully different from the AI tools they already know. The book teaches the vocabulary, the workflows, and the frameworks for deploying NotebookLM as the bounded, source-grounded learning tool it actually is — rather than as a faster ChatGPT.

The central argument: NotebookLM's distinctive educational value is not that it is a powerful AI assistant but that it is a *bounded* one. Its restriction to user-uploaded sources creates a citation-grounded, privacy-respecting learning environment that general chatbots cannot replicate. Educators who treat it as a faster ChatGPT will miss what it offers; educators who design around its constraint will find it the most defensible AI tool currently available for classroom use.

Each of the fourteen chapters teaches an operational decision — what to upload, which output to generate, how to redesign an assessment, how to write the administrator brief, how to assess the evidence honestly — at the level a working teacher can actually apply on Monday morning. The book closes (Chapter 14) by handing the reader an honest capability assessment they can write for their own context, grounded in a four-bucket evidence framework that keeps overclaiming honest.

The book is companion-published with the **Medhavy** ([medhavy.com](https://www.medhavy.com/)) AI-native adaptive tutoring platform — the Kindle and online editions integrate with Medhavy's chapter-aware tutoring.

---

## Table of contents

### Front matter
- `00-frontmatter.md` — Title page, copyright, dedication, preface
- `00-introduction.md` — Introduction (Chapter 0): the bounded-tool argument; the phase gate; how to read

### Act One — Orient (the design principle)
- `01-the-bounded-tool.md` — Ch 1: *NotebookLM is not a faster ChatGPT. Its restriction to your sources is the feature.*
- `02-your-first-notebook.md` — Ch 2: *Upload three source types, generate three output types, and evaluate each against the source before you trust any of them.*
- `03-output-type-is-a-pedagogical-choice.md` — Ch 3: *Audio Overview is not the default. Every output type encodes an assumption about how learning happens.*

### Act Two — Build (role-specific workflows)
- `04-the-k12-teacher.md` — Ch 4: *Teachers use NotebookLM to turn approved materials into differentiated student resources — not to outsource the curriculum, but to multiply it.*
- `05-the-k12-student.md` — Ch 5: *The question is not whether students will use NotebookLM. It is whether you design the activity so that using it well requires engaging with the material.*
- `06-google-classroom-integration.md` — Ch 6: *The Classroom integration is where the pedagogy and the admin meet. Both have to work.*
- `07-assessment-redesign.md` — Ch 7: *Any assessment a student can complete by generating a NotebookLM output and submitting it is an assessment you need to redesign.*
- `08-academic-integrity.md` — Ch 8: *An AI use policy that says "don't" without saying "because" will not survive the first conversation with a student who asks why.*
- `09-higher-ed-research-and-synthesis.md` — Ch 9: *For graduate students and faculty, NotebookLM is most valuable when the reading load is high, the sources are curated, and the goal is synthesis across sources.*
- `10-higher-ed-course-design-and-self-testing.md` — Ch 10: *The Monash model — configure NotebookLM to quiz the learner, not explain to them — is the highest-leverage use case for undergraduate course integration.*
- `11-privacy-equity-and-the-access-gap.md` — Ch 11: *Free does not mean equitably available. The institutional account, the admin toggle, and the district policy all stand between the tool and the student.*

### Act Three — Sustain (institutional + evaluative)
- `12-choosing-the-right-tool.md` — Ch 12: *The right tool is the one whose design constraint matches your learning goal.*
- `13-the-administrator-brief.md` — Ch 13: *Administrators will ask three questions. This chapter gives you the answers.*
- `14-honest-capability-assessment.md` — Ch 14: *NotebookLM is not a learning revolution. It is a useful bounded tool with a thin evidence base, strong adoption evidence, and real deployment risks. This chapter gives you the language to say that clearly.* (The book's terminal deliverable.)

### Appendix
- `97-fundamental-themes.md` — Appendix A: *The Fundamental Themes — Frictional · Phase Gates · Humans + AI.* The theoretical bridge to the broader **Frictional / Irreducibly Human / Brutalist / Boondoggling** series this book belongs to. Optional reading.

### Back matter
- `99-back-matter.md` — Acknowledgments, About the Author, Notes, References, Why no Index (Medhavy integration), Glossary, Errata

---

## Repository structure

```
.
├── README.md                  ← this file
├── LICENSE.md                 ← copyright and licensing terms
├── book.md                    ← book description and high-level outline (planning)
├── TIKTOC.md                  ← Tic TOC: the full 14-chapter spec
├── outline.md                 ← chapter-level table of contents (planning)
├── vision.md                  ← Tic TOC Phase 1: vision and positioning
├── architecture.md            ← Tic TOC Phase 2: learning architecture
├── chapters-spec.md           ← Tic TOC Phase 3: chapter specifications
├── risks.md                   ← Tic TOC Phase 4: scope, market, risks
├── metadata.yaml              ← EPUB metadata
├── build.sh                   ← build script (pandoc → EPUB)
├── graphs.sh                  ← figure-comment processor
├── chapters/                  ← the book's actual content (see TOC above)
├── pantry/                    ← research notes and library files
│   ├── README.md              ← pantry index
│   ├── notebooklm_education_research.md
│   ├── 01-the-bounded-tool_notes.md  ... (one per chapter)
│   └── _lib_*.md              ← copied from the shared MD library
├── images/                    ← figure files
├── styles/                    ← Kindle CSS
└── logs/
    └── log.csv                ← per-run drafting log
```

The four Tic TOC planning files are templated. The current source-of-truth for the book's structure is `TIKTOC.md`.

---

## Build

```bash
./build.sh
```

Output goes to `output/notebook-lm-for-education-a-practitioners-guide.epub` (gitignored).

## Figures

```bash
./graphs.sh
```

Processes `<!-- → [TYPE: description] -->` comments in chapter files:

- Tabular figures → classed markdown tables (`.infographic-table`, `.comparison-table`, `.data-table`)
- Non-tabular figures → placeholder images in `images/`, ready to replace
- CSS log appended to `styles/kindle-book.css` on each run

Review `chapters/*-updated.md`, then promote:

```bash
for f in chapters/*-updated.md; do mv "$f" "${f/-updated/}"; done
```

## Publish

Upload `output/notebook-lm-for-education-a-practitioners-guide.epub` to [KDP](https://kdp.amazon.com). For the Medhavy-integrated online edition, see [medhavy.com](https://www.medhavy.com/) onboarding documentation.

---

## Copyright

Copyright © 2026 Nik Bear Brown. All rights reserved.

Published by Bear Brown, LLC.

No part of this publication may be reproduced, distributed, or transmitted in any form or by any means without the prior written permission of the publisher, except in the case of brief quotations in critical reviews and certain other noncommercial uses permitted by copyright law.

See `LICENSE.md` for full terms.

For permissions, errata, and corrections: bear@bearbrown.co.

---

*Practitioner Guides for the AI Classroom* — a series of short, opinionated handbooks for educators deploying AI tools in real classrooms. The series argues for deliberate design over enthusiasm, honest evidence framing over marketing, and the labor separation between what AI does well and what only a human can do.

---

## Who This Book Is For

This is a book for practicing educators. It is for the K–12 teacher who heard about NotebookLM in a professional-development workshop, opened it once, and could not tell whether the Audio Overview she generated was good enough to assign. It is for the community-college instructor whose department head asked her to "explore AI tools" with no further specification. It is for the graduate-program faculty member who has 40 papers to read this week and has wondered, more than once, whether NotebookLM could help with that. It is not for AI researchers, edtech-industry analysts, or instructional-design specialists already deep in the field. It is for the person who has slides to make for Tuesday, students to teach on Wednesday, and 30 minutes on Monday night to figure out whether this tool is worth the effort.

---

## How to Read It

Fourteen chapters in three acts.

**Act One — Orient (Chapters 1–3): the design principle.** Chapter 1 names NotebookLM as a bounded tool and argues that the boundary is the feature. Chapter 2 walks you through your first notebook in thirty minutes, with the verification step intact. Chapter 3 reframes output-type selection as a pedagogical decision rather than a feature exploration.

**Act Two — Build (Chapters 4–11): role-specific workflows.** Chapters 4 and 5 cover the K–12 teacher and K–12 student perspectives. Chapter 6 addresses the Google Classroom integration and the admin landscape. Chapter 7 takes on the hardest question: redesigning assessments for an AI-augmented environment. Chapter 8 covers academic integrity policy. Chapters 9 and 10 cover higher-education research workflows and undergraduate course design. Chapter 11 addresses privacy and equity — the structural deployment constraints.

**Act Three — Sustain (Chapters 12–14): institutional and evaluative work.** Chapter 12 places NotebookLM in the broader AI-tool landscape and teaches a selection framework. Chapter 13 walks you through writing a one-page administrator brief. Chapter 14 is the book's terminal deliverable: the honest capability assessment you write for your own context, using a four-bucket evidence framework to keep your claims defensible.

The Appendix follows. It is optional. The book works without it.

---

## Signature Simulations

<!-- TODO: populate from chapter content -->

---

## About the Author

**Nik Bear Brown** is an Associate Teaching Professor in the College of Engineering at Northeastern University, where he teaches AI, data science, programming, and the design of AI-assisted education infrastructure. He founded *Humanitarians AI* (a 501(c)(3) supporting graduate students building consequential AI projects) and *Bear Brown & Company*, which publishes the *Practitioner Guides for the AI Classroom* series this book belongs to. His current work centers on the *Irreducibly Human* framework — a curriculum project on the cognitive capacities the AI era most urgently requires humans to develop — and on *Medhavy*, an AI-native adaptive tutoring platform that this book is designed to integrate with.

He holds a PhD in Computer Science from UCLA (computational and systems biology, AI, statistics), an MS in Information Design and Data Visualization from Northeastern, an MBA from Northeastern, and a BA in Biochemistry and Molecular Biology from UC Santa Cruz. He did a part-time postdoc in deep learning at Harvard Medical School while teaching at Northeastern. Earlier in his career he worked as a molecular biologist at DNAX Research Institute and Cetus Corporation.

He writes at [nikbearbrown.com](https://www.nikbearbrown.com), at [irreducibly.xyz](https://irreducibly.xyz), and at [skepticism.ai](https://www.skepticism.ai). He works in Boston.

The connective thread across his work is simple: AI is powerful, but power without judgment is just a microscope sitting in a box. This book is one attempt to put the right humans in the room with the microscope, looking at the right thing, asking the right questions.

