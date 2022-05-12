filename=proj5

$(filename).pdf: $(filename).ps
	ps2pdf $^

$(filename).ps: $(filename).dvi
	dvips $^

$(filename).dvi: $(filename).tex
	latex $^
	latex $^

pdflatex: $(filename).tex
	pdflatex $^
	pdflatex $^

clean:
	rm -f $(filename).ps $(filename).snm $(filename).toc $(filename).nav $(filename).vrb $(filename).log $(filename).aux $(filename).out $(filename).dvi $(filename).bbl $(filename).blg
