# SIFT-seq: VDJ and scRNA-seq of T cells targeting public neoantigens

>GEO accession number: GSE172403 -- for processed data, see the individual donor's R packages

Naïve CD8+ T cells from healthy donor samples were stimulated in vitro with mutated PIK3CA. Following a qPCR screen to identify mutation-specific upregulation of inflammatory transcript, positive wells were selcted for SIFT-seq. Matched aliquots were restimulated acutely with antigen-presenting wells expressing WT or mutated PIK3CA and subject to single-cell RNA-seq and V(D)J immunoprofiling using the 10x genomics platform. All clonotypes associated with a mutation-specific activation signature were identified and their TCR gene sequences were retrieved. Candidate TCR gene sequences were retrovirally transferred to open-repertoire T cell to confirm mutation-specific recognition.

This repository contains the code that was used to generate draft versions of the figures shown in the final manuscript. 
For reasons of legibility, most final figures based on single-cell RNA-seq data were generated in GraphPad Prism; you can find the corresponding data files (text files, spread sheets) here as well. 

The basis for the figures is the **processed scRNA-seq/VDJ-seq data**, for which we have generated **one R package per patient/donor**.

* 21LT2
* 0606T1
* MR4050/MK_02

These packages contain all code for the processing and analysis of the **combined single-cell RNA-seq and single-cell TCR-seq** samples, details can be found in the vignettes of each package.
In brief, the steps were:

1. associate the transcriptome information of individual cells with their corresponding TCR sequences (= clonotype), 
2. assign clonotype IDs that identify cells with the same clonotype across the two conditions (stimulated with (1) WT antigen or (2) with the tumor antigen),
3. identify the clonotype that shows the greatest increase of cytotoxic/effector function (based on expression of IFNg, IL-2, TNFa),
4. determine additional genes that are differentially expressed when comparing the cells of the MUT-antigen condition to the cells of the WT-antigen condition from the same clonotype.

To run the code of the figures, you'll need to **download and install these packages** as they come with their own functions to access the data for each donor.

![](https://raw.githubusercontent.com/abcwcm/Scott2019/master/WCM_MB_LOGO_HZSS1L_CLR_RGB.png)

The code deposited here was written by Friederike Dündar at the [Applied Bioinformatics Core](https://abc.med.cornell.edu) of Weill Cornell Medicine.
Don't hesitate to get in touch with questions either via the issues panel here or via `abc -at- med.cornell.edu`.

