---
title: 'TRAFICA: An Open Chromatin Language Model to Improve Transcription Factor Binding Affinity Prediction'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - YuXu
  - Lu Zhang
  - 'et al'
# Author notes (optional)
author_notes:
  - 'First author'
  - 'Corresponding author'

date: '2023-11-05T00:00:00Z'
doi: 'https://doi.org/10.1101/2023.11.02.565416'

# Schedule page publish date (NOT publication's date).
publishDate: '2023-11-05T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['3']

# Publication name and optional abbreviated publication name.
publication: 'BioRxiv'
publication_short: ''

abstract: "In silico transcription factor and DNA (TF-DNA) binding affinity prediction plays a vital role in examining TF binding preferences and understanding gene regulation. The existing tools employ TF-DNA binding profiles from in vitro high-throughput technologies to predict TF-DNA binding affinity. However, TFs tend to bind to sequences in open chromatin regions in vivo, such TF binding preference is seldomly considered by these existing tools. In this study, we developed TRAFICA, an open chromatin language model to predict TF-DNA binding affinity by integrating the characteristics of sequences from open chromatin regions in ATAC-seq experiments and in vitro TF-DNA binding profiles from high-throughput technologies. We applied self-supervised learning to pre-train TRAFICA on over 13 million nucleotide sequences from the peaks in ATAC-seq experiments to learn the TF binding preference in vivo. TRAFICA was further fine-tuned using the TF-DNA binding profiles from PBM and HT-SELEX technologies to learn the association between TFs and their target DNA sequences. We observed that TRAFICA significantly outperformed both machine learning-based and deep learning-based tools in predicting in vitro and in vivo TF-DNA binding affinity. These findings indicate that considering the characteristics of sequences from open chromatin regions could significantly improve TF-DNA binding affinity prediction, particularly when limited TF-DNA binding profiles from high-throughput technologies are available for specific TFs."
# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags: 
- Transcription factor binding affinitiy
- language models
- In vitro binding
- open chromatin regions
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: ''
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
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/pLCdAaMFLTE)'
  focal_point: ''
  preview_only: false

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


Supplementary notes can be added here, including [code](https://github.com/ericcombiolab/TRAFICA) and [data](https://zenodo.org/records/8248340).
