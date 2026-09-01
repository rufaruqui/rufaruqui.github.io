# CSE 815 -- lecture slides
# Requires: latexmk, TeX Live (beamer, metropolis, pgfplots, tcolorbox), gnuplot.
# -shell-escape is required: cost-surface contours use pgfplots' gnuplot backend.

DECKS := $(basename $(wildcard W*.tex))
PDFS  := $(addsuffix .pdf,$(DECKS))

LATEXMK := latexmk -pdf -shell-escape -interaction=nonstopmode -halt-on-error

all: $(PDFS)

%.pdf: %.tex cse815.sty
	$(LATEXMK) $<

# Rebuild everything and surface only the warnings that matter.
check:
	@$(MAKE) --no-print-directory distclean >/dev/null
	@$(MAKE) --no-print-directory all 2>&1 | grep -Ei '^!|Overfull|Underfull' || echo "clean: no over/underfull boxes"

clean:
	latexmk -c $(DECKS) 2>/dev/null || true
	rm -f *.aux *.log *.nav *.out *.snm *.toc *.vrb *.fdb_latexmk *.fls \
	      *_contourtmp*.table *_contourtmp*.script *_contourtmp*.dat *.gnuplot

distclean: clean
	rm -f $(PDFS)

.PHONY: all check clean distclean
