.PHONY: clean build read aread

filename={{cookiecutter.project_slug}}

all: build clean-all

build:
	latexmk -pdf -f ${filename}.tex

introduction:
	latexmk -pdf -f Abstract.tex

introduction:
	latexmk -pdf -f Introduction.tex

methods:
	latexmk -pdf -f Methods.tex

results:
	latexmk -pdf -f Results.tex

discussion:
	latexmk -pdf -f Discussion.tex

conclusion:
	latexmk -pdf -f Conclusion.tex

appendix:
	latexmk -pdf -f Appendix.tex

guidelines:
	latexmk -pdf -f Guidelines.tex
	
clean-all: clean clean-setup clean-tables

clean:
	find . -name '*.aux' -exec rm -f {} +
	find . -name '*.log' -exec rm -f {} +
	find . -name '*.blg' -exec rm -f {} +
	find . -name '*.bbl' -exec rm -f {} +
	find . -name '*.run.xml' -exec rm -f {} +
	find . -name '*.toc' -exec rm -f {} +
	find . -name '*.bcf' -exec rm -f {} +
	find . -name '*.synctex.gz' -exec rm -f {} +
	find . -name '*.fls' -exec rm -f {} +
	find . -name '*.fdb_latexmk' -exec rm -f {} +
	find . -name '*.loa' -exec rm -f {} +
	find . -name '*.lof' -exec rm -f {} +
	find . -name '*.out' -exec rm -f {} +

clean-setup:
	$(MAKE) -C setup clean

clean-tables:
	$(MAKE) -C tables clean

read:
	evince ${filename}.pdf &

aread:
	acroread ${filename}.pdf

