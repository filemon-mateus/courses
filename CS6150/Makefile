TEXINPUTS:=.

HW= \
	pdf/hw1.pdf \
	pdf/hw2.pdf \
	pdf/hw3.pdf \
	pdf/hw4.pdf \
	pdf/hw5.pdf \
	pdf/hw6.pdf \

.PHONY: all copy
all: %(HW)

pdf/%.pdf: tex/%.tex
	latexmk -pvc -pdf -auxdir=tmp -output-directory=pdf -pdflatex="pdflatex" $<

clean:
	rm -f pdf/*.aux pdf/*.log pdf/*.out
	rm -f pdf/*.nav pdf/*.snm pdf/*.toc
	rm -f pdf/*.vrb

distclean: clean
	rm -f pdf/*.pdf
