[![.github/workflows/latex.yml](https://github.com/Pinzauti/LaTeX-thesis-template/actions/workflows/latex.yml/badge.svg)](https://github.com/Pinzauti/LaTeX-thesis-template/actions/workflows/latex.yml)
![MIT](https://img.shields.io/badge/license-MIT-brightgreen) 
[![Latest release](https://badgen.net/github/release/Pinzauti/LaTeX-thesis-template)](https://github.com/Pinzauti/LaTeX-thesis-template/releases/tag/v1.1)
# LaTeX Thesis Template
Clean LaTeX template for a thesis or a large writeup. You can see [here](https://github.com/Pinzauti/LaTeX-thesis-template/releases/download/v1.1/template.pdf) the generated PDF.

## Requirements
You need a working LaTeX enviroment installed in your system.
#### Minted
If you want to add source code to your document and therefore use the [minted package](https://ctan.org/pkg/minted?lang=en), you need to make sure to have [Python](https://www.python.org/) and the [pygments package](https://pygments.org/) installed in your system. You can take a look at the [documentation](http://tug.ctan.org/macros/latex/contrib/minted/minted.pdf) to have a better insight.

Note that this setup is default but not mandatory for the template, if you don't need to write code in your document just remove the minted package from the ```config.tex``` file (and of course the example code in the first chapter).

## Getting started

In order to compile the template you just need to navigate to the ```src``` folder and execute the command:

```
latexmk
```

### Editors
If you use [Overleaf](https://www.overleaf.com/project), [Visual Studio Code](https://code.visualstudio.com/) or any other editor just compile everything as usual.

## File structure
    .
    ├── .github                               
    |   ├── workflows
    |       ├── latex.yml               # Action to compile and upload the PDF document to the workflow tab  
    ├── src                             # Where the actual template is               
    │   ├── Chapters                    # Chapters of the document
    |       ├── AppendixA               
    |           ├── Index.tex           # Entrypoint of Appendix A, here you should link your sections
    |           ├── Section1.tex        # First section of the appendix
    |           └── ...
    |       ├── Chapter1
    |           ├── Index.tex           # Entrypoint of Chapter 1, here you should link your sections
    |           ├── Section1.tex        # First section of the chapter
    |           └── ...
    |       └── ...
    │   ├── FrontBack                   # Material of the frontpage or the backpage
    |       ├── Abstract.tex            # Abstract of the document
    |       ├── Bibliography.tex        # Add the bibliography to the document, customizable
    |       ├── Conclusions.tex         # Conclusions of the document
    |       ├── Frontespizio.tex        # Frontpage of the document
    |       ├── Quote.tex               # An initial quote 
    |       └── Titleback.tex           # Page behind the frontpage
    |   ├── Images                      # Where images are located
    |       └── logo.png                # Logo in the frontpage, replace with your logo
    │   |── Bibliography.bib            # Bibliography entries
    |   |── config.tex                  # Configuration (e.g. packages, theorems etc.)
    |   |── main.tex                    # Main file, it is what you have to compile
    |   └── .latexmkrc                  # Contains the commands to compile the document
    |── .gitignore
    |── CITATION.cff
    |── LICENSE
    └── README.md
 
## Configuration file
It is the file [config.tex](https://github.com/Pinzauti/LaTeX-thesis-template/blob/main/src/config.tex). It contains some pre-included packages and defines the ```\abs``` command for the absolute value. It also defines the ambients ```Postulate```, ```Definition``` and ```Theorem```. More info [here](http://www.ams.org/arc/tex/amscls/amsthdoc.pdf).

### Included packages

- [classicthesis](https://ctan.org/pkg/classicthesis): main package used for the thesis style.
- [frontespizio](https://ctan.org/pkg/frontespizio): generates the first page of the document.
- [biblatex](https://ctan.org/pkg/biblatex): bibliography.
- [graphicx](https://ctan.org/pkg/graphicx): handles images.
- [fontenc](https://ctan.org/pkg/fontenc): handles fonts.
- [mathtools](https://ctan.org/pkg/mathtools): provides many useful tools for mathematical typesetting.
- [amssymb](https://ctan.org/pkg/amsfonts): provides some mathematical symbols.
- [amsthm](https://ctan.org/pkg/amsthm): handles theorems setup.
- [minted](https://ctan.org/pkg/minted): to add source code in a nice way.
- [epigraph](https://ctan.org/pkg/epigraph): to add quotes.

## Included Github action

Used in order to compile the document and to upload it to the [workflow tab](https://github.com/Pinzauti/LaTeX-thesis-template/actions/workflows/latex.yml). More info [here](https://github.com/xu-cheng/latex-action/).
