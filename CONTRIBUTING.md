# Contributing to This Blog

Guidelines for writing and organizing posts.

## Creating a New Post

1. **Choose the right template** from `templates/`:
   - `post-template.md` - General technical posts
   - `tutorial-template.md` - Step-by-step guides
   - `deep-dive-template.md` - In-depth technical explorations

2. **Copy the template** to `drafts/`:
   ```bash
   cp templates/post-template.md drafts/my-new-post.md
   ```

3. **Fill in the frontmatter** - All fields are important for organization

4. **Write your content** - Follow the structure but adapt as needed

## Publishing a Post

1. **Complete the frontmatter**:
   - Set `status: published`
   - Add `published_date`
   - Update `last_updated`
   - Ensure all tags and categories are set

2. **Rename with date prefix**:
   ```bash
   mv drafts/my-post.md published/2026-01-13-my-post.md
   ```

3. **Final review**:
   - [ ] Spell check completed
   - [ ] Code examples tested
   - [ ] Links verified
   - [ ] Images properly referenced
   - [ ] Summary is compelling

## Style Guide

### Code Blocks

Always specify the language:

```python
def example():
    return "Hello, World!"
```

### Images

Store in `assets/images/` and reference with relative paths:

```markdown
![Alt text](../assets/images/diagram.png)
```

### Internal Links

Link to other posts using relative paths:

```markdown
See my post on [related topic](./2026-01-01-related-post.md)
```

### Formatting

- Use ATX-style headers (`#`, `##`, `###`)
- One sentence per line for easier diffs
- Use fenced code blocks (triple backticks)
- Prefer lists for multiple items
- Use tables for comparisons

## Checklist Before Publishing

- [ ] Title is clear and descriptive
- [ ] Summary captures the essence (for social sharing)
- [ ] Tags are relevant and consistent with existing tags
- [ ] Code is tested and works
- [ ] No sensitive information exposed
- [ ] Proper attribution for external content
