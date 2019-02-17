+++
title = "Multiple Testing under Dependence via Graphical Models"
date = "2016-09-01"

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["__J Liu__", "C Zhang", "D Page"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference proceedings
# 2 = Journal
# 3 = Work in progress
# 4 = Technical report
# 5 = Book
# 6 = Book chapter
publication_types = ["2"]

# Publication name and optional abbreviated version.
publication = "In *The Annals of Applied Statistics*"
publication_short = "In *Annals of Applied Statistics*"

# Abstract and optional shortened version.
abstract = "Large-scale multiple testing tasks often exhibit dependence. Leveraging the dependence between individual tests is still one challenging and important problem in statistics. With recent advances in graphical models, it is feasible to use them to capture the dependence among multiple hypotheses. We propose a multiple testing procedure which is based on a Markov-random-field-coupled mixture model. The underlying true states of hypotheses are represented by a latent binary Markov random field, and the observed test statistics appear as the coupled mixture variables. The model can be learned by a novel EM algorithm. The next step is to infer the posterior probability that each hypothesis is null (termed local index of significance), and the false discovery rate can be controlled accordingly. We also provide a semiparametric variation of the graphical model which is useful in the situation where $f_1$ (the density function of the test statistic under the alternative hypothesis) is heterogeneous among multiple hypotheses. This semiparametric approach exactly generalizes the local FDR procedure [J. Amer. Statist. Assoc. 96 (2001) 1151–1160] and connects with the BH procedure [J. Roy. Statist. Soc. Ser. B 57 (1995) 289–300]. Simulations show that the numerical performance of multiple testing can be improved substantially by using our procedure. We apply the procedure to a real-world genome-wide association study on breast cancer, and we identify several SNPs with strong association evidence."
abstract_short = ""

# Summary. An optional shortened abstract.
summary = ""

# Digital Object Identifier (DOI)
doi = ""

# Is this a featured publication? (true/false)
feature = false

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
projects = ["multiple-testing"]

# Links (optional).
url_pdf = "files/AOAS16_liu.pdf"
url_preprint = ""
url_code = ""
url_dataset = ""
url_project = ""
url_slides = ""
url_video = ""
url_poster = ""
url_source = ""
url_custom = [{name = "Multiple Testing", url = "https://en.wikipedia.org/wiki/Multiple_comparisons_problem"}, {name = "Graphic Model", url = "https://en.wikipedia.org/wiki/Graphical_model"}, {name = "GWAS", url = "https://en.wikipedia.org/wiki/Genome-wide_association_study"}]

# Does the content use math formatting?
math = true

# Does the content use source code highlighting?
highlight = true

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = ""
caption = ""

+++

More detail can easily be written here using *Markdown* and $\rm \LaTeX$ math code.
