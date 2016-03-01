#
# $Id$
#
FIG2DEV=fig2dev
#LANG=ps
LANG=eps
FIGFILES=
EPSFILES=$(FIGFILES:.fig=.eps)
PDFFILES=$(EPSFILES:.eps=.pdf)
all: eps pdf
eps: ${EPSFILES}
pdf: eps ${PDFFILES}

%.pdf: %.eps
	epstopdf $<
%.eps: %.fig
	${FIG2DEV} -L ${LANG} $< $*.eps
clean:
	rm -f *.eps *.pdf *.bak
