---
title: "dynDeepDRIM: a dynamic deep learning model to infer direct regulatory interactions using time-course single-cell gene expression data"
authors:
- YuXu
- JiaxingCheng
- Aiping Lyu
- William K. Cheung
- Lu Zhang
author_notes:
- "First author"
- "Co-first author"
- "Corresponding author"
- "Corresponding author"
- "Corresponding author"
date: "2022-09-01T00:00:00Z"
doi: "https://doi.org/10.1093/bib/bbac424"

# Schedule page publish date (NOT publication's date).
publishDate: "2022-09-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "Briefings in Bioinformatics"
publication_short: ""

abstract: "Time-course single-cell RNA sequencing (scRNA-seq) data have been widely used to explore dynamic changes in gene expression of
transcription factors (TFs) and their target genes. This information is useful to reconstruct cell-type-specific gene regulatory networks
(GRNs). However, the existing tools are commonly designed to analyze either time-course bulk gene expression data or static scRNA-seq
data via pseudo-time cell ordering. A few methods successfully utilize the information from multiple time points while also considering
the characteristics of scRNA-seq data. We proposed dynDeepDRIM, a novel deep learning model to reconstruct GRNs using time-
course scRNA-seq data. It represents the joint expression of a gene pair as an image and utilizes the image of the target TF–gene
pair and the ones of the potential neighbors to reconstruct GRNs from time-course scRNA-seq data. dynDeepDRIM can effectively
remove the transitive TF–gene interactions by considering neighborhood context and model the gene expression dynamics using high-
dimensional tensors. We compared dynDeepDRIM with six GRN reconstruction methods on both simulation and four real time-course
scRNA-seq data. dynDeepDRIM achieved substantially better performance than the other methods in inferring TF–gene interactions
and eliminated the false positives effectively. We also applied dynDeepDRIM to annotate gene functions and found it achieved evidently
better performance than the other tools due to considering the neighbor genes."
# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
- GRN reconstruction
- Single-cell
featured: false

# links:
# - name: ""
#   url: ""
url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: 'https://mp.weixin.qq.com/s/HC3hKauYrNiCaef8n7cZVQ'
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

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
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
# slides: []
---

Supplementary materials, including [code](https://github.com/ericcombiolab/dynDeepDRIM) and [data](https://zenodo.org/record/6720690).
