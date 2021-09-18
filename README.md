# Diet-induced alterations of small intestinal function
This repository contains scripts to reproduce the results of the single-cell data from:
A. Aliluev, S. Tritschler et al., "Diet-induced alteration of intestinal stem cell function underlies obesity and prediabetes in mice", Nature Metabolism, 2021
doi: 10.1038/s42255-021-00458-9


The notebooks contain code for the following analyses:

scRNA-seq of intestinal crypt cells:  
- _Preprocessing.ipynb_ --> QC, preprocessing, batch correction, ambient gene identification (input data are raw count matrices)  
- _Manifold_clustering.ipynb_ --> Manifold, clustering and annotation steps (input data are preprocessed, filtered and annotated count matrices)  
- _Analyses_Figure1_S1_S2.ipynb, Analyses_Figure3_S7.ipynb, Analyses_Figure4_S8.ipynb, Analyses_Figure5_S9.ipynb, Differential_expression_limma.ipynb_ --> main analyses to reproduce results and plots of the manuscript (input data are preprocessed, filtered and annotated count matrices)  
- Analyses_Figure4_RNAvelocity.ipynb --> RNA velocity estimation of EE lineage (input data are preprocessed, filtered and annotated count matrices and bam files to extract splicing information)  

scRNA-seq of intestinal villi:  
- Preprocessing_manifold_clustering_villus.ipynb --> QC, preprocessing, manifold, clustering and annotation steps (input data are raw count matrices)  
- Analyses_villus.ipynb --> main analyses to reproduce results and plots of the manuscript (input data are preprocessed, filtered and annotated count matrices)  


The data has been deposited in GEO under accession number GSE147319. The raw count matrices as well as preprocessed, filtered and annotated count matrices are provided as supplementary file as an Anndata object (h5ad-file) for crypt and villi data.

For further exploration load the processed h5ad-files into a cellxgene browser for visualization or into a python-session for additional analyses using scanpy.

Note that most of the analysis was done with scanpy v1.0.4. Some functions have changed in newer versions of scanpy. For other package versions please consult the notebook or the methods in the supplementary information of the manuscript. Numeric results can vary depending on package versions and e.g. affect clustering.

If the materials in this repo are of use to you, please consider citing the above publication.

If you have any questions about the data or analysis feel free to contact us. :)