.PHONY: introduction methods results conclusion appendix clean

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
	
clean:
	find . -name '*.aux' -exec rm -f {} +
