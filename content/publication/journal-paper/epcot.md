---
title: "A generalizable framework to comprehensively predict epigenome, chromatin organization, and transcriptome"
authors:
- __Z Zhang__
- __F Fang__
- __Y Qiu__
- __J Liu__
date: "2023-05-31T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2023-05-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "Nucleic Acids Research"
publication_short: "Nucleic Acids Res"

abstract: Many deep learning approaches have been proposed to predict epigenetic profiles, chromatin organization, and transcription activity. While these approaches achieve satisfactory performance in predicting one modality from another, the learned representations are not generalizable across predictive tasks or across cell types. In this paper, we propose a deep learning approach named EPCOT which employs a pre-training and fine-tuning framework, and comprehensively predicts epigenome, chromatin organization, transcriptome, and enhancer activity in one framework. EPCOT is the first framework proposed to predict all of these genomic modalities and performs well in individual modality prediction, which is also generalizable to new cell and tissue types. EPCOT also maps from DNA sequence and chromatin accessibility profiles to generic representations which are generalizable across different modalities. Interpreting EPCOT model also provides biological insights including mapping between different genomic modalities, identifying TF sequence binding patterns, and analyzing cell-type specific TF impacts on enhancer activity.

# Summary. An optional shortened abstract.
# summary: 

# tags:
# - Source Themes
featured: false

# links:
# - name: ""
#   url: ""
url_pdf: https://www.biorxiv.org/content/10.1101/2022.05.23.493129v2
url_code: 'https://github.com/liu-bioinfo-lab/EPCOT'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''


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
projects: ['epcot']

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
#slides: 
---
