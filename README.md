# bioc-release

```
FROM rocker/rstudio:4.1.0

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update\
 && apt-get upgrade -y\
 && apt-get install -y curl\
 && apt-get install -y imagemagick\
 && apt-get install -y libblas-dev\
 && apt-get install -y libcairo2-dev\
 && apt-get install -y libfontconfig1-dev\
 && apt-get install -y libfribidi-dev\
 && apt-get install -y libgdal-dev\
 && apt-get install -y libgit2-dev\
 && apt-get install -y libglpk-dev\
 && apt-get install -y libgsl-dev\
 && apt-get install -y libharfbuzz-dev\
 && apt-get install -y liblapack-dev\
 && apt-get install -y libmagick++-dev\
 && apt-get install -y libomp-dev\
 && apt-get install -y libopenblas-dev\
 && apt-get install -y libopenmpi-dev\
 && apt-get install -y libsodium-dev\
 && apt-get install -y libudunits2-dev\
 && apt-get install -y libv8-dev\
 && apt-get install -y libz-dev\
 && apt-get install -y llvm\
 && apt-get install -y qpdf\
 && apt-get install -y ssh\
 && apt-get install -y texlive-full\
 && apt-get install -y tree\
 && apt-get install -y vim\
 && r -e "utils::install.packages('BiocManager')"\
 && r -e "BiocManager::install(ask = FALSE)"\
 && r -e "BiocManager::install('AnnotationHub')"\
 && r -e "BiocManager::install('ExperimentHub')"\
 && r -e "BiocManager::install('BiocCheck')"\
 && r -e "BiocManager::install('BiocStyle')"\
 && r -e "BiocManager::install('Biostrings')"\
 && r -e "BiocManager::install('GenomicRanges')"\
 && r -e "BiocManager::install('MultiAssayExperiment')"\
 && r -e "BiocManager::install('SummarizedExperiment')"\
 && r -e "BiocManager::install('SingleCellExperiment')"\
 && r -e "BiocManager::install('TreeSummarizedExperiment')"\
 && r -e "BiocManager::install('devtools')"\
 && r -e "BiocManager::install('roxygen2')"\
 && r -e "BiocManager::install('snakecase')"\
 && r -e "BiocManager::install('tidymodels')"\
 && r -e "BiocManager::install('tidyverse')"

```
