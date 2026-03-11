# REPO_CONTEXT.md - AI Schema for This Repository

## Overview

This is a personal tech learning journal stored in a GitHub Pages site.

## Core Rules

1. **REPO_CONTEXT.md = Pure Schema Only** - This file contains ONLY rules/structure, no actual learning content
2. **Content goes in dedicated folders** - Knowledge base files belong in `knowledge/` folder
3. **Daily entries link to knowledge** - Daily learning files should reference detailed notes in knowledge folder
4. **Always get user permission before pushing to GitHub**
5. **Save Google AI Studio links** - Whenever user pastes a Google AI Studio link, ALWAYS add it to the notes (Resources section). These links contain their thinking/learning roadmap, evaluations, and research.
6. **UPDATE README files** - Always update `daily-learnings/README.md` when adding new daily entries
7. **USE knowledge/ folder for long-term notes** - Don't forget it exists! Use `knowledge/[topic]/` for stackable, reusable content that will be referenced across multiple entries

## Repository Structure

```
notes/
├── REPO_CONTEXT.md           # THIS FILE - Schema/Rules ONLY
├── knowledge/                # Detailed knowledge base (stackable notes)
│   └── [topic]/
│       ├── README.md          # Index for this topic
│       └── *.md               # Detailed notes
└── daily-learnings/          # Daily learning records
    ├── README.md             # Index
    └── YYYY/
        ├── YYYY.md           # Yearly summary
        └── MM/
            └── YYYY-MM-DD.md # Daily entry
```

## File Naming

| Type | Format | Example |
|------|--------|---------|
| Daily Entry | `YYYY-MM-DD.md` | `2026-03-08.md` |
| Yearly Summary | `YYYY.md` | `2026.md` |
| Knowledge Topic | lowercase-with-dashes | `ai-agents`, `context-engineering` |

## Content Guidelines

### Daily Entry (in `daily-learnings/YYYY/MM/`)
```markdown
# YYYY-MM-DD

## What I Learned
- Brief summary

## Notes
- Key points
- Reference to knowledge folder: [[knowledge/topic/concept]]

## Tags
#tag1 #tag2

## Resources
- [Link](url)
```

### Knowledge Note (in `knowledge/[topic]/`)
```markdown
# Concept Name

## Definition
...

## Key Points
- Point 1
- Point 2

## Examples
...

## Related Daily Entries
- [YYYY-MM-DD](../daily-learnings/2026/03/2026-03-08.md)
```

## Adding New Content

1. **Daily learning**: Create in `daily-learnings/YYYY/MM/YYYY-MM-DD.md`
2. **New knowledge topic**: Create folder in `knowledge/[topic]/`
3. **Update summaries**: Link new content in `YYYY.md` yearly summary
4. **Update README**: Add new entry to `daily-learnings/README.md` index
5. **Ask permission before GitHub push**

---

*Last updated: 2026-03-11*
