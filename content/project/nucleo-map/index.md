+++
#Date this page was created.
date = "2022-07-14"

# Project title.
title = "NucleoMap"

# Project summary to display on homepage.
summary = "A computational tool for identifying nucleosomes in ultra-high resolution contact maps."

# Tags: can be used for filtering projects.
# Example: tags = ["machine-learning", "deep-learning"]
tags = ["4d-nucleome"]

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
Although poorly positioned nucleosomes are ubiquitous in the eukaryotic genome, they are difficult to identify with existing nucleosome identification methods. Recently available enhanced high-throughput chromatin conformation capture techniques such as Micro-C, DNase Hi-C, and Hi-CO characterize nucleosome-level chromatin proximity, probing the positions of mono-nucleosomes and the spacing between nucleosome pairs at the same time, enabling nucleosome profiling in poorly positioned regions. Here we develop a novel computational approach, NucleoMap, to identify nucleosome positioning from ultra-high resolution chromatin contact maps. By integrating nucleosome read density, contact distances, and binding preferences, NucleoMap precisely locates nucleosomes in both prokaryotic and eukaryotic genomes and outperforms existing nucleosome identification methods in both precision and recall. We rigorously characterize genome-wide association in eukaryotes between the spatial organization of mono-nucleosomes and their corresponding histone modifications, protein binding activities, and higher-order chromatin functions. We also find evidence of two tetra-nucleosome folding structures in human embryonic stem cells and analyze their association with multiple structural and functional regions. Based on the identified nucleosomes, nucleosome contact maps are constructed, reflecting the inter-nucleosome distances and preserving the contact distance profiles in original contact maps.