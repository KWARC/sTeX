STEXDIR = ../..
TARGET = paper.tex
MODSLIBDIR = ../background
BIBINPUTS = $(PREFIX)/lib/bib:

include $(STEXDIR)/lib/make/Makefile.vars
all: pdf 
include $(STEXDIR)/lib/make/Makefile.in 

localize:
	python3 $(HOME)/vc/git/github.com/sLaTeX/lmhtools/minimathhub.py paper.tex

