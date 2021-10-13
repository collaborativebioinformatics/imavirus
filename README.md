# imavirus: Interrogating MAssive public databases to identify clinically relevant Viral integration sites from available unbiased RNA-seq datasets.


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

***Figure 1: Project overview

![](https://github.com/collaborativebioinformatics/imavirus/blob/7dd2b136a9592c2cb86b449f48f7b54aa2df7a67/SV%20hackathon%20figure.jpg)
***Figure 2: Reads from single- and paired-end data can support putative virus integration (insertion) sites.

## Methods

1.) SRA -> Accessions 

2.) Human reference genome: hg19. Mouse reference genome mm10. See table for virus reference genomes.

3.) Quality control measures include at read level and target coverage. Minimap2/STAR/HISAT2 will be used to query thresholded data.

4.) We will evaluate common mappers Minimap2/STAR/HISAT2 for their ability to identify HIV transgene insertion sites from a the Tg26 model organism (Jax:022354). Tg26 is a mouse with HIV inserted as a transgene in 15 copies across several previously characterized sites (Gener et al. 2020).

## Test data

![](https://github.com/collaborativebioinformatics/imavirus/blob/84a24bed481bd93c2771a7d395ef160db5497db3/Screen%20Shot%202021-10-12%20at%202.57.23%20PM.png)
***Table 1: Viruse reference genomes considered

![](https://github.com/collaborativebioinformatics/imavirus/blob/faea5562d55e5ac4700ae02ffdca48d0b5d2b284/Screen%20Shot%202021-10-12%20at%2011.51.39%20AM.png)
***Table 2: Metrics for datasets pulled from Short Read Archive (SRA) before threshholding.

Above depends on depositors including virus-specific metadata.

For EBV, ENCODE data from lymphoblasrtoid cell lines may not have EBV metadata.

Tg26 HIV transgenic mouse RNA-seq data will be used to evaluate insertion sites from RNA-seq. The accession for the pNL4-3 used to make the Tg26 mouse is GenBank:AF324493.2.

## Results

![](https://github.com/collaborativebioinformatics/imavirus/blob/9f98ed66786761bb9c3a7d75e78c0c0eecf58f17/Screen%20Shot%202021-10-12%20at%2011.05.21%20PM.png)
***Figure 3: HISAT2 retained read group and pairs' chromosome info for easy visual inspection. Putative insertion half-sites on chr8 are supported my short-read data. Data: SRR10302267. The pNL4-3 plasmid backbone segment is marked in red. Breakpoints analogous to reads spannig insertion half-sites occure upstream and downstream of plasmid backbone.

![](https://github.com/collaborativebioinformatics/imavirus/blob/10e9939a319b1c3306493a512a61ac25b1e9aeeb/snapshort_01.png)
***Figure 4: STAR notes chimeric reads (Figure 2), recapitulating an HIV transgene insertion half-site in mouse Dcaf15. The other site on chr8 is in Cdc2a, which is our of frame.


## Sources

***Other tools doing similar things:

Nguyen, Nam-phuong D., Viraj Deshpande, Jens Luebeck, Paul S. Mischel, and Vineet Bafna. 2018. “ViFi: Accurate Detection of Viral Integration and MRNA Fusion Reveals Indiscriminate and Unregulated Transcription in Proximal Genomic Regions in Cervical Cancer.” Nucleic Acids Research 46(7):3309–25.

Xia, Yuchao, Yun Liu, Minghua Deng, and Ruibin Xi. 2019. “Detecting Virus Integration Sites Based on Multiple Related Sequencing Data by VirTect.” BMC Medical Genomics 12(Suppl 1):19.

Cameron, Daniel L., Nina Jacobs, Paul Roepman, Peter Priestley, Edwin Cuppen, and Anthony T. Papenfuss. 2021. “VIRUSBreakend: Viral Integration Recognition Using Single Breakends.” Bioinformatics 37(19):3115–19.

***Tools used:

Minimap2: Li, Heng. 2018. “Minimap2: Pairwise Alignment for Nucleotide Sequences.” Bioinformatics 34(18):3094–3100.

STAR: Dobin, Alexander, Carrie A. Davis, Felix Schlesinger, Jorg Drenkow, Chris Zaleski, Sonali Jha, Philippe Batut, Mark Chaisson, and Thomas R. Gingeras. 2013. “STAR: Ultrafast Universal RNA-Seq Aligner.” Bioinformatics (Oxford, England) 29(1):15–21.

HISAT2: Kim, Daehwan, Ben Langmead, and Steven L. Salzberg. 2015. “HISAT : A Fast Spliced Aligner with Low Memory Requirements.” 12(4).

Galaxy: Afgan, Enis, Dannon Baker, Marius van den Beek, Daniel Blankenberg, Dave Bouvier, Martin Čech, John Chilton, Dave Clements, Nate Coraor, Carl Eberhard, Björn Grüning, Aysam Guerler, Jennifer Hillman-Jackson, Greg Von Kuster, Eric Rasche, Nicola Soranzo, Nitesh Turaga, James Taylor, Anton Nekrutenko, and Jeremy Goecks. 2016. “The Galaxy Platform for Accessible, Reproducible and Collaborative Biomedical Analyses: 2016 Update.” Nucleic Acids Research 44(W1):W3–10.

***Datasets:

Tg26 mouse: https://www.jax.org/strain/022354

Tg26 RNA-seq dataset: Chakravarthi, V. Praveen, Sireesha Yerrathota, Priyanka Radadiya, Clark Bloomer, Sumedha Gunewardhana, and Madhulika Sharma. 2020. “Transcriptomic Data Indicating Differential Expressed Genes between HIV-1 Associated Nephropathy (HIVAN) Mouse Model (Tg26) and Wildtype Mice.” Data in Brief 30:4–8.

Tg26 insertion site: Gharavi, A. G., T. Ahmad, R. D. Wong, R. Hooshyar, J. Vaughn, S. Oller, R. Z. Frankel, L. A. Bruggeman, V. D. D’Agati, P. E. Klotman, and R. P. Lifton. 2004. “Mapping a Locus for Susceptibility to HIV-1-Associated Nephropathy to Mouse Chromosome 3.” Proc Natl Acad Sci U S A 101(8):2488–93.

Multiple Tg26 transgenes: A. R. Gener, T. Washington, D. Hyink, P. Klotman. “The Multiple HIV-1 Transgenes in the Murine Model of HIV-Associated Nephropathy Fail to Segregate as Expected.” American Society of Human Genetics Virtual  Meeting, USA. October 27-30, 2020.
