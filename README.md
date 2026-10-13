# Bounded Weighted Edit Distance with Integer Metric Costs

Manuscript by Jihan Wang, Department of Computer Science, The University of Illinois Urbana-Champaign.
Contact: [jihanw2@illinois.edu](mailto:jihanw2@illinois.edu).

This paper studies exact bounded weighted edit distance for integer metric costs and approximation for normalized real metric costs.

## Source files

- `main.tex`: the complete manuscript, including proofs, pseudocode, tables, and the TikZ figure.
- `ref.bib`: the bibliography. Citation keys are used in `main.tex`.
- `LICENSE`: the repository's MIT license.

The PDF and other build products are generated locally and are not tracked by Git.

## Build

Use TeX Live or MiKTeX with pdfLaTeX, BibTeX, `latexmk`, and the `alphaurl` bibliography style from `urlbst`. The manuscript's LaTeX packages are listed in the preamble of `main.tex`.

From the repository directory, run:

```sh
latexmk -pdf -interaction=nonstopmode -halt-on-error main.tex
```

The output is `main.pdf`. `latexmk` runs BibTeX and repeats LaTeX as needed to resolve citations and cross-references.

Without `latexmk`, run these commands in order:

```sh
pdflatex -interaction=nonstopmode -halt-on-error main.tex
bibtex main
pdflatex -interaction=nonstopmode -halt-on-error main.tex
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```

## Updating the manuscript

The repository uses branch `main`. Its `origin` is `https://github.com/Jihan-Wang/EXWED.git`.

After building and reviewing the changes, stage the source and supporting files:

```sh
git add main.tex ref.bib README.md .gitignore .gitattributes
git diff --cached --check
git diff --cached
git commit -m "Update weighted edit distance manuscript"
git push origin main
```

## Editing

Edit the manuscript in `main.tex` and references in `ref.bib`. Rebuild after changes and check the log for unresolved references or citations. `.gitignore` excludes generated files; `.gitattributes` normalizes source files to LF line endings.
