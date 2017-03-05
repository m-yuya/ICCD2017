# Title: Makefile
# Date:  2016/03/03
# Name:  Yuya, Takuro

# Target file name
TARGET = codes+isss2017
# BIB file
REFDIR = ./
# REFDIR = ../../bib/
REF = $(REFDIR)/reference.bib
# CLASS File
CLS = sig-alternate-05-2015.cls

# platex
PLATEX = platex
# dvipdfmx
DVIPDFMX = dvipdfmx
# pbibtex
PBIBTEX = pbibtex

# Objects
OBJS := $(TARGET).aux $(TARGET).log $(TARGET).dvi
PDFOBJ := $(TARGET).pdf
BIBOBJS := $(TARGET).bbl $(TARGET).blg

#
# Target
#

.PHONY: all
all: dvi pdf

.PHONY: dvi
dvi: $(OBJS)

$(OBJS): $(TARGET).tex $(REF)
	$(PLATEX) $(TARGET).tex
	$(PBIBTEX) $(TARGET)
	$(PLATEX) $(TARGET).tex
	$(PLATEX) $(TARGET).tex

.PHONY: pdf
pdf: $(PDFOBJ)

$(PDFOBJ): $(TARGET).dvi
	$(DVIPDFMX) $(TARGET).dvi

.PHONY: simple
simple: 
	$(PLATEX) $(TARGET).tex
	$(PLATEX) $(TARGET).tex
	$(DVIPDFMX) $(TARGET).dvi

# 
# Optional Target
# 

.PHONY: diff
diff:
	sh latexdiff2pdf.bash $(TARGET)

.PHONY: clean
clean:
	rm -f $(OBJS) $(BIBOBJS)

.PHONY: realclean
realclean:
	rm -f $(OBJS) $(BIBOBJS) $(PDFOBJ)
