---
title: "scHiCTools: a computational toolbox for analyzing single-cell Hi-C data"
authors:
- X Li
- F Feng
- H Pu
- W Leung
- __J Liu__
date: "2021-05-01T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2020-06-15T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "*PLOS Computational Biology*"
publication_short: ""

abstract: Single-cell Hi-C (scHi-C) sequencing technologies allow us to investigate three-dimensional chromatin organization at the single-cell level. However, we still need computational tools to deal with the sparsity of the contact maps from single cells and embed single cells in a lower-dimensional Euclidean space. This embedding helps us understand relationships between the cells in different dimensions such as cell-cycle dynamics and cell differentiation. Here, we present an open-source computational toolbox, scHiCTools, for analyzing single cell Hi-C data. The toolbox takes singlecell Hi-C data files as input, and projects single cells in a lower-dimensional Euclidean space. The toolbox includes three commonly used methods for smoothing scHi-C data (linear convolution, random walk, and network enhancing), three projection methods for embedding single cells (fastHiCRep, Selfish, and InnerProduct), three clustering methods for clustering cells (k-means, spectral clustering, and HiCluster) and a build-in function to visualize the cells embedding in a two-dimensional or three-dimensional plot. We benchmark the embedding performance and run time of these methods on a number of scHi-C datasets, and provide some suggestions for practice use. scHiCTools, based on Python3, can run on different platforms, including Linux, macOS, and Windows. Our software package is available at https://github.com/liu-bioinfo-lab/scHiCTools.

# Summary. An optional shortened abstract.
# summary: 

# tags:
# - Source Themes
featured: false

# links:
# - name: ""
#   url: ""
url_pdf: https://www.biorxiv.org/content/10.1101/769513v2.full.pdf
url_code: 'https://github.com/liu-bioinfo-lab/scHiCTools'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
#image:
#  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/jdD8gXaTZsc)'
#  focal_point: ""
#  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: ["hic-embedding"]

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
#slides: 
---
