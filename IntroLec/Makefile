R_OPTS=--no-save --no-restore --no-init-file --no-site-file # --vanilla, but without --no-environ

STEM = qtl_intro

FIGS = Figs/scale_fig1.pdf \
	   Figs/batches_fig1.pdf \
	   Figs/epistasis_f2.pdf \
	   Figs/congenic.pdf \
	   Figs/ail.pdf \
	   Figs/hs.pdf \
	   Figs/rilines.pdf \
	   Figs/ri8.pdf \
	   Figs/pleiotropy_network.pdf \
	   Figs/causal_network.pdf \
	   Figs/plot-eqtl-islet.png

$(STEM).pdf: $(STEM).tex header.tex $(FIGS)
	xelatex $<

web: $(STEM).pdf
	scp $(STEM).pdf broman-10.biostat.wisc.edu:Website/presentations/PBPG2018intro.pdf

Figs/scale_fig1.pdf: R/scale_fig.R
	cd $(<D);R $(R_OPTS) -e "source('$(<F)')"

Figs/batches_fig1.pdf: R/batches_fig.R
	cd $(<D);R $(R_OPTS) -e "source('$(<F)')"

Figs/epistasis_f2.pdf: R/epistasis_fig.R
	cd $(<D);R $(R_OPTS) -e "source('$(<F)')"

Figs/congenic.pdf: R/congenic_fig.R
	cd $(<D);R $(R_OPTS) -e "source('$(<F)')"

Figs/ail.pdf: R/ail_fig.R
	cd $(<D);R $(R_OPTS) -e "source('$(<F)')"

Figs/hs.pdf: R/hs_fig.R
	cd $(<D);R $(R_OPTS) -e "source('$(<F)')"

Figs/ri8.pdf: R/ri8_fig.R
	cd $(<D);R $(R_OPTS) -e "source('$(<F)')"

Figs/rilines.pdf: R/rilines_fig.R
	cd $(<D);R $(R_OPTS) -e "source('$(<F)')"

Figs/causal_network.pdf: R/causal_network.R
	cd $(<D);R $(R_OPTS) -e "source('$(<F)')"

Figs/pleiotropy_network.pdf: R/pleiotropy_network.R
	cd $(<D);R $(R_OPTS) -e "source('$(<F)')"
