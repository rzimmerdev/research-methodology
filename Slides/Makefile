VERSION  	?= main
OUTPUT    ?= $(VERSION)
BUILD    ?= build
OUTDIR  ?= $(BUILD)/$(VERSION)

# args for tex
TEXARGS  ?= -interaction=nonstopmode -halt-on-error -file-line-error -synctex=1 -pdf -cd -f

all: $(OUTDIR)/$(OUTPUT).pdf

$(OUTDIR)/$(OUTPUT).pdf: $(VERSION).tex
	latexmk $(TEXARGS) -outdir=$(OUTDIR) $(VERSION).tex

clean:
	latexmk -C
	rm -rf $(BUILD)/*

.PHONY: all clean
