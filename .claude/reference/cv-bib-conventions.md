# CV Bibliography Conventions — ref.bib

File: `template/ref.bib` (relative to the repository root)

> **Make this yours:** replace the placeholder name `Smith, John R.` throughout this file with your own name, in `Last, First M.` format, so new entries bold the right author.

---

## How Entries Render

`template/main.tex` (the "Bibliography entry layout" block) prints every entry as:

```
Title [link icon]  (linked to the entry's url)
Authors            (omitted for presentations: keywords I, T, P, D)
Venue, Year
Note               (only if the entry has a note)
-- addendum bullets
```

Volume, number, pages and month are kept in the data but never printed.

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
Leave the trailing period **off**: the title prints on its own line, so a period in
the data shows up as a stray period. Titles that end in `?` or `!` keep that mark.

---

## Shared Field Rules

- **`url`**: use `https://doi.org/...` whenever a DOI exists. The URL itself is never printed; it becomes the link on the entry's title
- **Venue names**: don't include the year (e.g. a booktitle ending in "2026"); the CV already prints `year` after the venue

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
Always include `month` on articles: it orders same-year articles correctly. It is
never printed.

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
    howpublished = {Revise and Resubmit at \textit{Venue Name}},
    year         = {2024},
    url          = {https://doi.org/...},
    keywords     = {R}
}
```
Use `Under review at \textit{Venue Name}` if not yet R&R. Use venue name only (not "Proceedings of...") if accepted to venue.

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
- `\ul{}` marks the venue name (rendered as italics in the CV)
- For events hosted at an institution, use `Event @ Institution` inside `\ul{}`, e.g. `\ul{Cool Lab @ Your University} (Virtual)`. Informal demos (D entries) use the same pattern
- Virtual events: `(Virtual)` instead of city/state/country
- Presentations (I, T, P, D) print no author line, since the CV owner is assumed to be the presenter. Don't add a "presented by" note; still fill in `author`

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
