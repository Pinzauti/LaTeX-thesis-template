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
    |       ├── Bibliography.tex        # Add the bilbiography to the document
    |       ├── Conclusions.tex         # Conclusions of the document
    |       ├── Frontespizio.tex        # Frontpage of the document
    |       ├── Quote.tex               # An initial quote 
    |       └── Titleback.tex           # Page behind the frontpage
    │   |── Bibliography.bib            # Bibliography entries.
    |   |── config.tex                  # Configuration (e.g. packages, theorems etc.)
    |   └── main.tex                    # Main file, it is what you have to compile
    |── README.md
    └── .gitignore
    
## Pre-included packages

- [classicthesis](https://ctan.org/pkg/classicthesis): Main package used for the thesis style.
- [frontespizio](https://ctan.org/pkg/frontespizio): Generates the first page of the document.
- [biblatex](https://ctan.org/pkg/biblatex): Bibliography
- [graphicx](https://ctan.org/pkg/graphicx): For handling images.
- amsmath
- amssymb
- amsthm
- mathtools

## Pre-included Github action

Used in order to compile the document and to upload it to the worflow tab. More info [here](https://github.com/xu-cheng/latex-action/).
