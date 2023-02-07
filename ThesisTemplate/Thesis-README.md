# uiucthesis class

A LaTeX package for formatting theses in the format required by the University of Illinois at Urbana-Champaign.

A class file and style file are provided. Both provide identical functionality except that the class file loads the "book" class with the [oneside] option.

## Files

- uiucthesis2021.dtx: Source for uiucthesis.cls, uiucthesis.sty and thesis-ex.tex
- uiucthesis2021.ins: Driver file for uiucthesis.dtx
- uiucthesis2021.pdf: Precompiled PDF file of documentation from .dtx file
- thesis.tex: Example main file
- uiucthesis2021.cls: Pregenerated class file
- uiucthesis2021.sty: Pregenerated style file (for backwards-compatibility)

## Installation

To (re)generate the `.ins`, `.cls`, and `.sty` file (and the documentation), simply compile `uiucthesis2021.dtx` like any other document.
E.g., using `latexmk`,

```bash
latexmk -pdf -synctex=1 uiucthesis2021.dtx
```

## Dependencies

This package uses the `setspace`, `geometry`, `babel`, `titletoc`, and `fancyhdr` packages.
`titlesec` is used for the example chapter heading format in `ruledchapters.sty`.

## Update Notes

- 3.1 (Zachary J Weiner)
  * Format table of contents entries with titletoc, prepend "Chapter" and "Appendix"
  * Place appendices after references, returning to `\mainmatter` so that appendices are still numbered
  * Add copyright and licensing information
- 3.0 (Zachary J Weiner)
  * Significant revision, obsolete options removed and source simplified
- 2.25b (Stephen Mayhew)
  * Removed the Vita Section
  * Added a Makefile
  * Changed all dates from 2009 -> 2014
  * Be careful when updating the date in the first line of uiucthesis2021.dtx! All numbers must be two digits, including month and day.
