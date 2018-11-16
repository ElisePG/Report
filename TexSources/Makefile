MAINDOC = maindoc
LATEX   = pdflatex
BIBTEX  = bibtex
DVIPS   = dvips
PSPDF   = ps2pdf13 -sPAPERSIZE=a4 -dPDFSETTINGS=/prepress


.PHONY:		clean
.PHONY:		okular

all:		$(MAINDOC).ps

$(MAINDOC).ps :	$(MAINDOC).tex
		$(LATEX) $(MAINDOC)	
		- $(BIBTEX) $(MAINDOC)
		$(LATEX) $(MAINDOC)
		$(LATEX) $(MAINDOC)
#		$(DVIPS) $(MAINDOC).dvi -o $(MAINDOC).ps
#		$(PSPDF) $(MAINDOC).ps		

clean:
	rm -f *~ *.aux *.log *.dvi *.bak *.ps *.out *.backup *.zip *.bbl *.blg *.toc *.new *.ind *.idx *.ilg *.bcf *.lof *.lot *.xml *.not
	rm -f */*~ */*.aux */*.log */*.dvi */*.bak */*.ps */*.out */*.backup */*.zip */*.bbl */*.blg */*.toc */*.new */*.bcf */*.lof */*.lot */*.xml */*.not


okular:
	okular $(MAINDOC).pdf &

