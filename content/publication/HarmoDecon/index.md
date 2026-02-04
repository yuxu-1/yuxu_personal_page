---
title: 'Mitigation of Multi-scale Biases in Cell-type Deconvolution for Spatially Resolved Transcriptomics Using HarmoDecon'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Zirui Wang
  - Ke Xu
  - Yang Liu
  - YuXu
  - Lu Zhang

# Author notes (optional)
author_notes:
  - ''
  - ''
  - ''
  - ''
  - 'Corresponding author'

date: '2025-09-01T00:00:00Z'
doi: 'https://doi.org/10.1093/bioinformatics/btaf451'

# Schedule page publish date (NOT publication's date).
publishDate: '2025-09-01T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['2']

# Publication name and optional abbreviated publication name.
publication: 'Bioinformatics'
publication_short: ''

abstract: "Motivation: The advent of spatially resolved transcriptomics (SRT) has revolutionized our understanding of tissue molecular microenvironments by enabling the study of gene expression in its spatial context. However, many SRT platforms lack single-cell resolution, necessitating cell-type deconvolution methods to estimate cell-type proportions in SRT spots. Despite advancements in existing tools, these methods have not addressed biases occurring at three scales: individual spots, entire tissue samples, and discrepancies between SRT and reference scRNA-seq datasets. These biases result in overbalanced cell-type proportions for each spot, mismatched cell-type fractions at the sample level, and data distribution shifts across platforms. Results: To mitigate these biases, we introduce HarmoDecon, a novel semi-supervised deep learning model for spatial cell-type deconvolution. HarmoDecon employs a multi-scale bias correction strategy, including spot-level bias correction, sample-level bias correction, and cross-platform bias correction, to enhance deconvolution accuracy. We systematically evaluated HarmoDecon using both simulated and real SRT datasets across multiple platforms. The experimental results demonstrated that HarmoDecon significantly outperformed existing methods in accurately estimating cell-type proportions while maintaining computational efficiency."

# Summary. An optional shortened abstract.
summary: A semi-supervised deep learning model for spatial cell-type deconvolution that mitigates multi-scale biases in spatially resolved transcriptomics.

tags: 
- Spatial transcriptomics
- Cell-type deconvolution
- Deep learning in Genomics
- Multi-scale bias correction
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://academic.oup.com/bioinformatics/article-pdf/41/9/btaf451/61698887/btaf451.pdf'
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: 'HarmoDecon framework'
  focal_point: 'Smart'
  preview_only: false 
  # Uncomment to use the original image size without processing
  # filename: featured.png  # if your image is PNG format

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
#projects:
#  - example

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
# slides: example
---

Supplementary notes can be added here, including code and data when available.
