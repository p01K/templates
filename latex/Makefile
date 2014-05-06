LATEX = pdflatex
TARGET = paper
OPEN = open
BIBTEX = bibtex -min-crossrefs=99

TEXFILES = report.tex

FIGS = 

.SUFFIXES:
.SUFFIXES: .eps .pdf .png .dia

.dia.png:
        dia -e $@ $< --size=1024

all: ${TEXFILES} reliability.bib ${FIGS}
        $(MAKE) -C figs
        $(LATEX) $(TARGET)
        $(BIBTEX) $(TARGET)
        $(LATEX) $(TARGET)
        $(LATEX) $(TARGET)


clean:
        $(MAKE) -C figs clean
        rm -f *.out *.aux *.log *.bbl *.blg ${FIGS} $(TARGET).pdf
