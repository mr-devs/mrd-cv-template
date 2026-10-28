---
name: cv-add-presentation
description: Use when adding a talk, poster, invited talk, or demonstration to the LaTeX CV bibliography (template/ref.bib)
---

# Adding a Presentation to ref.bib

**Reference file:** Read `.claude/reference/cv-bib-conventions.md` for full templates and formatting rules.

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

**Event hosted at an institution (including informal demos):**
```
howpublished = {\ul{Lab or Event Name @ the University} (Virtual)},
```

Keep the year out of the venue name: the CV prints it after the venue
(`Venue (City), 2024`). `\ul{}` renders as italics in the CV.

Presentations (`I`, `T`, `P`, `D`) print no author line, since the CV owner
is assumed to be the presenter, so don't add a presenter note. Still fill in
`author` with the full author list.

## Checklist Before Writing the Entry

- [ ] Entry type is `@misc`
- [ ] Correct keyword: `I`, `T`, `P`, or `D`
- [ ] `\ul{}` wraps venue name
- [ ] Location in parentheses after venue
- [ ] `(Virtual)` used for remote presentations
- [ ] `month` field included (three-letter abbreviation: `jan`, `feb`, etc.)
- [ ] CV owner's name bolded (see the reference file): `\textbf{First M. Last}`
- [ ] Title in double braces, no trailing period: `title = {{Title}}`
      (each field prints on its own line in the CV, so no punctuation is needed)

## Common Mistakes

| Mistake | Fix |
|---------|-----|
| Using `@inproceedings` for a talk | All presentations use `@misc` |
| Missing `\ul{}` around venue | Wrap formal venue names in `\ul{Venue}` |
| Forgetting `month` | Required for all presentation entries |
| Year in the venue name | Drop it; the CV prints `year` after the venue |
