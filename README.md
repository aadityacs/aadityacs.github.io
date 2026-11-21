# aadityacs.github.io

Personal academic website of Aaditya Chandrasekhar, built on the
[al-folio](https://github.com/alshedivat/al-folio) template.

This page is the editing guide. Everything you will ever need to change is a
plain-text file listed in the table below. You never need to touch HTML.

---

## How editing works

1. Open the file on github.com and click the pencil icon. For a full editor with
   all files side by side, press the `.` key on the repository page.
2. Make the change and click "Commit changes".
3. The site rebuilds by itself. It is live in about 3 to 5 minutes.
4. To watch the rebuild, open the "Actions" tab. A green tick means it worked.
   A red cross usually means a typo (see "If something breaks" at the bottom).

---

## Which file to open

| I want to change | Open this file |
| --- | --- |
| My bio text | `_pages/about.md` (bottom half) |
| The line under my name, my address | `_pages/about.md` (top half) |
| My photo | replace `assets/img/prof_pic.jpg` (keep the name) |
| Add or edit a paper | `_bibliography/papers.bib` |
| Which papers appear on the home page | `_bibliography/papers.bib` (`selected = {true}`) |
| A paper's picture or GIF | `assets/img/publication_preview/` plus `preview = {...}` in the paper |
| Add or edit a patent | `_bibliography/patents.bib` |
| Add a news item | new file in `_news/` |
| My CV | replace `assets/pdf/CV_Aaditya_Chandrasekhar.pdf` (keep the name) |
| Email, Scholar, GitHub, LinkedIn | `_data/socials.yml` |
| Colour or link of a venue badge (SMO, CAD, ...) | `_data/venues.yml` |
| Which coauthor names become links | `_data/coauthors.yml` |

Everything else (`_config.yml`, `.github/`, `Gemfile`, `assets/` apart from the
files above) runs the site. Leave it alone unless you want to change how the
site works.

---

## Copy-paste templates

### A new paper

Paste at the top of `_bibliography/papers.bib`. Delete the lines you do not need.
The quickest start is the BibTeX from Google Scholar ("Cite", then "BibTeX") or
from the journal page, with the extra lines added.

```bibtex
@article{chandrasekhar2027example,
  abbr        = {SMO},
  bibtex_show = {true},
  title       = {Title of the Paper},
  author      = {Chandrasekhar, Aaditya and Coauthor, First and Chen, Wei},
  journal     = {Structural and Multidisciplinary Optimization},
  volume      = {70},
  number      = {1},
  pages       = {12},
  year        = {2027},
  doi         = {10.1007/xxxxx},
  arxiv       = {2701.01234},
  code        = {https://github.com/UW-ERSL/Example},
  preview     = {example.gif},
  selected    = {true}
}
```

For a preprint, use `journal = {arXiv preprint arXiv:2701.01234}` and leave out
`doi`, `volume`, `number` and `pages`.

### A paper picture or GIF

1. Upload the file to `assets/img/publication_preview/`, for example `example.gif`.
2. Add `preview = {example.gif},` to the paper in `_bibliography/papers.bib`.

### A news item

Create a new file in `_news/`, for example `_news/2027-01-15-new-paper.md`, with

```markdown
---
date: 2027-01-15
inline: true
---

Our paper on [TOBACO](https://doi.org/10.1007/s00158-026-04273-2) is out in SMO.
```

The first time you add one, also set `enabled: true` under `announcements`
in `_pages/about.md` so the news section appears on the home page.

### A patent

Paste at the top of `_bibliography/patents.bib`.

```bibtex
@misc{chandrasekhar2027patent,
  abbr            = {GoogleX},
  title           = {Title of the Patent},
  author          = {Chandrasekhar, Aaditya and Williamson, Ian},
  year            = {2027},
  additional_info = {U.S. Patent Application [US 2027/0123456 A1](https://patents.google.com/patent/US20270123456A1/en)}
}
```

### A new venue badge

Add to `_data/venues.yml`, then use the same short name as `abbr` in the paper.

```yaml
"CMAME":
  url: https://www.sciencedirect.com/journal/computer-methods-in-applied-mechanics-and-engineering
  color: "#1565c0"
```

---

## If something breaks

The Actions tab shows a red cross and the site keeps showing the last version
that worked, so nothing goes offline. Usual causes are

- a missing `}` or `,` in a `.bib` entry,
- two papers with the same key (the word after `@article{`),
- wrong indentation in a `.yml` file (use spaces, never tabs).

Undo the last change, or fix the typo and commit again.

---

## One-time setup on GitHub

1. Settings, then Pages. Set "Deploy from a branch" to `gh-pages`, folder `/ (root)`.
2. Settings, then Actions, then General. Set "Workflow permissions" to
   "Read and write permissions".
