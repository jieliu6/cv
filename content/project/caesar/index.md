+++
#Date this page was created.
date = "2021-04-19"

# Project title.
title = "CAESAR"

# Project summary to display on homepage.
summary = "A deep learning model for connecting high-resolution 3D chromatin organization with epigenomics."

# Tags: can be used for filtering projects.
# Example: tags = ["machine-learning", "deep-learning"]
tags = ["predictive-models", "4d-nucleome", "machine-learning"]

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
The resolution of chromatin conformation capture technologies keeps increasing, and the recent nucleosome resolution chromatin contact maps allow us to explore how fine-scale 3D chromatin organization is related to epigenomic states in human cells. Using publicly available Micro-C datasets, we develop a deep learning model, CAESAR, to learn a mapping function from epigenomic features to 3D chromatin organization. The model accurately predicts fine-scale structures, such as short-range chromatin loops and stripes, that Hi-C fails to detect. With existing epigenomic datasets from ENCODE and Roadmap Epigenomics Project, we successfully impute high-resolution 3D chromatin contact maps for 91 human tissues and cell lines. In the imputed high-resolution contact maps, we identify the spatial interactions between genes and their experimentally validated regulatory elements, demonstrating CAESAR’s potential in coupling transcriptional regulation with 3D chromatin organization at high resolution.

Web Portal: https://nucleome.dcmb.med.umich.edu/caesar/

Source Code: https://github.com/liu-bioinfo-lab/caesar