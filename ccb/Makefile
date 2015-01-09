all: ccb.pdf

%.pdf: %.tex
	pdflatex -interaction=nonstopmode $?
	pdflatex -interaction=nonstopmode $?

clean:
	rm -rf *.pdf *.log *.aux *.out
