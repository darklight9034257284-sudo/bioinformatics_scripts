# PCA on Gene Expression Data (Breast Cancer)

## Introduction

Principal Component Analysis (PCA) is a dimensionality reduction technique used to simplify high-dimensional data while preserving important patterns. In bioinformatics, PCA helps identify patterns in gene expression data.

## Objective

To analyze gene expression data of breast cancer patients and:

* Visualize expression of XBP1 and GATA3 genes
* Observe separation between ER+ and ER- cancer types
* Apply PCA and project the data onto the first principal component (PC1)

## Dataset

* GEO ID: GSE5325
* 105 patient samples
* Gene expression values for thousands of genes
* Labels:

  * 1 → ER+ breast cancer
  * 0 → ER- breast cancer

## Methodology

### 1. Data Loading

* Loaded gene expression dataset
* Cleaned column names to remove extra spaces

### 2. Gene Selection

* Extracted expression values for:

  * XBP1 (Gene ID: 4404)
  * GATA3 (Gene ID: 2625)

### 3. Visualization (Figure 1a)

* Scatter plot created:

  * X-axis → GATA3
  * Y-axis → XBP1
* Colored by class:

  * Red → ER+
  * Blue → ER-

### 4. PCA (Figure 1c)

* Applied PCA on full dataset
* Reduced data to 1 dimension (PC1)
* Plotted projection of all samples

## Results

* Scatter plot shows partial separation between ER+ and ER- samples
* PCA projection preserves this separation in reduced dimension
* Confirms that gene expression patterns can distinguish cancer types

## Conclusion

PCA effectively reduces dimensionality while retaining meaningful biological patterns. Gene expression analysis using PCA can help classify disease subtypes.

## Tools Used

* Python
* Pandas
* Matplotlib
* Scikit-learn
