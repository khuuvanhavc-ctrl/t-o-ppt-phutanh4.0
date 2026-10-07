# Input JSON schema (informal)

Top-level fields:
- `title` (string, required): presentation title
- `subtitle` (string, optional)
- `subject` (string, optional)
- `grade` (string, optional)
- `source_note` (string, optional)
- `slides` (array, required): slide objects

Each slide:
- `title` (string, required)
- `layout` (string, optional): `bullets`, `two_column`, `timeline`, or `closing`
- `bullets` (array of strings, optional)
- `left_title`, `left_bullets`, `right_title`, `right_bullets` (optional for `two_column`)
- `note` (string, optional): source/teacher note displayed in small text
- `accent` (hex string, optional): e.g. `#2F6690`

Keep bullets concise. For a real lesson, supply verified content and source notes. The generator does not fact-check input.
