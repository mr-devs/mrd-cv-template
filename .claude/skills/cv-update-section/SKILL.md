---
name: cv-update-section
description: Use when adding or editing entries in Matthew DeVerna's LaTeX CV section files (education, awards, teaching, service, advising, memberships, media, tools, other experience)
---

# Updating a CV Section File

**Reference file:** Read `~/.claude/reference/cv-section-format.md` for the full longtable format, date conventions, and subsection routing.

## Quick Decision: Which File?

```
Awards, fellowships, honors?  → awards.tex
Teaching roles?               → teaching.tex
Academic service?             → service.tex
Education?                    → education.tex
Research positions?           → exp_research.tex
Media coverage?               → media.tex
Software/tools?               → tools.tex
Advising?                     → advising.tex
Memberships?                  → memberships.tex
Other work experience?        → exp_other.tex
```

Publications and presentations → use `cv-add-publication` or `cv-add-presentation` instead.

## service.tex Subsection Routing

| Role | Subsection |
|------|------------|
| Special issue editor | Guest Editor |
| Conference chair/co-chair/web chair | Conference Organizer |
| Summer school lead/co-lead | Summer School Organizer |
| Speaker series coordinator | Speaker Series Organizer |
| Workshop organizer at a conference | Workshop Organizer |
| Peer review for a journal | Journal Reviewer |
| Peer review / program committee for a conference | Conference Reviewer |
| Panelist, podcast, outreach talk | Invited Speaker |
| Departmental roles, student rep | Other Service |

## teaching.tex Subsection Routing

- Stanford → `\subsection*{Stanford University}`
- Indiana University → `\subsection*{Indiana University Bloomington}`

## Checklist Before Writing the Entry

- [ ] Correct file and subsection identified
- [ ] Date format matches convention: `YYYY`, `YYYY--YY`, or `YYYY--`
- [ ] Dollar amounts escaped: `\$5,000`
- [ ] URLs wrapped: `\href{https://...}{Link Text}`
- [ ] Citations use `\cite{citekey}` with `~` before: `~\cite{key}`
- [ ] Entry ends with `\\`
- [ ] Entries in reverse-chronological order within subsection

## Common Mistakes

| Mistake | Fix |
|---------|-----|
| Unescaped `$` in dollar amounts | Use `\$` |
| Wrong subsection in service.tex | See routing table above |
| Missing `\\` at end of row | Every longtable row needs `\\` |
| Bare URL instead of `\href` | Wrap all links in `\href{url}{text}` |
