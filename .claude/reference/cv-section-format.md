# CV Section File Conventions

All section files live in `template/` (relative to the repository root).

---

## Longtable Format

Every section uses a 2-column `longtable`:

```latex
\begin{longtable}[l]{@{}p{.1\textwidth} p{\dimexpr.9\textwidth-2\tabcolsep\relax}@{}}

    YEAR & Description text \\

\end{longtable}
```

- Left column (`.1\textwidth`): date
- Right column (`\dimexpr.9\textwidth-2\tabcolsep\relax`): description; the `\dimexpr` and trailing `@{}` keep the table inside the right margin
- No `\hline`, no column separators

---

## Date Conventions

| Pattern | Meaning | Example |
|---------|---------|---------|
| `YYYY` | Single year / one-time event | `2023` |
| `YYYY--YY` | Range, ended | `2020--25` |
| `YYYY--` | Ongoing | `2024--` |

---

## Section File → Which File to Edit

| CV Section | File |
|------------|------|
| Appointments | `appointments.tex` |
| Education | `education.tex` |
| Research Experience | `exp_research.tex` |
| Awards & Honors | `awards.tex` |
| Tools & Software | `tools.tex` |
| Selected Media Coverage | `media.tex` |
| Teaching | `teaching.tex` |
| Academic Advising | `advising.tex` |
| Academic Service | `service.tex` |
| Professional Memberships | `memberships.tex` |
| Other Experience | `exp_other.tex` |

Publications and Presentations are managed through `ref.bib`, not section files.

---

## service.tex — Subsections

Add to the correct subsection, creating it (same longtable pattern) if the file doesn't have it yet:

| Subsection | When to use |
|------------|-------------|
| **Guest Editor** | Edited a special issue of a journal |
| **Conference Organizer** | Chair, co-chair, web chair of a full conference |
| **Summer School Organizer** | Organized/co-led a summer school (e.g., SICSS) |
| **Speaker Series Organizer** | Coordinated a seminar/speaker series |
| **Workshop Organizer** | Organized a workshop at a conference |
| **Journal Reviewer** | Peer review for a journal |
| **Conference Reviewer** | Peer review / program committee for a conference |
| **Invited Speaker** | Panelist, podcast, outreach talk (not a research presentation) |
| **Other Service** | Departmental roles, student rep, anything else |

Entry format (all subsections are the same longtable pattern):
```latex
    YEAR & Description of role, Venue/Organization \\
```

---

## teaching.tex — One Subsection per Institution

```
\subsection*{University Name}
```

Pick the institution where the teaching occurred, adding a new subsection if needed.

Entry format:
```latex
    YEAR & Role, Course Name, Level (e.g., Graduate (PhD) or Undergraduate) \\
```

---

## awards.tex

Single longtable (no subsections). Entries may include:

- Dollar amounts: escape the dollar sign — `\$5,000`
- Role clarification: `(Role: PI)` or `(Role: Co-PI)` in parentheses
- Citations to related publications: `\cite{citekey}`
- URLs: `\href{https://...}{Link text}`

Example entries:
```latex
    2024 & Fancy NSF Grant (\$1,000,000; Role: PI) \\
    2023 & Best Paper Award, Super Cool Conference~\cite{Conf3} \\
```

---

## Common Formatting Patterns

Links:
```latex
\href{https://url.com}{Link Text}
```

Footnote-size text (used in some sections):
```latex
\footnotesize Text here \normalsize
```

Entries are generally in **reverse-chronological order** within each subsection (most recent first).
