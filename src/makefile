TEX     = xelatex
SRC_DIR = resume
SRC     = resume.tex $(shell find $(SRC_DIR) -name '*.tex')
OUT_DIR = ../build
OUT     = $(OUT_DIR)/resume.pdf

.PHONY: all all-before all-after clean-custom clean

all: clean $(OUT) clean-custom

clean-custom:
	rm -rf  *.aux $(OUT_DIR)/*.aux *.lof $(OUT_DIR)/*.lof *.log $(OUT_DIR)/*.log *.lot $(OUT_DIR)/*.lot *.fls $(OUT_DIR)/*.fls *.out $(OUT_DIR)/*.out *.toc $(OUT_DIR)/*.toc *.fdb_latexmk $(OUT_DIR)/*.fdb_latexmk *.synctex.gz $(OUT_DIR)/*.synctex.gz

clean: clean-custom
	rm -rf *.pdf $(OUT_DIR)/*.pdf

$(OUT):
	$(TEX) -output-directory=$(OUT_DIR) $(SRC) && $(TEX) -output-directory=$(OUT_DIR) $(SRC) && make clean-custom
