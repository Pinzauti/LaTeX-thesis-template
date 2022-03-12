[![.github/workflows/latex.yml](https://github.com/Pinzauti/LaTeX-thesis-template/actions/workflows/latex.yml/badge.svg)](https://github.com/Pinzauti/LaTeX-thesis-template/actions/workflows/latex.yml)
# LaTeX Thesis Template
Clean LaTeX template for thesis or large writeups.

## Get started
In order to compile the project you have to:
- Navigate to the ```src``` folder.
- Compile the file ```main.tex```.
- Compile the file ```main-frn.tex```.
- Compile (yes, again) the file ```main.tex```.

If you use pdflatex this is:
```
cd src/
pdflatex main.tex
pdflatex main-frn.tex
pdflatex main.tex
```

If you use [Overleaf](https://www.overleaf.com/project) just uncomment [these lines](https://github.com/Pinzauti/LaTeX-thesis-template/blob/main/src/FrontBack/Frontespizio.tex#L24) and just compile the file as usual.

## File structure
    .
    ├── .github                               
        ├── workflows
            ├── latex.yml               # Action to compile and upload the PDF document to the workflow tab.  
    ├── src                             # Where the actual template is               
    │   ├── Chapters                    # Chapters of the document
    |       ├── AppendixA               
    |           ├── index.tex           # Entrypoint of Appendix A, here you should link your sections
                ├── section1.tex        # First section of the appendix
    |           └── ...
    |       ├── Chapter1
    |           ├── index.tex           # Entrypoint of Chapter 1, here you should link your sections
                ├── section1.tex        # First section of the chapter
    |           └── ...
            └── ...
    │   ├── FrontBack                   # Material of the frontpage or the backpage
    |       ├── Abstract.tex            # Abstract of the document
    |       ├── Bibliography.tex        # You can change the bibliography style here
    |       ├── Conclusions.tex         # Conclusions of the document
    |       ├── Frontespizio.tex        # Frontpage of the document
    |       ├── Quote.tex               # An initial quote 
    |       └── Titleback.tex           # Page behind the frontpage
    │   |── Bibliography.bib            # Bibliography entries
    |   |── config.tex                  # Configuration (e.g. packages, theorems etc.)
    |   └── main.tex                    # Main file, it is what you have to compile
    |── README.md
    └── .gitignore
 
## Configuration file
It is the file [config.tex](https://github.com/Pinzauti/LaTeX-thesis-template/blob/main/src/config.tex). It contains some pre-included packages and defines the ```\abs``` command for the absolute value. It also defines the ambients ```Postulate```, ```Definition``` and ```Theorem```. More info [here](http://www.ams.org/arc/tex/amscls/amsthdoc.pdf).

### Pre-included packages

- [classicthesis](https://ctan.org/pkg/classicthesis): main package used for the thesis style.
- [frontespizio](https://ctan.org/pkg/frontespizio): generates the first page of the document.
- [biblatex](https://ctan.org/pkg/biblatex): bibliography.
- [graphicx](https://ctan.org/pkg/graphicx): for handling images.
- [mathtools](https://ctan.org/pkg/mathtools): provides many useful tools for mathematical typesetting.
- [amssymb](https://ctan.org/pkg/amsfonts?lang=en): provides some mathematical symbols.
- [amsthm](https://ctan.org/pkg/amsthm?lang=en): for theorems setup.
- [epigraph](https://ctan.org/pkg/epigraph?lang=en): for adding quotes at the beginning of the chapters.

## Pre-included Github action

Used in order to compile the document and to upload it to the worflow tab. More info [here](https://github.com/xu-cheng/latex-action/).
