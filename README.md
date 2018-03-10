## BIRD-data:a dataset for big data prediction

This is the training dataset used for [BIRD(Big data Regression for predicting DNase I hypersensitivity)](https://github.com/WeiqiangZhou/BIRD). It contains two types of genomic data: chromatin accessibility (DNase-seq) and gene expression (Exon array). 

This dataset can also be useful for testing other machine learning algorithms in the context of genomics. For more details about the introduction of prediction problems in genomics, please check the following papers:

Zhou W, Sherwood B, Ji Z, Xue Y, Du F, Bai J, Ying M, Ji H. Genome-wide Prediction of DNase I Hypersensitivity Using Gene Expression. _Nature Communications_ 8, 1038 (2017). ([open access](https://www.nature.com/articles/s41467-017-01188-x))

Zhou W, Sherwood B, Ji H. Computational Prediction of the Global Functional Genomic Landscape: Applications, Methods, and Challenges. _Human Heredity_ 81, 88-105 (2017). ([Author manuscript](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5599299/pdf/nihms904916.pdf))

### Download the data
The data can be downloaded via the following link:


### Chromatin accessibility data
To load the data, use the follow command in [R](https://www.r-project.org).
```
DNase_data <- readRDS("DNase_data_57_cells.rds")

