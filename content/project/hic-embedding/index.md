+++
#Date this page was created.
date = "2019-01-01"

# Project title.
title = "scHi-C embedding"

# Project summary to display on homepage.
summary = "The first computational embedding method for single cells in terms of their chromatin organization. "

# Tags: can be used for filtering projects.
# Example: tags = ["machine-learning", "deep-learning"]
tags = ["4d-nucleome", "machine-learning"]

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
Single-cell Hi-C (scHi-C) data promises to enable scientists to interrogate the 3D architecture of DNA in the nucleus of the cell, studying how this structure varies stochastically or along developmental or cell cycle axes.  However, Hi-C data analysis requires methods that take into account the unique characteristics of this type of data.  In this work, we explore whether methods that have been developed previously for the analysis of bulk Hi-C data can be applied to scHi-C data.  We apply methods designed for analysis of bulk Hi-C data to scHi-C data in conjunction with unsupervised embedding.  We find that one of these methods, HiCRep, when used in conjunction with multidimensional scaling (MDS), strongly outperforms three other methods, including a technique that has been used previously for scHi-C analysis.  We also provide evidence that the HiCRep/MDS method is robust to extremely low per-cell sequencing depth, that this robustness is improved even further when high-coverage and low-coverage cells are projected together, and that the method can be used to jointly embed cells from multiple published datasets.