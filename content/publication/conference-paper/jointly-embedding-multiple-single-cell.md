+++
title = "Jointly embedding multiple single-cell omics measurements"
date = "2019-06-01"

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["__J Liu__", "__Y Huang__", "R Singh", "J Vert", "W Noble"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference proceedings
# 2 = Journal
# 3 = Work in progress
# 4 = Technical report
# 5 = Book
# 6 = Book chapter
publication_types = ["1"]

# Publication name and optional abbreviated version.
publication = "The Workshop on Algorithms in Bioinformatics"
publication_short = "WABI"

# Abstract and optional shortened version.
abstract = "Many single-cell sequencing technologies are now available, but it is still difficult to apply multiple sequencing technologies to the same single cell. In this paper, we propose an unsupervised manifold alignment algorithm, MMD-MA, for integrating multiple measurements carried out on disjoint aliquots of a given population of cells. Effectively, MMD-MA performs an in silico co-assay by embedding cells measured in different ways into a learned latent space. In the MMD-MA algorithm, single-cell data points from multiple domains are aligned by optimizing an objective function with three components: (1) a maximum mean discrepancy (MMD) term to encourage the differently measured points to have similar distributions in the latent space, (2) a distortion term to preserve the structure of the data between the input space and the latent space, and (3) a penalty term to avoid collapse to a trivial solution. Notably, MMD-MA does not require any correspondence information across data modalities, either between the cells or between the features. Furthermore, MMD-MA’s weak distributional requirements for the domains to be aligned allow the algorithm to integrate heterogeneous types of single cell measures, such as gene expression, DNA accessibility, chromatin organization, methylation, and imaging data. We demonstrate the utility of MMD-MA in simulation experiments and using a real data set involving single-cell gene expression and methylation data."

# Summary. An optional shortened abstract.
summary = ""

# Digital Object Identifier (DOI)
doi = ""

# Is this a selected publication? (true/false)
featured = true

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
projects = ["single-cell-multi-omics-integration"]

# Links (optional).
url_PDF = "files/mmd-ma.pdf"
url_code = "https://noble.gs.washington.edu/proj/mmd-ma/"


# Does the content use math formatting?
math = true

# Does the content use source code highlighting?
highlight = true

+++

