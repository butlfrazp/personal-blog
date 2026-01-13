# Technical Blog

A personal technical blog covering software engineering, systems design, and emerging technologies.

## 📁 Structure

```
blogs/
├── drafts/           # Work-in-progress posts
├── published/        # Live, published posts
├── archived/         # Older posts no longer actively promoted
├── templates/        # Post templates
└── assets/
    └── images/       # Images and diagrams for posts
```

## 📝 Post States

| State | Location | Description |
|-------|----------|-------------|
| **Draft** | `drafts/` | Posts in progress, not ready for publication |
| **Published** | `published/` | Live posts, ready for readers |
| **Archived** | `archived/` | Older posts, kept for reference |

## 🚀 Workflow

1. **Create**: Start a new post using a template from `templates/`
2. **Write**: Develop your post in `drafts/`
3. **Review**: Update frontmatter, proofread, add images
4. **Publish**: Move completed post to `published/` and update the `status` and `published_date`
5. **Archive**: Move older posts to `archived/` when no longer current

## 📋 Frontmatter Schema

Every post should include YAML frontmatter:

```yaml
---
title: "Your Post Title"
slug: your-post-title
author: Your Name
status: draft | published | archived
created_date: YYYY-MM-DD
published_date: YYYY-MM-DD
last_updated: YYYY-MM-DD
tags:
  - tag1
  - tag2
categories:
  - category1
summary: "A brief 1-2 sentence summary of the post"
---
```

## 🏷️ Tags & Categories

### Categories (broad topics)
- `software-engineering`
- `systems-design`
- `ai-ml`
- `devops`
- `programming-languages`
- `tools-productivity`
- `architecture`
- `security`

### Tags (specific topics)
Use lowercase, hyphenated tags like: `python`, `kubernetes`, `distributed-systems`, `agentic-ai`, `llm`, `testing`, `ci-cd`, etc.

## ✍️ Writing Guidelines

1. **Be technical but accessible** - Explain concepts, don't assume knowledge
2. **Include code examples** - Use fenced code blocks with language identifiers
3. **Add diagrams** - Store in `assets/images/` and reference with relative paths
4. **Link sources** - Credit and link to references
5. **Keep it focused** - One main topic per post

## 📖 File Naming Convention

Use lowercase, hyphenated names with the date prefix for published posts:

- Drafts: `topic-name.md`
- Published: `YYYY-MM-DD-topic-name.md`

## 🔧 Local Preview

You can preview Markdown posts using:
- VS Code Markdown Preview (`Cmd+Shift+V`)
- Any static site generator (Hugo, Jekyll, Astro, etc.)
