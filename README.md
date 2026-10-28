# mrd-cv-template

## What is this?

This is the CV template that I use.
I've converted it into a template hoping that it might be helpful for others.

The idea was to make it as easy as possible to manage and update on a regular basis.
I think the template makes this super easy on its own, but the inclusion of Claude Code [skills](https://agentskills.io) makes it even easier (included in the `.claude/` directory).

### Example

See [**cv-example.pdf**](cv-example.pdf) for a rendered PDF of this template, filled with placeholder content that exercises every feature listed below.

### Key Features

- Designed to be easy to update and maintain overtime, with academics in mind
- Uses very minimal fancy LaTeX functions to maximize long-term durability
- Modularizes sections so they are easy to update and organize
- Easy to customize with different fonts, link colors, etc.
  - If you don't know where to start, links to different LaTeX fonts and colors are included within the document
- Manage and format your publications with BibLaTex
  - Clean, scannable entries: title (linked to its DOI or URL, with a small link icon), authors, then venue and year, plus optional bullet notes for awards and the like
  - Presentations list just the title, venue, and year (the author list is hidden, on the assumption that you gave them; one line in `main.tex` to change)
  - Includes reverse numbering for bibliography sections, with `\cite` kept in sync with the reversed labels (see the Publications and Selected Media Coverage sections of [cv-example.pdf](cv-example.pdf))
  - Sorts entries by date, so same-year entries appear in the right order (give them a `month`; only the year is printed)
  - Separate sections for manuscripts under review, in preparation, journal articles, conference proceedings, other writings, invited talks, talks, posters, and demos
- Leverages PDF Bookmarks providing full control over the side-bar sections within the document for easy PDF navigation
- Includes Claude Code commands for automatically updating different sections of the document

### Getting Started

1. Customize your personal information in the \mytitle
2. Add your content to the respective section files (e.g., education.tex, exp_research.tex).
3. Update the ref.bib file with your publications and categorize them using keywords.
4. If you use the Claude Code skills, replace the placeholder name in `.claude/reference/cv-bib-conventions.md` with your own so new entries bold the right author.

> **Note**: Detailed instructions for each section are included within each file to guide you through the customization process.

### Found this useful?

If you use this template I would appreciate it if you let me know.
You can contact me directly ([matthewdeverna.com](https://matthewdeverna.com)) or create an issue in this repository.
Thanks!!

#### Folks who have used this template

- [Bao Tran Truong](https://btrantruong.github.io/)
- [Rachith Aiyappa](https://rachithaiyappa.github.io/)
- [Daniel Kaiser](https://kaiser-dan.github.io/)
- [Kevin W. Jin](https://kevinwjin.com/)
- [Larry Zhang](https://www.larryzhang.io/)
- [Do Won Kim](https://do-won.github.io/)
- [Hannah Rose Kirk](https://www.hannahrosekirk.com/)

## Overleaf/LaTeX CV template

There is an [**OLD** template on Overleaf](https://www.overleaf.com/latex/templates/clean-academic-cv-template/tjpjkzmvztwn) that can be directly imported into Overleaf.
This is old because Overleaf no longer supports templates for CVs ([source](https://docs.overleaf.com/templates/submitting-to-the-overleaf-template-gallery#Other_ways_to_share_templates,_examples_and_completed_works)).
