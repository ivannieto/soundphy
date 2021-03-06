SPHINXOPTS    =
SPHINXBUILD   = sphinx-build
BUILDDIR      = build

ALLSPHINXOPTS   = -d $(BUILDDIR)/doctrees $(SPHINXOPTS) source

.PHONY: help clean html changes linkcheck

help:
	@echo "Please use \`make <target>' where <target> is one of"
	@echo "  html       standalone HTML files"
	@echo "  changes    overview of all changed/added/deprecated items"
	@echo "  linkcheck  check all external links for integrity"

clean:
	-rm -rf $(BUILDDIR)/*

html:
	$(SPHINXBUILD) -b html $(ALLSPHINXOPTS) $(BUILDDIR)/html
	@echo
	@echo "Build finished. The HTML pages are in $(BUILDDIR)/html."

latexpdf:
	$(SPHINXBUILD) -b latex $(ALLSPHINXOPTS) $(BUILDDIR)/latex
	@echo "Running LaTeX files through pdflatex..."
	make -C $(BUILDDIR)/latex all-pdf
	@echo "pdflatex finished; the PDF files are in $(BUILDDIR)/latex."

changes:
	$(SPHINXBUILD) -b changes $(ALLSPHINXOPTS) $(BUILDDIR)/changes
	@echo
	@echo "The overview file is in $(BUILDDIR)/changes."

linkcheck:
	$(SPHINXBUILD) -b linkcheck $(ALLSPHINXOPTS) $(BUILDDIR)/linkcheck
	@echo
	@echo "Link check complete; look for any errors in the above output " \
	      "or in $(BUILDDIR)/linkcheck/output.txt."
