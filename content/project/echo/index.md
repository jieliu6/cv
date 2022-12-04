+++
#Date this page was created.
date = "2022-06-06"

# Project title.
title = "ECHO"

# Project summary to display on homepage.
summary = "A deep learning model for characterizing collaborative transcription regulation."

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
Human epigenome and transcription activities have been characterized by a number of sequence-based deep learning approaches which only utilize the DNA sequences. However, transcription factors interact with each other, and their collaborative regulatory activities go beyond the linear DNA sequence. Therefore leveraging the informative 3D chromatin organization to investigate the collaborations among transcription factors is critical. We developed ECHO, a graph-based neural network, to predict chromatin features and characterize the collaboration among them by incorporating 3D chromatin organization from 200-bp high-resolution Micro-C contact maps. ECHO predicted 2,583 chromatin features with significantly higher average AUROC and AUPR than the best sequence-based model. We observed that chromatin contacts of different distances affected different types of chromatin features' prediction in diverse ways, suggesting complex and divergent collaborative regulatory mechanisms. Moreover, ECHO was interpretable via gradient-based attribution methods. The attributions on chromatin contacts identify important contacts relevant to chromatin features. The attributions on DNA sequences identify TF binding motifs and TF collaborative binding. Furthermore, combining the attributions on contacts and sequences reveals important sequence patterns in the neighborhood which are relevant to a target sequence's chromatin feature prediction.