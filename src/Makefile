TARGETS      := main.pdf
PDFLATEX     := $$pdflatex='pdflatex -interaction=nonstopmode -synctex=1 %S %O'
LATEXMK      := latexmk -cd -e $(PDFLATEX) -f -pdf
CHECKPOINT   := 

all : $(TARGETS)

%.pdf : %.tex
	$(LATEXMK) $<

.PHONY : all

clean : 
	latexmk -c
	rm -f $(wildcard *.pdf)
