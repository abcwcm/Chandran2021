# SIFT-seq: VDJ and scRNA-seq of T cells targeting public neoantigens

GEO accession number: GSE172403

Naïve CD8+ T cells from healthy donor samples were stimulated in vitro with mutated PIK3CA. Following a qPCR screen to identify mutation-specific upregulation of inflammatory transcript, positive wells were selcted for SIFT-seq. Matched aliquots were restimulated acutely with antigen-presenting wells expressing WT or mutated PIK3CA and subject to single-cell RNA-seq and V(D)J immunoprofiling using the 10x genomics platform. All clonotypes associated with a mutation-specific activation signature were identified and their TCR gene sequences were retrieved. Candidate TCR gene sequences were retrovirally transferred to open-repertoire T cell to confirm mutation-specific recognition.

This repository contains the code that was developed to process and analyze combined single-cell RNA-seq and single-cell TCR-seq samples to:

1. associate the transcriptome information of individual cells with their corresponding TCR sequences (= clonotype), 
2. assign clonotype IDs that identify cells with the same clonotype across the two conditions (stimulated with (1) WT antigen or (2) with the tumor antigen),
3. identify the clonotype that shows the greatest increase of cytotoxic/effector function (based on expression of IFNg, IL-2, TNFa),
4. determine additional genes that are differentially expressed when comparing the cells of the MUT-antigen condition to the cells of the WT-antigen condition from the same clonotype.

The code deposited here was written by Friederike Dündar at the [Applied Bioinformatics Core](https://abc.med.cornell.edu) of Weill Cornell Medicine.
Don't hesitate to get in touch with questions either via the issues panel here or via `abc -at- med.cornell.edu`.
