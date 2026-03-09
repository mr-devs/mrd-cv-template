# CV Bibliography Conventions — ref.bib

File: `/Users/mdeverna/Documents/Projects/cv/ref.bib`

---

## Keyword → CV Section Map

| Entry type | `keywords` | CV Section | Label prefix |
|------------|------------|------------|--------------|
| `@article` | `J` | Journal Articles | J |
| `@inproceedings` | `C` | Peer-reviewed Conference Proceedings | C |
| `@misc` | `R` | Manuscripts under review | R |
| `@misc` | `W` | Manuscripts in Preparation | W |
| `@misc` | `O` | Other Writings | O |
| `@misc` | `I` | Invited Talks | I |
| `@misc` | `T` | Talks | T |
| `@misc` | `P` | Posters | P |
| `@misc` | `D` | Demonstrations & Tutorials | D |

---

## Author Formatting

- **Always bold DeVerna**: `\textbf{DeVerna, Matthew R.}` (Last, First M. format)
- **All authors**: `Last, First M.` format, separated by ` and `
- **Equal contribution**: place `$^\diamond$` *immediately after the last name*, before the comma:
  ```
  Ghosh$^\diamond$, Shalmoli and \textbf{DeVerna, Matthew R.}$^\diamond$ and Menczer, Filippo
  ```
  No space between the name and `$^\diamond$`.

---

## Title Formatting

Use double braces to preserve capitalization:
```
title = {{Title With Preserved Caps.}},
```
Titles end with a period inside the inner braces.

---

## Publication Entry Types

### @article (keyword J)
```bibtex
@article{LastnameYEARShortTitle,
    title   = {{Title.}},
    author  = {\textbf{DeVerna, Matthew R.} and Coauthor, First M.},
    journal = {Journal Name},
    volume  = {1},
    number  = {2},
    pages   = {1--10},
    year    = {2024},
    url     = {https://doi.org/...},
    keywords= {J}
}
```
Optional `addendum` for footnotes under entry:
```
addendum = {\\ -- Note text, e.g. award or citation}
```

### @inproceedings (keyword C)
```bibtex
@inproceedings{LastnameYEARShortTitle,
    author    = {\textbf{DeVerna, Matthew R.} and Coauthor, First M.},
    title     = {{Title.}},
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
    title        = {{Title.}},
    author       = {\textbf{DeVerna, Matthew R.} and Coauthor, First M.},
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
    title        = {{Title.}},
    author       = {\textbf{DeVerna, Matthew R.} and Coauthor, First M.},
    howpublished = {arXiv[Preprint]},
    year         = {2024},
    url          = {https://doi.org/...},
    keywords     = {W}
}
```

### @misc — Other Writings (keyword O)
```bibtex
@misc{LastnameYEARShortTitle,
    author       = {Matthew R. DeVerna},
    title        = {Title.},
    howpublished = {PhD dissertation, Indiana University},
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
  howpublished = {\ul{Venue Name} (City, State; presented by Francesco Pierri)},
  ```

### howpublished format for informal venues (D entries)
Informal demos may omit `\ul{}`:
```
howpublished = {Invited to the Learning Informatics Lab, University of Minnesota (Virtual)},
```

### month field
Always include `month` for presentations. Use three-letter abbreviation: `jan`, `feb`, `mar`, `apr`, `may`, `jun`, `jul`, `aug`, `sep`, `oct`, `nov`, `dec`.

### Invited Talk (keyword I)
```bibtex
@misc{VenueYEAR,
    title        = {{Title.}},
    author       = {\textbf{DeVerna, Matthew R.} and Coauthor, First M.},
    howpublished = {\ul{Seminar/Lab/Event Name} (City, State, Country)},
    month        = apr,
    year         = {2024},
    keywords     = {I}
}
```

### Talk (keyword T)
```bibtex
@misc{VenueShortYEAR,
    title        = {{Title.}},
    author       = {\textbf{DeVerna, Matthew R.} and Coauthor, First M.},
    howpublished = {\ul{Conference Name} (City, State, Country)},
    month        = jul,
    year         = {2024},
    keywords     = {T}
}
```

### Poster (keyword P)
```bibtex
@misc{VenueShortYEAR,
    title        = {{Title.}},
    author       = {\textbf{DeVerna, Matthew R.} and Coauthor, First M.},
    howpublished = {\ul{Conference Name} (City, State, Country)},
    month        = jul,
    year         = {2024},
    keywords     = {P}
}
```

### Demo/Tutorial (keyword D)
```bibtex
@misc{ToolNameN,
    author       = {\textbf{DeVerna, Matthew R.}},
    title        = {Tool Name: Subtitle.},
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
% Other Writings (Popular media, blogs, ...)
% Invited Talks
% Talks
% Posters
% Demonstrations and Tutorials
```
Add new entries within the appropriate section block.

---

## Cite Key Conventions

Pattern: `LastnameYEARShortTitle` — e.g., `DeVerna2024AIFactChecking`, `covaxxy_deverna_2021`
For presentations: `VenueAbbrevYEAR` — e.g., `CINDTalk26`, `ModelingMisinfoic2s2-24`
