.PHONY: clean build read aread

filename={{cookiecutter.project_slug}}

all: build clean-all read

build:
	pdflatex -interaction=nonstopmode -output-format=pdf ${filename}.tex
	biber ${filename}
	pdflatex -interaction=nonstopmode -output-format=pdf ${filename}.tex
	pdflatex -interaction=nonstopmode -output-format=pdf ${filename}.tex

abstract: filename=Abstract
abstract: build clean-all read

introduction: filename=Introduction
introduction: build clean-all read

methods: filename=Methods
methods: build clean-all read

results: filename=Results
restuls: build clean-all read

discussion: filename=Discussion
discussion: build clean-all read

conclusion: filename=Conclusion
conclusion: build clean-all read

appendix: filename=Appendix
appendix:build clean-all read
	
clean-all: clean clean-tables

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
	find . -name '*.lot' -exec rm -f {} +
	find . -name '*.out' -exec rm -f {} +

clean-tables:
	$(MAKE) -C tables clean

read:
	xdg-open ${filename}.pdf &

# PDF compression (low quality - small filesize)
screen:
	gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dNOPAUSE -dQUIET -dBATCH -dPDFSETTINGS=/screen -sOutputFile=${filename}_screen.pdf ${filename}.pdf

# PDF compression (medium quality - medium filesize)
ebook:
	gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dNOPAUSE -dQUIET -dBATCH -dPDFSETTINGS=/ebook -sOutputFile=${filename}_ebook.pdf ${filename}.pdf

# PDF compression (high quality - largest but smaller than original filesize)
prepress:
	gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dNOPAUSE -dQUIET -dBATCH -dPDFSETTINGS=/prepress -sOutputFile=${filename}_prepress.pdf ${filename}.pdf
