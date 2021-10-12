# imavirus: finding virus integration sites, and more!* (*allegedly)


## Contributors

Alejandro Gener (lead), 
Michael Jochum, 
Hiroko Ohmiya, 
Carolina Peralta (writer), 
Remy Schwab, 
Rajarshi Mondal, 
Daniel Cameron, 
Enrico Barrozo, 
Fawaz Dabbaghie, 


## Description
Identifying insertions and in particular virus integration sites is challenging. Moreover, there are not many tools to reliabliy detect viral presence and integration events. 
Many virus have the capability of integrating into host genomes and can lead to DNA damage and disrupt genes. 	
The aim of this project is to find putative virus integration sites (pIS) in public data. Identifying insertion sites from genomic DNA is challenging.


## Goals

This project has two main aims: 1) to identify (putative) integration sites (pIS) in public data and 2) Determining whether insertion sites occur at sites which may affect cell-function (contribute to disease?) and/or anti-viral responses (which may contribute to virus fitness). 


## Overview Diagram

![](https://github.com/collaborativebioinformatics/imavirus/blob/2f27cd88604fc01b134df44fc492afca9830ef25/Untitled%20Diagram%20v2.jpg)

## Methods

SRA -> Accessions 

Minimap2 will be used to query thresholded data.

Quality control measures

## Test data

![](https://github.com/collaborativebioinformatics/imavirus/blob/faea5562d55e5ac4700ae02ffdca48d0b5d2b284/Screen%20Shot%202021-10-12%20at%2011.51.39%20AM.png)

Above depends on depositors including virus-specific metadata.

For EBV, ENCODE data from lymphoblasrtoid cell lines may not have EBV metadata.

Tg26 HIV transgenic mouse RNA-seq data will be used to evaluate insertion sites from RNA-seq. The accession for the pNL4-3 used to make the Tg26 mouse is GenBank:AF324493.2.

## Results

## Sources

Other tools doing similar things:

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6357354/

https://academic.oup.com/nar/article/46/7/3309/4944397

Tools:

Minimap2: Li, Heng. 2018. “Minimap2: Pairwise Alignment for Nucleotide Sequences.” Bioinformatics 34(18):3094–3100.

Datasets:

Tg26 mouse: https://www.jax.org/strain/022354

Tg26 RNA-seq dataset: Chakravarthi, V. Praveen, Sireesha Yerrathota, Priyanka Radadiya, Clark Bloomer, Sumedha Gunewardhana, and Madhulika Sharma. 2020. “Transcriptomic Data Indicating Differential Expressed Genes between HIV-1 Associated Nephropathy (HIVAN) Mouse Model (Tg26) and Wildtype Mice.” Data in Brief 30:4–8.

Tg26 insertion site: Gharavi, A. G., T. Ahmad, R. D. Wong, R. Hooshyar, J. Vaughn, S. Oller, R. Z. Frankel, L. A. Bruggeman, V. D. D’Agati, P. E. Klotman, and R. P. Lifton. 2004. “Mapping a Locus for Susceptibility to HIV-1-Associated Nephropathy to Mouse Chromosome 3.” Proc Natl Acad Sci U S A 101(8):2488–93.

Multiple Tg26 transgenes: A. R. Gener, T. Washington, D. Hyink, P. Klotman. “The Multiple HIV-1 Transgenes in the Murine Model of HIV-Associated Nephropathy Fail to Segregate as Expected.” American Society of Human Genetics Virtual  Meeting, USA. October 27-30, 2020.
