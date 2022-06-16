DOCNAME=main

all: document

document:
	pdflatex $(DOCNAME).tex -shell-escape
	biber $(DOCNAME)
	pdflatex $(DOCNAME)-frn.tex -shell-escape
	pdflatex $(DOCNAME).tex -shell-escape