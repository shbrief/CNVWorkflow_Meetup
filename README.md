# CNV Anaylsis Workflow Presentation

November 29th, 2018    
NYC R/Bioconductor Meetup   
Present by Sehyun Oh

Absolute copy number analysis requires simultaneous inference of purity, ploidy, and loss of heterozygosity. Commonly used algorithms rely on high quality genome-wide data with matched normal profiles, limiting their applicability in clinical settings. In this workshop, I will introduce a benchmark example of absolute copy number variation (CNV) analysis from tumor-only whole exome sequencing (WES) data, followed by a step-by-step tutorial on the analysis workflow. The workflow is based on PureCN, a R/Bioconductor package.

## PureCN
A tool developed for tumor-only diagnostic sequencing using hybrid-capture
protocols. It provides copy number adjusted for purity and ploidy and can
classify mutations by somatic status and clonality. It requires a pool of
process-matched normals for coverage normalization and artifact filtering.
(https://github.com/lima1/PureCN)

## Installation

The major package we are using is PureCN.   
To install this package, start R and enter:

```
if (!requireNamespace("BiocManager", quietly=TRUE))
    install.packages("BiocManager")
BiocManager::install("PureCN")
```
Some optional packages:

```
BiocManager::install("TCGAutils")
BiocManager::install("jsonlite")
BiocManager::install("curl")
BiocManager::install("downloader")
BiocManager::install("GenomicDataCommons")
BiocManager::install("magrittr")
BiocManager::install("rtracklayer")
```

## Meetup materials
http://rpubs.com/shbrief/meetup_1   
http://rpubs.com/shbrief/meetup_2

## Paper

Riester M, Singh A, Brannon A, Yu K, Campbell C, Chiang D and Morrissey M
(2016). “PureCN: Copy number calling and SNV classification using targeted
short read sequencing.” _Source Code for Biology and Medicine_, **11**, pp. 13.
doi: [10.1186/s13029-016-0060-z](https://doi.org/10.1186/s13029-016-0060-z).
