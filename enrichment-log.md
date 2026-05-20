# Enrichment Log — NotebookLM for Education: A Practitioner's Guide

*Generated 2026-05-18.*

Per-chapter record of work performed by the Tables / Figures / Wayback enrichment pass.

---

## Per-chapter detail

- `00-frontmatter.md` — 0 tables rendered, 0 figures generated, Wayback Machine: (no section)
- `00-introduction.md` — 0 tables rendered, 0 figures generated, Wayback Machine: (no section)
- `01-the-bounded-tool.md` — 3 tables rendered, 2 figures generated, Wayback Machine: (no section)
- `02-your-first-notebook.md` — 3 tables rendered, 1 figure generated, Wayback Machine: (no section)
- `03-output-type-is-a-pedagogical-choice.md` — 2 tables rendered, 1 figure generated, Wayback Machine: (no section)
- `04-the-k12-teacher.md` — 3 tables rendered, 2 figures generated, Wayback Machine: (no section)
- `05-the-k12-student.md` — 2 tables rendered, 0 figures generated, Wayback Machine: (no section)
- `06-google-classroom-integration.md` — 3 tables rendered, 1 figure generated, Wayback Machine: (no section)
- `07-assessment-redesign.md` — 3 tables rendered, 1 figure generated, Wayback Machine: (no section)
- `08-academic-integrity.md` — 2 tables rendered, 0 figures generated, Wayback Machine: (no section)
- `09-higher-ed-research-and-synthesis.md` — 2 tables rendered, 1 figure generated, Wayback Machine: (no section)
- `10-higher-ed-course-design-and-self-testing.md` — 2 tables rendered, 0 figures generated, Wayback Machine: (no section)
- `11-privacy-equity-and-the-access-gap.md` — 3 tables rendered, 0 figures generated, Wayback Machine: (no section)
- `12-choosing-the-right-tool.md` — 2 tables rendered, 2 figures generated, Wayback Machine: (no section)
- `13-the-administrator-brief.md` — 2 tables rendered, 1 figure generated, Wayback Machine: (no section)
- `14-honest-capability-assessment.md` — 2 tables rendered, 0 figures generated, Wayback Machine: (no section)
- `97-fundamental-themes.md` — 0 tables rendered, 0 figures generated, Wayback Machine: (no section) — appendix
- `99-back-matter.md` — 0 tables rendered, 0 figures generated, Wayback Machine: (no section)

---

## Summary

```
Total chapters processed: 18 chapter files (12 content chapters with markup, 6 front/back/appendix files)
Total tables rendered: 34
Total figures generated (SVG+PNG pairs): 12
Total Wayback Machine subjects replaced: 0 (no Wayback Machine sections exist in this book)
```

---

## What was done

**Pass 1 — Tables.** All 34 `<!-- → [TABLE: …] -->` comments across chapters 01–14 rendered to populated GitHub-flavored markdown tables. Every cell carries real content inferred from the comment description and the chapter context; no placeholder strings.

**Pass 2 — Figures.** All 12 `<!-- → [DIAGRAM|IMAGE: …] -->` comments rendered to editorial monochrome SVG figures (700×420 to 700×480 viewBox), rasterized to 2× PNGs via `cairosvg`, and saved to `images/`. Each comment replaced in chapter prose with `![alt-text](../images/filename.png)` + `*Figure N.N — title*`.

**Pass 3 — AI Wayback Machine.** Skipped — this book does not use the Wayback Machine pattern. No `## AI Wayback Machine` section exists in any chapter. The pass's validation/replacement and portrait-stub work has nothing to apply to.

**Pass 4 — Log.** This file.

---

## Style conformance check

All 12 figures conform to the editorial style guide:

- ✓ viewBox 700×420 (or 700×480 / 700×360 where content required taller / shorter canvas)
- ✓ Monochrome warm grayscale only — `--ink #1a1714`, `--gray-dark #4a4540`, `--gray-mid #8a8480`, `--gray-light #c8c4c0`, `--cream #f5f2ee`, `--white #fdfcfb`
- ✓ Georgia serif throughout; no sans-serif
- ✓ Box fills `--cream` with `--ink` 1px borders; arrows 1.5px `--ink` with arrowhead marker; dashed scaffold 0.75px `--gray-light` 4-3 stroke pattern
- ✓ 32px margins; flat fills; no rounded corners; no shadows; no gradients
- ✓ All `&` characters in text content properly escaped to `&amp;`
- ✓ PNG rasters at 2× SVG dimensions

---

## File index

**SVG/PNG pairs in `images/`:**

| File | Chapter | Figure | Title |
|---|---|---|---|
| `01-the-bounded-tool-fig-01` | Ch 1 | 1.1 | Open-loop chatbot vs. source-grounded tool |
| `01-the-bounded-tool-fig-02` | Ch 1 | 1.2 | The RAG pipeline, three steps |
| `02-your-first-notebook-fig-01` | Ch 2 | 2.1 | The Sources panel: listing is not ingestion |
| `03-output-type-is-a-pedagogical-choice-fig-01` | Ch 3 | 3.1 | The Note-to-Source loop |
| `04-the-k12-teacher-fig-01` | Ch 4 | 4.1 | Where the bottleneck moves |
| `04-the-k12-teacher-fig-02` | Ch 4 | 4.2 | The Note-to-Source feedback loop |
| `06-google-classroom-integration-fig-01` | Ch 6 | 6.1 | The admin email that resolves in one round |
| `07-assessment-redesign-fig-01` | Ch 7 | 7.1 | Same data. Two interpretations. |
| `09-higher-ed-research-and-synthesis-fig-01` | Ch 9 | 9.1 | The Note-to-Source research workflow |
| `12-choosing-the-right-tool-fig-01` | Ch 12 | 12.1 | Bounded vs. open-loop architecture |
| `12-choosing-the-right-tool-fig-02` | Ch 12 | 12.2 | The four-question framework |
| `13-the-administrator-brief-fig-01` | Ch 13 | 13.1 | The one-page brief, six sections |

---

## Outstanding work (none introduced by this pass)

This pass touched only the TABLE and FIGURE comments. It did not modify chapter prose, headings, exercises, or any other content. The two `[verify]` flags previously noted in chapter content (Mohamed 2025 citation; Cassidy 2003 *New Yorker* article date) remain present in chapters 14 and 7 respectively — they were not affected by this pass.
