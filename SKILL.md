---
name: eduppt-creator
description: Create editable PowerPoint lessons for Vietnamese lower-secondary History and Geography. Use when turning lesson requests, textbooks, PDFs, Word documents, or notes into structured classroom presentations, with factual checks, visual design, and PPTX export.
license: MIT
metadata:
  version: "1.0.0"
  language: vi
---

# EduPPT Creator

## Mission
Create accurate, pedagogically useful, visually clear, editable `.pptx` presentations for Vietnamese THCS History and Geography, especially under the 2018 General Education Curriculum.

## Workflow
1. **Clarify only essentials.** Determine topic, grade, textbook series/source, purpose, duration or slide count, and any required visual style. If enough information is already supplied, proceed using sensible defaults: Vietnamese, 16:9, modern academic style.
2. **Read source material first.** Use available file-reading/OCR tools for supplied PDFs, DOCX, images, and notes. Treat the user's source as the primary scope when asked. Never pretend to have read pages or images that were inaccessible.
3. **Build a lesson map.** Define learning outcomes, key concepts, slide sequence, student tasks, and assessment. Keep alignment with the specified grade, textbook series, and curriculum. Do not mix textbook series without stating it.
4. **Check facts.** Verify dates, names, places, historical cause/effect, geographic locations, units, and data. Prefer primary/official/academic sources. Mark unresolved claims for review; never invent citations, page numbers, statistics, or URLs.
5. **Design slides.** Give each slide one main purpose. Use concise readable text, meaningful visuals, diagrams, maps, timelines, tables, or charts. Avoid text walls and decorative visuals that obscure learning.
6. **Build the editable PPTX.** Use the bundled `scripts/create_ppt.py` for structured JSON input, or another compatible presentation tool. Prefer native PowerPoint text and shapes for editability. Use a 16:9 canvas by default.
7. **Quality assurance.** Check slide count, text overflow where feasible, missing titles, broken image paths, citations, and output-file existence. If a renderer is available, export previews and visually inspect every slide. Never claim visual inspection unless performed.
8. **Deliver.** Provide the actual `.pptx` file link and briefly state any known limitations. Include PDF only if requested and a PDF renderer is available.

## THCS History guidance
- Distinguish facts, interpretations, and later historical evaluations.
- Check chronology, periodization, actors, locations, causes, developments, and consequences.
- Use timelines, event maps, source excerpts, comparison tables, and evidence-based questions where appropriate.
- Avoid anachronism and unsupported claims about motives.
- Identify illustrative/AI-generated imagery as illustration, not documentary evidence.

## THCS Geography guidance
- Check location, direction, scale, legend, units, dates, and geographic terminology.
- Distinguish observed data from interpretation and forecast.
- Use maps, cross-sections, climate graphs, diagrams, and data charts when they help answer the learning question.
- Do not invent map boundaries or statistics. Cite the data year and source.

## Pedagogy defaults
Where appropriate, organize the lesson into:
- Opening / activation of prior knowledge
- Exploration and formation of knowledge
- Practice / consolidation
- Application / connection to real life
- Assessment / exit ticket

These are adaptable stages, not mandatory headings for every presentation. Write student-facing prompts clearly. Add teacher notes only when requested or useful.

## Visual defaults
- 16:9 widescreen.
- Vietnamese Unicode fonts such as Aptos, Arial, or Calibri; use an installed font where possible.
- Consistent title, body, and accent styles.
- Prefer short bullets, generous whitespace, high contrast, and meaningful visual hierarchy.
- Keep source notes readable and close to the relevant claim/image.
- Use editable text and shapes whenever possible.

## Source and copyright rules
- Prioritize user-provided sources and cite external factual claims.
- Never fabricate references or imply that an unverified source was checked.
- Do not reproduce long copyrighted passages from textbooks. Summarize in original wording and use only brief excerpts when justified.
- Use images only when permitted or appropriately licensed; record attribution where required.

## Bundled generator
Input JSON schema and examples are in `references/input-schema.md` and `examples/lesson.json`.
Run:
`python scripts/create_ppt.py examples/lesson.json --output output/lesson.pptx`

The generator creates a basic editable deck from structured slide content. It does not itself research facts, parse PDFs, generate images, or visually render slides. Those tasks require separate tools or an AI agent workflow.

## Completion checklist
- [ ] Correct grade, subject, source, and requested scope
- [ ] Learning goals and slide sequence fit the lesson
- [ ] Dates, names, places, units, and claims checked where possible
- [ ] No invented references or data
- [ ] Text readable and layout consistent
- [ ] PPTX exists and opens
- [ ] Visual rendering inspected if renderer was available
- [ ] Limitations disclosed honestly
