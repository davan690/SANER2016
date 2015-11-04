# SANER2016
This GitHub repository contains the datasets that we has generated and processed for the paper (currently under submission) *When GitHub meets CRAN: An Analysis of Inter-Repository Package Dependency Problems*, co-authored by A. Decan, T. Mens, M. Claes, Ph. Grosjean (COMPLEXYS Research Institute, University of Mons, Belgium)

## CRAN results 
 - checks-history.csv.gz : results of the R CMD check on CRAN.
 - cran-descfiles-150601.csv : DESCRIPTION files (package metadata) for R packages on CRAN.
 - cran-packages-150601.csv - List of archived and unarchived packages.
 
## GitHub results
 - github-raw-150601.csv - Raw DESCRIPTION files (package metadata) extracted from R packages stored in GitHub repositories.
 - R-apiv3-2015-01-01T00:00:00-2015-06-01T00:00:00.tar.gz - Raw JSON from the API of GitHub, containing every GitHub repository related to R having a PushEvent in Q1+Q2 2015.
 - RPackage-Repositories-150101-150601 - List of GitHub repositories extracted from R-apiv3-2015-01-01T00:00:00-2015-06-01T00:00:00.
 - r-travis.csv - List of GitHub repositories containing an identified R package and using Travis-CI.
 - readme.csv - List of README files that were parsed to find some terms and that contains sentences that were grepped by our regular expressions (see paper for more information)

## Merged CRAN + GitHub results
 - github-cran-150601.csv - Merge of the available data for CRAN and GitHub.
