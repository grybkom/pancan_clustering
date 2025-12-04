# pancan_clustering
Clustering models for the classification of five types of cancerous tissues based on RNA sequencing data.

## Introduction
This project uses clustering algorithms to classify five classes of cancerous tissues based on RNA sequencing (RNA-seq) data. Cancer begins when cell differentiation becomes unregulated and cells begin growing out of control (National Cancer Institute, 2021). This process has well established genomic origins (Weinstein et al., 2013). There are numerous types of cancer and cancer can originate in almost any tissue type (National Cancer Institute, 2021). By analyzing RNA-seq data from different cancer types, The Cancer Genome Atlas Pan-Cancer Analysis Project aims to identify the genomic changes that are associated with cancer to gain a better understanding of cancer’s molecular underpinnings (Weinstein et al., 2013). Labels were added to clustering results from hierarchical and K-means models and results were compared. Hierarchical clustering did very well, achieving an accuracy of over 99%, and outperformed K-means clustering after PCA dimensionality reduction.

## Data

### Access
The original data set (large) is maintained by The Cancer Genome Atlas Pan-Cancer Analysis Project and is hosted at:
https://www.synapse.org/#!Synapse:syn4301332

The truncated dataset used in this project is hosted at UC Irvine Machine Learning Repository:
https://archive.ics.uci.edu/dataset/401/gene+expression+cancer+rna+seq

### Description
- The data contains RNA-seq data from five types of cancerous tissue; BRCA, KIRC, COAD, LUAD and PRAD 
  - BRCA - Breast invasive carcinoma
  - KIRC - Kidney renal clear cell carcinoma
  - COAD - Colon adenocarcinoma
  - LUAD - Lung adenocarcinoma
  - PRAD - Prostate adenocarcinoma

- The dataset is comprised of 800 samples and 20,530 genes.

- The raw data appear to be already log plus 1 transformed. 

![gene_max_min_ave_distributions](https://github.com/user-attachments/assets/041efbb6-7999-439c-b7a4-efdcdc4a7db3)

![percent_zero_expression](https://github.com/user-attachments/assets/65062908-7cec-496b-9134-300295cc6938)

## Results

### PCA

![pca_explained_variance](https://github.com/user-attachments/assets/f2cb4523-349e-4c8e-aeb1-370f6f90c6bf)

### K-means Clustering with PCA Dimensionality Reduction
![optimal_pca_dims_kmeans](https://github.com/user-attachments/assets/759dab33-d061-4cdf-b82b-6e066cc824cd)
![confusion_matrix_pca_kmeans_clustering](https://github.com/user-attachments/assets/be3e221e-329a-4fb7-bc27-d152cdb826e8)

### Hierarchical Clustering 
![confusion_matrix_agg_clustering](https://github.com/user-attachments/assets/e9f5a23d-3d75-420d-9d03-40980ca72a99)

## References
National Cancer Institute. (2021, October 11). What is cancer? Cancer.gov. https://www.cancer.gov/about-cancer/understanding/what-is-cancer

Weinstein, J. N., Collisson, E. A., Mills, G. B., Shaw, K. R. M., Ozenberger, B. A., Ellrott, K., Shmulevich, I., Sander, C., & Stuart, J. M. (2013). The Cancer Genome Atlas Pan-Cancer analysis project. Nature Genetics, 45(10), 1113–1120. https://doi.org/10.1038/ng.2764
