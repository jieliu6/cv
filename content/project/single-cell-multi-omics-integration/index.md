+++
#Date this page was created.
date = "2019-06-01"

# Project title.
title = "single-cell multi-omics integration"

# Project summary to display on homepage.
summary = "An unsupervised manifold alignment algorithm, MMD-MA, for integrating multiple measurements carried out on disjoint aliquots of a given population of single cells."

# Tags: can be used for filtering projects.
# Example: tags = ["machine-learning", "deep-learning"]
tags = ["machine-learning"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Featured image
# To use, add an image named featured.jpg/png to your project's folder.
[image] 
 preview_only = true

# Caption (optional)
caption = ""

# Focal point (optional)
# Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
focal_point = "Smart"

+++
Many single-cell sequencing technologies are now available, but it is still difficult to apply multiple sequencing technologies to the same single cell. In this paper, we propose an unsupervised manifold alignment algorithm, MMD-MA, for integrating multiple measurements carried out on disjoint aliquots of a given population of cells. Effectively, MMD-MA performs an in silico co-assay by embedding cells measured in different ways into a learned latent space. In the MMD-MA algorithm, single-cell data points from multiple domains are aligned by optimizing an objective function with three components: (1) a maximum mean discrepancy (MMD) term to encourage the differently measured points to have similar distributions in the latent space, (2) a distortion term to preserve the structure of the data between the input space and the latent space, and (3) a penalty term to avoid collapse to a trivial solution. Notably, MMD-MA does not require any correspondence information across data modalities, either between the cells or between the features. Furthermore, MMD-MA's weak distributional requirements for the domains to be aligned allow the algorithm to integrate heterogeneous types of single cell measures, such as gene expression, DNA accessibility, chromatin organization, methylation, and imaging data. We demonstrate the utility of MMD-MA in simulation experiments and using a real data set involving single-cell gene expression and methylation data.