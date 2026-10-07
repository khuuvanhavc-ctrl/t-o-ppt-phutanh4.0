# EduPPT Creator (THCS History & Geography)

Portable Agent Skill package for creating editable Vietnamese lower-secondary History/Geography PowerPoint decks.

## Contents
- `SKILL.md` — skill instructions and workflow
- `scripts/create_ppt.py` — creates an editable `.pptx` from JSON
- `examples/lesson.json` — small demonstration input
- `references/input-schema.md` — JSON format reference
- `requirements.txt` — Python dependency

## Requirements
- Python 3.10+
- `python-pptx`

Install:
```bash
python -m pip install -r requirements.txt
```

Create a deck:
```bash
python scripts/create_ppt.py examples/lesson.json --output output/lesson.pptx
```

The generated presentation uses editable PowerPoint text boxes and shapes. This starter package does not automatically read PDFs/DOCX, browse the web, generate images, or render slides for visual QA. Connect those capabilities through the AI agent/runtime you use.

## Portable skill format
The package follows the common Agent Skills directory pattern: a `SKILL.md` file with YAML frontmatter, plus optional scripts, examples, and references. Compatibility depends on the host agent's support for this format.
