### SOURCES
#
# List source TeX files (per quiz section) here
#
SECTIONS=	\
		general.tex \
		things.tex \
		whatisthis.tex \
		places.tex \
		people.tex \
		ballroom.tex

### TOOLING
#
# In principle nothing needs to be changed here
#
# On openSUSE, install texlive-latex-bin-bin
#
TEX=	TEXINPUTS=.:./beamer: pdflatex

all: Quiz.pdf

Quiz.pdf : Quiz.tex $(SECTIONS)
	$(TEX) Quiz
	# $(TEX) Quiz
	@grep ^Q Quiz.log
	$(MAKE) tidy


clean: tidy
	@rm -f Quiz.pdf

tidy:
	@rm -f Quiz.aux Quiz.log Quiz.nav Quiz.out Quiz.snm Quiz.toc preamble.aux witq.aux
