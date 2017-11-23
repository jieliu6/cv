+++
# Date this page was created.
date = "2016-04-27"

# Project title.
title = "Personalized Breast Cancer Diagnosis"

# Project summary to display on homepage.
summary = "Our results show that radiologists can potentially use genetic variants (SNPs) to improve personalized breast cancer diagnosis."

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "radiogenomics_result1.jpg"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["precision-medicine"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false

+++

High hopes for using genetic profiling for personalized medicine have been, in part, driven by the rapid progress of genome-wide association studies, which continue identifying more common genetic variants associated with diseases with high population prevalence. In particular, the recent Collaborative Oncological Gene-environment Study (COGS), which pooled large quantities of genetic data via a massive international collaboration, more than doubled the number of known susceptibility loci that are associated to common cancers (breast, ovarian and prostate cancers). For breast cancer, over 130 institutions have collaborated and identified 41 new breast cancer associated variants. One way these genetic variants could be used in clinical breast cancer care is in individualized screening recommendations and personalized diagnosis. Early attempts to incorporate genetic variants into breast cancer risk models revealed modest improvements in risk prediction accuracy. For example, adding seven SNPs to the Gail model only increased the area under the ROC curve (AUROC) from 0.607 to 0.632 (Gail 2008, 2009). When ten SNPs were added to the Gail model, the AUROC increased from 0.580 to 0.618 on another dataset (Wacholder et al 2010). Incorporating these genetic variants with the mammographic findings to assess individualized risk will be highly relevant to clinical breast cancer diagnosis. 

We incorporated the genetic variants and consolidated a list of 77 SNPs which reflect the state of the art of breast cancer GWAS. We used the descriptors that radiologists observe on mammograms using the standardized lexicon in breast imaging, the Breast Imaging Reporting and Data System (BI-RADS). These mammography features included the shape and the margin of masses, the shape and the distribution of microcalcifications, background breast density and other associated findings. We built naïve Bayes models, using the 49 mammography features together with the 77 genetic variants (Combined-77 model). We observed that the inclusion of the genetic variants significantly improved the breast cancer diagnostic model. We discovered that the mammographic findings were more predictive for high-risk women, whereas the genetic variants were more predictive for low-risk women, which demonstrated the potential benefit of combining genetic variants and mammographic findings for personalized breast cancer diagnosis.

<img src="../../img/radiogenomics_result1.jpg">
<img src="../../img/radiogenomics_result2.jpg">