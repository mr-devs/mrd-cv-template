---
name: cv-add-publication
description: Use when adding a publication (journal article, conference paper, preprint, manuscript under review, dissertation, blog post) to Matthew DeVerna's LaTeX CV bibliography at /Users/mdeverna/Documents/Projects/cv/ref.bib
---

# Adding a Publication to ref.bib

**Reference file:** Read `~/.claude/reference/cv-bib-conventions.md` for full templates and formatting rules.

## Quick Decision: Entry Type + Keyword

```
Journal article?          → @article,       keywords={J}
Conference proceedings?   → @inproceedings, keywords={C}
Under review / R&R?       → @misc,          keywords={R}
In preparation / preprint?→ @misc,          keywords={W}
Dissertation, blog, other?→ @misc,          keywords={O}
```

## Checklist Before Writing the Entry

- [ ] Correct entry type and keyword (see above)
- [ ] DeVerna's name bolded: `\textbf{DeVerna, Matthew R.}`
- [ ] Equal contribution authors marked: `Author$^\diamond$, First` (no space before `$`)
- [ ] Title in double braces: `title = {{Title Text.}}`
- [ ] Entry placed in the correct comment-delimited section of `ref.bib`
- [ ] Cite key follows `LastnameYEARShortTitle` pattern

## Common Mistakes

| Mistake | Fix |
|---------|-----|
| Using `@article` for preprints/under review | Use `@misc` with keyword `R` or `W` |
| Forgetting `\textbf{}` on DeVerna | Always bold his name |
| Space before `$^\diamond$` | Must be `Name$^\diamond$,` with no space |
| Single braces on title | Use `{{Title}}` to preserve capitalization |
| Wrong section placement | Each keyword has its own comment block in ref.bib |
