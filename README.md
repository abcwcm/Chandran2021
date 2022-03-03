# Stimulation Induced Functional TCR sequencing (SIFT-seq): VDJ and scRNA-seq of T cells targeting public neoantigens

*Herein, we report the development and application of a high-throughput platform that combines single-cell transcriptomic and paired alpha/beta T cell receptor (TCR) sequencing to test whether Mut PIK3CA generates an immunogenic public NeoAg. Using this method, we developed a panel of TCRs that recognize an endogenously processed neoepitope resulting from a common PIK3CA hotspot mutation.*

The platform developed by the Klebanoff Lab entails the following steps:

1. naive T cells (TN) from a healthy donor undergo in vitro sensitization (IVS) with autologous monocyte-derived dendritic cells (moDCs) electroporated with mRNA encoding the Mut driver gene. HD T cells are selected to ensure sampling of a broad TCR repertoire that has not been exposed to the potentially tolerogenic environment present within cancer patients.
2. Matched aliquots from sensitized wells are re-stimulated with moDCs expressing the Mut or wildtype (WT) version of the driver gene. Cycle threshold (Ct) values, which inversely correlate with transcript abundance, are measured for the gene encoding IFNG using qPCR. A regression analysis is then performed to identify "hit" wells containing Mut-specific T cells that show higher activation levels in the presence of the mutated antigen compared to the WT antigen.
3. T cells from "hit" wells are again acutely re-stimulated with moDCs to identify reactive clonotypes and retrieve their TCR gene sequences. This step, which we have termed Stimulation Induced Functional TCR sequencing (SIFT-seq), is accomplished using combined single-cell (sc) TCR V(D)J and RNA sequencing. 
4. Finally, TCR clonotypes that selectively express T cell activation transcripts in response to a Mut variant of the driver but not its WT counterpart are reconstructed for functional validation. 

--------------------------------------

This repository contains the code that was used to generate draft versions of the figures shown in the final manuscript. 
For reasons of legibility, most final figures based on single-cell RNA-seq data were generated in GraphPad Prism; you can find the corresponding data files (text files, spread sheets) here as well. 

The basis for the figures is the **processed scRNA-seq/VDJ-seq data**, for which we have generated **one R package per patient/donor**.

* **21LT2**: [R package repo](https://github.com/abcwcm/Klebanoff21LT2) [![DOI](https://zenodo.org/badge/465661359.svg)](https://zenodo.org/badge/latestdoi/465661359)
* **0606T1**: [R package repo](https://github.com/abcwcm/Klebanoff0606T1) [![DOI](https://zenodo.org/badge/465691691.svg)](https://zenodo.org/badge/latestdoi/465691691)
* **MR4050** (MK_02 in the paper): [R package repo](https://github.com/abcwcm/KlebanoffMR4050) [![DOI](https://zenodo.org/badge/465693977.svg)](https://zenodo.org/badge/latestdoi/465693977)

These packages contain all code for the processing and analysis of the **combined single-cell RNA-seq and single-cell TCR-seq** samples, details can be found in the vignettes of each package.
In brief, the steps were:

1. associate the transcriptome information of individual cells with their corresponding TCR sequences (= clonotype), 
2. assign clonotype IDs that identify cells with the same clonotype across the two conditions (stimulated with (1) WT antigen or (2) with the tumor antigen),
3. identify the clonotype that shows the greatest increase of cytotoxic/effector function (based on expression of IFNg, IL-2, TNFa),
4. determine additional genes that are differentially expressed when comparing the cells of the MUT-antigen condition to the cells of the WT-antigen condition from the same clonotype.

To run the code of the figures, you'll need to **download and install these packages** as they come with their own functions to access the data for each donor.

For the raw data (i.e. CellRanger output, see GEO accession number: GSE172403).

![](https://raw.githubusercontent.com/abcwcm/Scott2019/master/WCM_MB_LOGO_HZSS1L_CLR_RGB.png)

The code deposited here was written by Friederike Dündar at the [Applied Bioinformatics Core](https://abc.med.cornell.edu) of Weill Cornell Medicine.
Don't hesitate to get in touch with questions either via the issues panel here or via `abc -at- med.cornell.edu`.

