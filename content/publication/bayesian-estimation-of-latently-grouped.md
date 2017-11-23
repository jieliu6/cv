+++
title = "Bayesian Estimation of Latently-grouped Parameters in Undirected Graphical Models"
date = "2013-12-01"

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["__J Liu__", "D Page"]

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
publication = "In *Advances in Neural Information Processing Systems*"
publication_short = "In *NIPS*"

# Abstract and optional shortened version.
abstract = "In large-scale applications of undirected graphical models, such as social networks and biological networks, similar patterns occur frequently and give rise to similar parameters. In this situation, it is beneficial to group the parameters for more efficient learning. We show that even when the grouping is unknown, we can infer these parameter groups during learning via a Bayesian approach. We impose a Dirichlet process prior on the parameters. Posterior inference usually involves calculating intractable terms, and we propose two approximation algorithms, namely a Metropolis-Hastings algorithm with auxiliary variables and a Gibbs sampling algorithm with “stripped” Beta approximation (Gibbs SBA). Simulations show that both algorithms outperform conventional maximum likelihood estimation (MLE). Gibbs SBA’s performance is close to Gibbs sampling with exact likelihood calculation. Models learned with Gibbs SBA also generalize better than the models learned by MLE on real-world Senate voting data."

# Featured image thumbnail (optional)
image_preview = ""

# Is this a selected publication? (true/false)
selected = false

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
projects = ["graphical_model_learning"]

# Links (optional).
url_pdf = "https://papers.nips.cc/paper/4961-bayesian-estimation-of-latently-grouped-parameters-in-undirected-graphical-models.pdf"

# Does the content use math formatting?
math = true

# Does the content use source code highlighting?
highlight = true

+++

