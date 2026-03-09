---
name: cv-add-presentation
description: Use when adding a talk, poster, invited talk, or demonstration to Matthew DeVerna's LaTeX CV bibliography at /Users/mdeverna/Documents/Projects/cv/ref.bib
---

# Adding a Presentation to ref.bib

**Reference file:** Read `~/.claude/reference/cv-bib-conventions.md` for full templates and formatting rules.

All presentations use `@misc`. The `keywords` field determines which subsection they appear in.

## Quick Decision: Keyword

```
Invited seminar, lab talk, or keynote?  → keywords={I}   (Invited Talks)
Conference talk (submitted/accepted)?   → keywords={T}   (Talks)
Conference poster?                      → keywords={P}   (Posters)
Demo, tutorial, tool walkthrough?       → keywords={D}   (Demonstrations & Tutorials)
```

## howpublished Format

**Standard (in-person):**
```
howpublished = {\ul{Venue Name} (City, State, Country)},
```

**Virtual:**
```
howpublished = {\ul{Venue Name} (Virtual)},
```

**Presented by someone else:**
```
howpublished = {\ul{Venue Name} (City, State; presented by First Last)},
```

**Informal demo (no \ul{}):**
```
howpublished = {Invited to the Lab Name, University (Virtual)},
```

## Checklist Before Writing the Entry

- [ ] Entry type is `@misc`
- [ ] Correct keyword: `I`, `T`, `P`, or `D`
- [ ] `\ul{}` wraps venue name (for formal venues)
- [ ] Location in parentheses after venue
- [ ] `(Virtual)` used for remote presentations
- [ ] `; presented by First Last` appended if DeVerna didn't present
- [ ] `month` field included (three-letter abbreviation: `jan`, `feb`, etc.)
- [ ] DeVerna's name bolded: `\textbf{DeVerna, Matthew R.}`
- [ ] Title in double braces: `title = {{Title.}}`

## Common Mistakes

| Mistake | Fix |
|---------|-----|
| Using `@inproceedings` for a talk | All presentations use `@misc` |
| Missing `\ul{}` around venue | Wrap formal venue names in `\ul{Venue}` |
| Forgetting `month` | Required for all presentation entries |
| Omitting presenter note | Add `; presented by Name` inside location parens |
