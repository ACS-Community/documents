TEXFILES = $(wildcard *.tex)
PDFFILES = $(TEXFILES:.tex=.pdf)

all: pdf clean

pdf: $(PDFFILES)

%.pdf: %.tex
	@rubber --pdf $<
	@if [ -d publish ];then mv *.pdf publish; else mkdir publish; mv *.pdf publish/;fi

clean:
	@rubber --clean $(TEXFILES:.tex=)

distclean: clean
	@rubber --clean --pdf $(TEXFILES:.tex=)
	@rm -rf publish

x_plain:
	@evince publish/plain_main.pdf

x_paper:
	@evince publish/paper_main.pdf
