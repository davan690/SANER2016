# SANER2016

This repository contains the (Python) notebooks and datasets that we have generated and processed for the paper (currently under submission) *When GitHub meets CRAN: An Analysis of Inter-Repository Package Dependency Problems*, co-authored by A. Decan, T. Mens, M. Claes, Ph. Grosjean (COMPLEXYS Research Institute, University of Mons, Belgium).
It also contains anonymised and sanitised versions of email interviews that we have carried out with R package maintainers active on GitHub, in order to confirm some of our findings.

## Interviews with R package maintainers
 - email-interview.pdf - results of the interviews with R selected R package maintainers.

## Datasets

### CRAN results 
 - checks-history.csv.gz - Results of the R CMD check on CRAN.
 - cran-descfiles-150601.csv - DESCRIPTION files (package metadata) for R packages on CRAN.
 - cran-packages-150601.csv - List of archived and unarchived packages.
 
### GitHub results
 - github-raw-150601.csv - Raw DESCRIPTION files (package metadata) extracted from R packages stored in GitHub repositories.
 - R-apiv3-2015-01-01T00:00:00-2015-06-01T00:00:00.tar.gz - Raw JSON from the API of GitHub, containing every GitHub repository related to R having a PushEvent in Q1+Q2 2015.
 - RPackage-Repositories-150101-150601.csv - List of GitHub repositories extracted from R-apiv3-2015-01-01T00:00:00-2015-06-01T00:00:00.
 - r-travis.csv - List of GitHub repositories containing an identified R package and using Travis-CI.
 - readme.csv - List of README files that were parsed to find some terms and that contains sentences that were grepped by our regular expressions (see paper for more information).

### Merged CRAN + GitHub results
 - github-cran-150601.csv - Merge of the available data for CRAN and GitHub.


## Python notebooks

These notebooks can be run using Jupyter and a Python kernel. 
They require external dependencies like numpy, scipy, seaborn, etc. 
The required dependencies are listed in the beginning of each notebook.


### Extraction & Transformation

 - GitHub - Repositories from API.ipynb - Query GitHub API to find a list of repositories that are related to R. This notebook populates *R-apiv3-2015-01-01T00:00:00-2015-06-01T00:00:00.tar.gz*.
 - GitHub - R Package Repository Identification.ipynb - Based on the result of the previous notebook, query each candidate repository to find a *DESCRIPTION* file. Results were stored in *RPackage-Repositories-150101-150601.csv*
 - GitHub - Data Extraction.ipynb - Given a local clone of each repository from *RPackage-Repositories-150101-150601.csv*, extract every version of the *DESCRIPTION* file. This notebook populates *github-raw-150601.csv*.
 - Parse README's from GitHub packages.ipynb - Given a local clone of each repository from the GitHub packages listed in *github-cran-150601.csv*, look in each version of the README's in those repositories for a set of interesting keywords. This notebook populates *readme.csv*.
 - Merging GitHub and CRAN data.ipynb - Merge the data from *github-raw-150601.csv*, *cran-descfiles-150601.csv* and *cran-packages-150601.csv* for further analysis.


### Analysis
 
 - SANER paper (1).ipynb - Distribution of R packages, survival analysis, R packages dependencies, source analysis, updade frequency & impact analysis, 
 - SANER paper (2).ipynb - R packages dependencies & maintainers analyses
 - SANER paper (3).ipynb - R packages README analyses
