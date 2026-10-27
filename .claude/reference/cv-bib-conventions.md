# CV Bibliography Conventions — ref.bib

File: `template/ref.bib` (relative to the repository root)

> **Make this yours:** replace the placeholder name `Smith, John R.` throughout this file with your own name, in `Last, First M.` format, so new entries bold the right author.

---

## Keyword → CV Section Map

| Entry type | `keywords` | CV Section | Label prefix |
|------------|------------|------------|--------------|
| `@article` | `J` | Journal Articles | J |
| `@inproceedings` | `C` | Peer-reviewed Conference Proceedings | C |
| `@misc` | `R` | Manuscripts Under Review | R |
| `@misc` | `W` | Manuscripts in Preparation | W |
| `@misc` | `O` | Other Writings | O |
| `@misc` | `I` | Invited Talks | I |
| `@misc` | `T` | Talks | T |
| `@misc` | `P` | Posters | P |
| `@misc` | `D` | Demonstrations & Tutorials | D |

---

## Author Formatting

- **Always bold the CV owner**: `\textbf{Smith, John R.}` (Last, First M. format)
- **All authors**: `Last, First M.` format, separated by ` and `
- **Equal contribution**: place `$^{\dagger}$` *immediately after the last name*, before the comma
  (the marker is explained under the Publications heading in `main.tex`):
  ```
  Doe$^{\dagger}$, Jane and \textbf{Smith$^{\dagger}$, John R.} and Roe, Richard
  ```
  No space between the name and `$^{\dagger}$`.

---

## Title Formatting

Use double braces to preserve capitalization:
```
title = {{Title With Preserved Caps}},
```
Leave the trailing period **off**. `main.tex` adds title punctuation for misc entries
(via `\DeclareFieldFormat`) and the bibliography style handles the rest; a period in
the data doubles up or breaks `... in Proceedings ...`. Titles that end in `?` or `!`
keep that mark.

---

## Publication Entry Types

### @article (keyword J)
```bibtex
@article{LastnameYEARShortTitle,
    title   = {{Title}},
    author  = {\textbf{Smith, John R.} and Coauthor, First M.},
    journal = {Journal Name},
    volume  = {1},
    number  = {2},
    pages   = {1--10},
    month   = mar,
    year    = {2024},
    url     = {https://doi.org/...},
    keywords= {J}
}
```
Always include `month` on articles: it orders same-year articles correctly, and
`main.tex` hides it at print time so only the year is shown.

Optional `addendum` for footnotes under entry:
```
addendum = {\\ -- Note text, e.g. award or citation}
```

### @inproceedings (keyword C)
```bibtex
@inproceedings{LastnameYEARShortTitle,
    author    = {\textbf{Smith, John R.} and Coauthor, First M.},
    title     = {{Title}},
    booktitle = {Proceedings of the Conference Name},
    volume    = {15},
    pages     = {1--10},
    number    = {1},
    year      = {2021},
    url       = {https://doi.org/...},
    keywords  = {C}
}
```

### @misc — Under Review (keyword R)
```bibtex
@misc{LastnameYEARShortTitle,
    title        = {{Title}},
    author       = {\textbf{Smith, John R.} and Coauthor, First M.},
    howpublished = {Revise and Resubmit in [Venue Name]},
    year         = {2024},
    url          = {https://doi.org/...},
    keywords     = {R}
}
```
Use `Under review at [Venue]` if not yet R&R. Use venue name only (not "Proceedings of...") if accepted to venue.

### @misc — In Preparation (keyword W)
```bibtex
@misc{LastnameYEARShortTitle,
    title        = {{Title}},
    author       = {\textbf{Smith, John R.} and Coauthor, First M.},
    howpublished = {arXiv[Preprint]},
    year         = {2024},
    url          = {https://doi.org/...},
    keywords     = {W}
}
```

### @misc — Other Writings (keyword O)
```bibtex
@misc{LastnameYEARShortTitle,
    author       = {\textbf{Smith, John R.}},
    title        = {{Title}},
    howpublished = {PhD dissertation, Your University},
    month        = jun,
    year         = {2025},
    keywords     = {O}
}
```

---

## Presentation Entry Types (all @misc)

### howpublished format for formal venues
```
howpublished = {\ul{Venue Name} (City, State, Country)},
```
- `\ul{}` underlines the venue name
- Virtual events: `(Virtual)` instead of city/state/country
- Presented by someone else: append `; presented by [Name]` inside the parens:
  ```
  howpublished = {\ul{Venue Name} (City, State; presented by First Last)},
  ```

### howpublished format for informal venues (D entries)
Informal demos may omit `\ul{}`:
```
howpublished = {Invited to the Cool Lab, Your University (Virtual)},
```

### month field
Always include `month` for presentations. Use three-letter abbreviation: `jan`, `feb`, `mar`, `apr`, `may`, `jun`, `jul`, `aug`, `sep`, `oct`, `nov`, `dec`.

### Invited Talk (keyword I)
```bibtex
@misc{VenueYEAR,
    title        = {{Title}},
    author       = {\textbf{Smith, John R.} and Coauthor, First M.},
    howpublished = {\ul{Seminar/Lab/Event Name} (City, State, Country)},
    month        = apr,
    year         = {2024},
    keywords     = {I}
}
```

### Talk (keyword T)
```bibtex
@misc{VenueShortYEAR,
    title        = {{Title}},
    author       = {\textbf{Smith, John R.} and Coauthor, First M.},
    howpublished = {\ul{Conference Name} (City, State, Country)},
    month        = jul,
    year         = {2024},
    keywords     = {T}
}
```

### Poster (keyword P)
```bibtex
@misc{VenueShortYEAR,
    title        = {{Title}},
    author       = {\textbf{Smith, John R.} and Coauthor, First M.},
    howpublished = {\ul{Conference Name} (City, State, Country)},
    month        = jul,
    year         = {2024},
    keywords     = {P}
}
```

### Demo/Tutorial (keyword D)
```bibtex
@misc{ToolNameN,
    author       = {\textbf{Smith, John R.}},
    title        = {{Tool Name: Subtitle}},
    howpublished = {\ul{Conference Name} (City, State, Country)},
    month        = jun,
    year         = {2021},
    keywords     = {D}
}
```

---

## File Organization

Entries are grouped by comment headers in this order:
```
% Journals
% Conferences
% Manuscripts under review
% Manuscripts in preparation
% Other Writings (Dissertations, popular media, blogs, ...)
% Invited Talks
% Talks
% Posters
% Demonstrations and Tutorials
```
Add new entries within the appropriate section block.

---

## Cite Key Conventions

Pattern: `LastnameYEARShortTitle` — e.g., `Smith2024CoolResult`
For presentations: `VenueAbbrevYEAR` — e.g., `ICWSMTalk24`, `CoolSciSeminar23`
