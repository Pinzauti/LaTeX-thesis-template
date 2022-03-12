# LaTeX Thesis Template
LaTeX template for thesis or large writeups.

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
    ├── src                   
    │   ├── Chapters   
    |       ├── AppendixA
    |           ├── index.tex
    |           └── ...
    |       ├── Chapter1
    |           ├── index.tex
    |           └── ...
    |       └── Chapter2
    |           ├── index.tex
    |           └── ...
    │   ├── FrontBack   
    |       ├── Abstract.tex
    |       ├── Bibliography.tex
    |       ├── Conclusion.tex
    |       ├── Frontespizio.tex
    |       ├── Quote.tex
    |       └── Titleback.tex
    │   |── Bibliography.bib
    |   |── config.tex
    |   └── main.tex
    |── README.md
    └── .gitignore
