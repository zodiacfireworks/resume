LANG    = "${LANG:-es}"
TEX     = xelatex
SRC_DIR = resume
SRC     = resume.tex $(shell find $(SRC_DIR) -name '*.tex')
OUT_DIR = ../build
OUT     = resume.pdf

.PHONY: all all-before all-after clean-custom clean

all: clean $(OUT) clean-custom

clean-custom:
	rm -rf *.aux *.lof  *.log *.lot  *.fls *.out  *.toc *.fdb_latexmk  *.synctex.gz *.tmp

clean: clean-custom
	rm -rf *.pdf

clean-all: clean
	rm -rf $(OUT_DIR)/*pdf

$(OUT):
	LANG=$(LANG) $(TEX) -shell-escape $(SRC) && $(TEX) -shell-escape $(SRC) && mv $(OUT) $(OUT_DIR)/resume_$(LANG).pdf
