LATEX = pdflatex
TARGET = paper
OPEN = open
BIBTEX = bibtex -min-crossrefs=99

TEXFILES = report.tex

FIGS = 

.SUFFIXES:
.SUFFIXES: .eps .pdf .png .dia

all: ${TEXFILES}  
	$(LATEX) $(TARGET)


clean:
	rm -f *.out *.aux *.log *.bbl *.blg 
