---
title: Learn Embedding
linktitle: Embedding
toc: true
type: docs
date: "2019-05-05T00:00:00+01:00"
draft: false
menu:
  schictools:
    parent: Usage
    weight: 3

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 6
---

```console
  >>>embs = loaded_data.learn_embedding(
  ... dim=2, similarity_method='inner_product', embedding_method='MDS',
  ... n_strata=None, aggregation='median', return_distance=False
  ... )
  ```
  This function will return the embeddings in the format of a numpy array with shape ( # of cells, # of dimensions).
  - dim (int): the dimension for the embedding
  - similarity_method (str): reproducibility measure, 'InnerProduct', 'HiCRep' or
  'Selfish'. Default: 'InnerProduct'
  - embedding_method (str): 'MDS', 'tSNE' or 'UMAP'
  - n_strata (int): only consider contacts within this genomic distance. Default: None.
  If it is None, it will use the all strata kept (the argument keep_n_strata from
  previous loading process). Thus n_strata and keep_n_strata (loading step) cannot be
  None at the same time.
  - aggregation (str): method to aggregate different chromosomes,
  'mean' or 'median'. Default: 'median'.
  - return_distance (bool): if True, return (embeddings, distance_matrix); if False, only return embeddings. Default: False.
  - Some additional argument for Selfish:
    - n_windows (int): split contact map into n windows, default: 10
    - sigma (float): sigma in the Gaussian-like kernel: default: 1.6
