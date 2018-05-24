.PHONY: clean build read aread

filename={{cookiecutter.project_slug}}

SUBDIR_ROOTS := chapters images setup tables
DIRS := . $(shell find $(SUBDIR_ROOTS) -type d)
GARBAGE_PATTERNS := *.aux *.log *.blg *.bbl *.run.xml *.toc *.bcf *.synctex.gz *.fls *.fdb_latexmk *.loa *.lof *.out
GARBAGE := $(foreach DIR,$(DIRS),$(addprefix $(DIR)/,$(GARBAGE_PATTERNS)))

all: build clean

clean:
	rm -rf $(GARBAGE)

build:
	latexmk -pdf -f ${filename}.tex

read:
	evince ${filename}.pdf &

aread:
	acroread ${filename}.pdf

