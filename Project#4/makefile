filename=proj4

$(filename).pdf: $(filename).ps
	ps2pdf $^

$(filename).ps: $(filename).dvi
	dvips -t a4paper $^

$(filename).dvi: $(filename).tex
	latex $^
	make bibtex
	latex $^
	latex $^

bibtex: $(filename).bib
	bibtex $(filename)

pdflatex: $(filename).tex
	pdflatex $^
	make bibtex
	pdflatex $^
	pdflatex $^

clean:
	rm -f $(filename).ps $(filename).log $(filename).aux $(filename).out $(filename).dvi $(filename).bbl $(filename).blg