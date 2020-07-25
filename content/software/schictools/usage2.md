---
title: Load Data
linktitle: Load Data
toc: true
type: docs
date: "2019-05-05T00:00:00+01:00"
draft: false
menu:
  schictools:
    parent: Usage
    weight: 2

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 5
---

## Import Package
  ```console
  >>>import scHiCTools
  ```

## Load scHiC data

  The scHiC data is stored in a series of files, with each of the files corresponding to one cell.
  You need to specify the list of scHiC file paths.

  Only intra-chromosomal interactions are counted.
  ```console
  >>>from scHiCTools import scHiCs
  >>>files = ['./cell_1', './cell_2', './cell_3']
  >>>loaded_data = scHiCs(
  ... files, reference_genome='mm9',
  ... resolution=500000, keep_n_strata=10,
  ... format='customized', adjust_resolution=True,
  ... customized_format=12345, header=0, chromosomes='except Y',
  ... operations=['OE_norm', 'convolution']
  ... )
  ```
  - reference genome (dict or str): now supporting 'mm9', 'mm10', 'hg19', 'hg38'.
  If your reference genome is not in ['mm9', 'mm10', 'hg19', 'hg38'], you need to provide the lengths of chromosomes
  you are going to use with a Python dict. e.g. {'chr1': 150000000, 'chr2': 130000000, 'chr3': 200000000}
  - resolution (int): the resolution to separate genome into bins.
  If using .hic file format, the given resolution must match with the resolutions in .hic file.
  - keep_n_strata (None or int): only store contacts within n strata near the diagonal. Default: 10.
  If 'None', it will not store strata
  - store_full_map (bool): whether store full contact maps in numpy matrices or
  scipy sparse matrices，If False, it will save memory.
  - sparse (bool): whether to use sparse matrices
  - format (str): file format, supported formats: 'shortest', 'shortest_score', 'short',
  'short_score' , 'medium', 'long', '4DN', '.hic', '.mcool', 'npy', 'npz', 'matrix',
  'HiCRep', 'matrix_txt' and 'customized'. Default: 'customized'.
  - customized_format (int or str or list): the column indices in the order of
  "chromosome 1 - position 1 - chromosome 2 - position 2 - contact reads" or
  "chromosome 1 - position 1 - chromosome 2 - position 2" or
  "chromosome 1 - position 1 - chromosome 2 - position 2 - map quality 1 - map quality 2".
  e.g. if the line is "chr1 5000000 chr2 3500000 2", the format should be '12345' or [1, 2, 3, 4, 5]; if there is no column
  indicating number of reads, you can just provide 4 numbers like '1234', and contact read will be set as 1.
  Default: '12345'.
  - adjust_resolution: whether to adjust resolution for the input file.
  Sometimes the input file is already in the proper resolution (e.g. position 3000000 has already been changed to 6 with 500kb resolution).
  For this situation you can set adjust_resolution=False. Default: True.
  - map_filter (float): keep all contacts with mapq higher than this threshold. Default: 0.0
  - header (int): how many header lines does the file have. Default: 0.
  - chromosomes (list or str): chromosomes to use, eg. ['chr1', 'chr2'], or
  just 'except Y', 'except XY', 'all'.
  Default: 'all', which means chr 1-19 + XY for mouse and chr 1-22 + XY for human.
  - operations (list or None): the operations use for pre-processing or smoothing the maps given in a list.
  The operations will happen in the given order.
  Supported operations: 'logarithm', 'power', 'convolution', 'random_walk',
  'network_enhancing', 'OE_norm', 'VC_norm', 'VC_SQRT_norm', 'KR_norm'。
  Default: None.
  - For preprocessing and smoothing operations, sometimes you need additional arguments
  (introduced in next sub-section).

  You can also skip pre-processing and smoothing in loading step (operations=None),
  and do them in next lines.

## Plot number of contacts and select cells

  You can plot the number of contacts of your cells.
  ```console
  >>>loaded_data.plot_contacts(hist=True, percent=True)
  ```
  If hist is `True`, plot Histogram of the number of contacts. If percent is `True`, plot the scatter plot of cells with  of short-range contacts (< 2 Mb) versus contacts at the mitotic band (2-12 Mb).

  You can select cells based on number of contacts:
  ```console
  >>>loaded_data.select_cells(min_n_contacts=10000,max_short_range_contact=0.99)
  ```
  The above command select cells have number of contacts bigger than 10000 and percent of short range contacts small than .99.

## Pre-processing and Smoothing Operations
  Stand alone pre-processing and smoothing:
  ```console
  >>>loaded_data.processing(['random_walk', 'network_enhancing'])
  ```
  If you didn't store full map (i.e. store_full_map=False), processing is not
  doable in a separate step.

  - logarithm:
  new_W_ij = log_(base) (W_ij + epsilon). Additional arguments:
    - log_base: default: e
    - epsilon: default: 1
  - power: new_W_ij = (W_ij)^pow. Additional argument:
    - pow: default: 0.5 (i.e., sqrt(W_ij))

  - VC_norm: VC normalization - each value divided by the sum of
  corresponding row then divided by the sum of corresponding column
  - VC_SQRT_norm: VC_SQRT normalization - each value divided by the sqrt of the sum
  of corresponding row then divided by the sqrt of the sum of corresponding column
  - KR_norm: KR normalization - iterating until the sum of each row / column is one
  Argument:
    - maximum_error_rate (float): iteration ends when max error is smaller
    than (maximum_error_rate). Default: 1e-4
  - OE_norm: OE normalization -  each value divided by the average of its
  corresponding strata (diagonal line)

  - convolution: smoothing with a N by N convolution kernel, with each value equal to 1/N^2.
  Argument:
    - kernel_shape: an integer. e.g. kernel_shape=3 means a 3*3 matrix with each value = 1/9. Default: 3.
  - Random walk: multiply by a transition matrix (also calculated from contact map itself).
  Argument:
    - random_walk_ratio: a value between 0 and 1, e.g. if ratio=0.9, the result will be
    0.9 * matrix_after_random_walk + 0.1 * original_matrix. Default: 1.0.
  - Network enhancing: transition matrix only comes from k-nearest neighbors of each line.
  Arguments:
    - kNN: value 'k' in kNN. Default: 20.
    - iterations: number of iterations for network enhancing. Default: 1
    - alpha: similar with random_walk_ratio. Default: 0.9