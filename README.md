# LaTeX guide for APA7 formatting with Göteborgs universitet (GU) style.

## workflow

document format is `.tex`, as usual. 

some preamble code

```
\documentclass[12pt,a4paper]{article}
\usepackage[T1]{fontenc}
\usepackage[swedish]{babel}
\usepackage[margin=1in]{geometry}
\usepackage{csquotes}
\usepackage{url}
\usepackage[style=apa, backend=biber, sortcites, url=true]{biblatex}
\addbibresource{uni.bib}
\usepackage{setspace}
```

`uni.bib` is the bibliography file, which resides in the current working directory.

when citing, use `\autocite`, `textcite`  or `nocite`.

compiling is as follows:

```
pdflatex test.tex && biber test.bcf && pdflatex text.tex
```
replace `test.tex` and `test.bcf` with your corresponding file names.



## dependencies (arch linux)
`texlive-bibtexextra`

`texlive-langeuropean`

`texlive-latex`

`texlive-latexextra`

`texlive-latexrecommended`

`biber`
