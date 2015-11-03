# SANER2016
Datasets for the paper "When GitHub meets CRAN: An Analysis of Inter-Repository Package Dependency Problems"

 - checks-history.csv.gz : results of the R CMD check on CRAN.
 - cran-descfiles-150601.csv : DESCRIPTION files for R packages on CRAN.
 - cran-packages-150601.csv - List of archived and unarchived packages.
 - github-cran-150601.csv - Merge of the available data for CRAN and GitHub.
 - github-raw-150601.csv - Raw DESCRIPTION files extracted from GitHub repositories.
 - R-apiv3-2015-01-01T00:00:00-2015-06-01T00:00:00.tar.gz - Raw JSON from the API of GitHub, containing every GitHub repositories related to R that have a PushEvent in Q1+Q2 2015.
 - readme.csv - List of README files that were parsed to find some terms and that contains sentences that were grepped by our regular expressions (see paper for more information)
 - RPackage-Repositories-150101-150601 - List of GitHub repositories extracted from R-apiv3-2015-01-01T00:00:00-2015-06-01T00:00:00.
 - r-travis.csv - List of GitHub repositories containing an identified R package and using Travis-CI.