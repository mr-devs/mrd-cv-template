---
name: cv-add-publication
description: Use when adding a publication (journal article, conference paper, preprint, manuscript under review, dissertation, blog post) to the LaTeX CV bibliography (template/ref.bib)
---

# Adding a Publication to ref.bib

**Reference file:** Read `.claude/reference/cv-bib-conventions.md` for full templates and formatting rules.

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
- [ ] CV owner's name bolded (see the reference file): `\textbf{First M. Last}`
- [ ] Equal contribution authors marked: `Author$^{\dagger}$, First` (no space before `$`)
- [ ] Title in double braces, no trailing period: `title = {{Title Text}}`
      (the title prints on its own line in the CV, so a period in the data shows up as a stray period)
- [ ] `url` set to `https://doi.org/...` when a DOI exists (it becomes the link on the title)
- [ ] Journal articles include `month` (sorts same-year articles; never printed)
- [ ] Entry placed in the correct comment-delimited section of `ref.bib`
- [ ] Cite key follows `LastnameYEARShortTitle` pattern

## Common Mistakes

| Mistake | Fix |
|---------|-----|
| Using `@article` for preprints/under review | Use `@misc` with keyword `R` or `W` |
| Forgetting `\textbf{}` on the CV owner | Always bold the owner's name |
| Space before `$^{\dagger}$` | Must be `Name$^{\dagger}$,` with no space |
| Single braces on title | Use `{{Title}}` to preserve capitalization |
| Wrong section placement | Each keyword has its own comment block in ref.bib |
