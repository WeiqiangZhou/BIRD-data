## BIRD-data: a dataset for big data prediction

This is the preprocessed training dataset used for [BIRD(Big data Regression for predicting DNase I hypersensitivity)](https://github.com/WeiqiangZhou/BIRD). It contains two types of genomic data: chromatin accessibility (DNase-seq) and gene expression (Exon array).

This dataset can also be useful for testing other machine learning algorithms in the context of genomics. For more details about the prediction problems in genomics, please check the following papers:

Zhou W, Sherwood B, Ji Z, Xue Y, Du F, Bai J, Ying M, Ji H. Genome-wide Prediction of DNase I Hypersensitivity Using Gene Expression. _Nature Communications_ **8**, 1038 (2017). ([open access](https://www.nature.com/articles/s41467-017-01188-x))

Zhou W, Sherwood B, Ji H. Computational Prediction of the Global Functional Genomic Landscape: Applications, Methods, and Challenges. _Human Heredity_ **81**, 88-105 (2016). ([author manuscript](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5599299/pdf/nihms904916.pdf))

### Download the data
The data can be downloaded via the following link:

https://github.com/WeiqiangZhou/BIRD-data/releases/download/v1.0/BIRD_data.zip

### Chromatin accessibility data
To load the data, use the follow command in [R](https://www.r-project.org).
```
DNase_data <- readRDS("DNase_data_57_cells.rds")
```
The first three columns in the data contains the location information of a genomic locus (200bp window). For other columns, each column is a cell type and each row is a genomic locus. The value represents the normalized and log-transformed DNase-seq signal.

### Gene expression data
To load the data, use the following command:
```
Exon_data <- readRDS("Exon_data_57_cells.rds")
```
The rownames of the data contains the "transcript cluster id" of each gene in the exon array data. For the annotation of these genes and ids, please check the [annotation data](http://www.affymetrix.com/Auth/analysis/downloads/na33/wtexon/HuEx-1_0-st-v2.na33.1.hg19.probeset.csv.zip). Each column is a cell type and each row is a gene. The value represents the quantile normalized and log transformed gene expression.

### The prediction problem
Let the chromatin accessibility data be Y and the gene expression data be X. The problem can be formulated as how to predict Y using X.

### Other files in the dataset
There are three other txt files in the dataset ("DH_cluster_1000.txt", "DH_cluster_2000.txt", and "DH_cluster_5000.txt"). These files contain the membership of the clustering result for the genomic loci (rows) using 1000, 2000, or 5000 clusters based on the chromatin accessibility data (Y). 

### Citations
The raw data for this dataset is obtained from ENCODE and processed as described in BIRD. Please cite the [ENCODE paper](https://www.nature.com/articles/nature11247) and the [BIRD paper](https://www.nature.com/articles/s41467-017-01188-x) if you used this dataset.

ENCODE Project Consortium. An integrated encyclopedia of DNA elements in the human genome. _Nature_ **489**, 57–74 (2012). ([open access](https://www.nature.com/articles/nature11247))

Zhou W, Sherwood B, Ji Z, Xue Y, Du F, Bai J, Ying M, Ji H. Genome-wide Prediction of DNase I Hypersensitivity Using Gene Expression. _Nature Communications_ **8**, 1038 (2017). ([open access](https://www.nature.com/articles/s41467-017-01188-x))





