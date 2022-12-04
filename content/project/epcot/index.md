+++
#Date this page was created.
date = "2021-09-14"

# Project title.
title = "EPCOT"

# Project summary to display on homepage.
summary = "A generalizable framework to comprehensively predict epigenome, chromatin organization, and transcriptome."

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
Many deep learning approaches have been proposed to predict epigenetic profiles, chromatin organization, and transcription activity. While these approaches achieve satisfactory performance in predicting one modality from another, the learned representations are not generalizable across predictive tasks or across cell types. In this paper, we propose a deep learning approach named EPCOT which employs a pre-training and fine-tuning framework, and comprehensively predicts epigenome, chromatin organization, transcriptome, and enhancer activity in one framework. EPCOT is the first framework proposed to predict all of these genomic modalities and performs well in individual modality prediction, which is also generalizable to new cell and tissue types. EPCOT also maps from DNA sequence and chromatin accessibility profiles to generic representations which are generalizable across different modalities. Interpreting EPCOT model also provides biological insights including mapping between different genomic modalities, identifying TF sequence binding patterns, and analyzing cell-type specific TF impacts on enhancer activity.