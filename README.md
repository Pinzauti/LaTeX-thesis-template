# LaTeX Thesis Template
Clean LaTeX template for thesis or large writeups.

## Get started
In order to compile the project you have to:
- Navigate to the ```src``` folder.
- Compile the file ```main.tex```.
- Compile the file ```main-frn.tex```.
- Compile (yes, again) the file ```main.tex```.

If you use pdflatex this translates to:
```
cd src/
pdflatex main.tex
pdflatex main-frn.tex
pdflatex main.tex
```

## File structure
    .
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
    │   ├── FrontBack   
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

- classicthesis
- frontespizio
- biblatex
- graphicx
- amsmath
- amssymb
- amsthm
- mathtools
