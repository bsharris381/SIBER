SIBER
=====

[![cran version](http://www.r-pkg.org/badges/version/SIBER)](http://cran.rstudio.com/web/packages/SIBER) 
[![rstudio mirror downloads](http://cranlogs.r-pkg.org/badges/SIBER?)](https://github.com/metacran/cranlogs.app)
[![rstudio mirror downloads](http://cranlogs.r-pkg.org/badges/grand-total/SIBER?color=82b4e8)](https://github.com/metacran/cranlogs.app)

Ellipse and convex hull fitting package to estimate niche width for stable isotope data (and potentially other relevant types of data)

[MixSIAR](https://github.com/brianstock/MixSIAR) is intended to encompass all the mixing model functionality in the [SIAR package](http://www.tcd.ie/Zoology/research/research/theoretical/siar.php). Additionally, we have updated the basic mixing model from SIAR and released this as a standalone pacakge for basic mixing model fitting as [simmr](https://cran.r-project.org/web/packages/simmr/). 

### Version notes
+ v2.0.1 allows character strings to be used as group labels in place of sequential numbering. Additionally, axes limits for `plotSiberObject()` can be manually specified using the new arguments `x.limits` and `y.limits`. See associated help files and vignettes for more information.
+ v2.0.0 is a major update over the functions embedded in the related package `siar`. The two big internal changes are: 1) fitting is now done by JAGS; and 2) data are internally mean centred and standardised prior to fitting before being back-transformed. Both of these changes improve model fitting and convergence.

## Important!!
SIAR development will stop at some point in the future (probably in late 2015),
and the SIBER routines will become orphaned. This is the start of a full recode of SIBER to be a standalone package. 
Also intended are some major improvements to model fitting, via z-scoring and back-transforming to improve fitting 
via MCMC in JAGS. 

Comments and suggestions welcome. If anyone wants to contribute code, please let me know and we can chat about how 
to proceed.

## Installation
This package is released on CRAN as v2.0.1. Type `install.packages("SIBER")`.

Alternatively, you can install directly from github

  - the stable release can be installed by
    - `library(devtools)` # install if necessary
    - install_github("andrewljackson/SIBER@v2.0.1")
    - library(SIBER)
  - The development (**and not guaranteed stable**) release is the master branch
    - `library(devtools)` # install if necessary
    - install_github("andrewljackson/SIBER@master")
    - library(SIBER)


## Tutorials
More information and examples from the previous version of SIBER which is part of the SIAR package is available from [my website](http://www.tcd.ie/Zoology/research/research/theoretical/Rpodcasts.php#siber). Much of this instructional content remains true, although the implementation of the code has changed substantially (for the better I hope).

The package vingette provides working examples of the two main analysis types.

## Help, Assistance and Queries
In the first instance, queries about analyses or problems with the software should be posted to [stackoverflow](https://stackoverflow.com/questions/tagged/siber) using the tag `siber`. If you are convinced you have discovered a bug or major problem in the software, you can raise an [issue here on github](https://github.com/AndrewLJackson/SIBER/issues).

##Acknowledgments
Some code and much input from my collaborator and co-author [Andrew Parnell](http://mathsci.ucd.ie/people/parnell_a) [@aparnellstats](https://twitter.com/aparnellstats). Thanks to Alex Bond [@thelabandfield](https://twitter.com/thelabandfield) for helping identify some problems in model fitting which is now resolved by z-scoring, fitting and back-transforming. Although not affecting every analysis, the potential issue is exemplified in [SIBER-sandbox]( https://github.com/AndrewLJackson/SIBER-sandbox).

## Citation
Jackson, A.L., Parnell, A.C., Inger R., & Bearhop, S. 2011. Comparing isotopic niche widths among and within communities: SIBER – Stable Isotope Bayesian Ellipses in R. Journal of Animal Ecology, 80, 595-602. [doi](http://dx.doi.org/10.1111/j.1365-2656.2011.01806.x)
