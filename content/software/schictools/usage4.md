---
title: Clustering
linktitle: Clustering
toc: true
type: docs
date: "2019-05-05T00:00:00+01:00"
draft: false
menu:
  schictools:
    parent: Usage
    weight: 4

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 7
---

There are two functions to cluster cells.

  ```console
  >>>label=loaded_data.clustering(
  ... n_clusters=4, clustering_method='kmeans', similarity_method='innerproduct',
  ... aggregation='median', n_strata=None
  ... )
  ```

  `clustering` function returns a numpy array of cell labels clustered.

  - n_clusters (int): Number of clusters.

  - clustering_method (str):
    Clustering method in 'kmeans', 'spectral_clustering' or 'HAC'(hierarchical agglomerative clustering).

  - similarity_method (str):
    Reproducibility measure.
    Value in ‘InnerProduct’, ‘HiCRep’ or ‘Selfish’.

  - aggregation (str):
    Method to aggregate different chromosomes.
    Value is either 'mean' or 'median'.
    Default: 'median'.

  - n_strata (int or None):
    Only consider contacts within this genomic distance.
    If it is None, it will use the all strata kept (the argument keep_n_strata) from previous loading process. Default: None.

  - print_time (bool):
    Whether to print the processing time. Default: False.


  ```console
  >>>hicluster=loaded_data.scHiCluster(dim=2,cutoff=0.8,n_PCs=10,k=4)
  ```

  `scHiCluster` function returns two componments.
  First componment is a numpy array of embedding of cells using HiCluster.
  Second componment is a numpy of cell labels clustered by HiCluster.

  - dim (int): Number of dimension of embedding. Default: 2.

  - cutoff (float): The cutoff proportion to convert the real contact matrix into binary matrix. Default: 0.8.

  - n_PCs (int): Number of principal components. Default: 10.

  - k (int): Number of clusters. Default: 4.
