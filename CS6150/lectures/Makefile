TEXINPUTS:=.

LEC= \
	pdf/2022-08-23.pdf \
	pdf/2022-08-25.pdf

.PHONY: all copy
all: %(LEC)

pdf/%.pdf: tex/%.tex
	pdflatex -output-dir pdf $<
	pdflatex -output-dir pdf $<

clean:
	rm -f pdf/*.aux pdf/*.log pdf/*.out
	rm -f pdf/*.nav pdf/*.snm pdf/*.toc
	rm -f pdf/*.vrb

distclean: clean
	rm -f pdf/*.pdf
