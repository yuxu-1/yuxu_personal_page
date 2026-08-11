---
title: 'stDyer enables spatial domain clustering with dynamic graph embedding'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Ke Xu
  - YuXu
  - Zirui Wang
  - Xin Maizie Zhou
  - Lu Zhang

# Author notes (optional)
author_notes:
    - "First author"
    - "Second author"
    - "Third author"
    - "Corresponding author"
    - "Corresponding author"
date: '2025-02-20T00:00:00Z'
doi: '10.1186/s13059-025-03503-y'

# Schedule page publish date (NOT publication's date).
publishDate: '2025-02-20T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['2']

# Publication name and optional abbreviated publication name.
publication:  Genome Biology
publication_short: Genome Biol

abstract: Spatially resolved transcriptomics (SRT) data provide critical insights into gene expression patterns within tissue contexts, necessitating effective methods for identifying spatial domains. We introduce stDyer, an end-to-end deep learning framework for spatial domain clustering in SRT data. stDyer combines Gaussian Mixture Variational AutoEncoder with graph attention networks to learn embeddings and perform clustering. Its dynamic graphs adaptively link units based on Gaussian Mixture assignments, improving clustering and producing smoother domain boundaries. stDyer's mini-batch strategy and multi-GPU support facilitate scalability to large datasets. Benchmarking against state-of-the-art tools, stDyer demonstrates superior performance in spatial domain clustering, multi-slice analysis, and large-scale dataset handling.

# Summary. An optional shortened abstract.
summary: An end-to-end deep learning framework for spatial domain clustering in spatially resolved transcriptomics data using dynamic graph embedding and Gaussian Mixture Variational AutoEncoder.

tags: 
  - Spatial Transcriptomics
  - Deep Learning
  - Graph Neural Networks
  - Bioinformatics

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://link.springer.com/content/pdf/10.1186/s13059-025-03503-y.pdf'
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: 'https://link.springer.com/article/10.1186/s13059-025-03503-y'
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: 'stDyer framework'
  focal_point: ''
  preview_only: false

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
slides: ""
---

## Overview

stDyer is an innovative deep learning framework designed for spatial domain clustering in spatially resolved transcriptomics (SRT) data. The framework integrates:

- **Gaussian Mixture Variational AutoEncoder (GM-VAE)** for learning meaningful embeddings
- **Graph Attention Networks (GAT)** for capturing spatial relationships
- **Dynamic Graph Construction** that adaptively links spatial units based on Gaussian Mixture assignments
- **Mini-batch Strategy** and **Multi-GPU Support** for handling large-scale datasets

## Key Features

### 1. Dynamic Graph Embedding
- Adaptively constructs graphs based on clustering assignments
- Produces smoother spatial domain boundaries
- Captures both transcriptomic similarity and spatial proximity

### 2. Scalability
- Mini-batch processing strategy
- Multi-GPU support for large datasets
- Efficient handling of high-resolution SRT data

### 3. Superior Performance
- Outperforms state-of-the-art tools in spatial domain clustering
- Excellent performance in multi-slice analysis
- Robust handling of large-scale datasets

## Citation

If you use stDyer in your research, please cite:

```bibtex
@article{xu2025stdyer,
  title={stDyer enables spatial domain clustering with dynamic graph embedding},
  author={Xu, Ke and Xu, Yu and Wang, Zirui and Zhou, Xin Maizie and Zhang, Lu},
  journal={Genome Biology},
  volume={26},
  number={1},
  pages={34},
  year={2025},
  publisher={BioMed Central},
  doi={10.1186/s13059-025-03503-y}
}
```
