---
title: 'TRAFICA: Improving Transcription Factor Binding Affinity Prediction using Deep Language Model on ATAC-seq Data'

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

abstract: "In silico prediction of transcription factor (TF) binding affinity plays a vital role in determining TF binding preferences and understanding gene regulation. Many existing tools utilize known TF-DNA binding data to train conventional machine learning and deep learning models to predict TF-DNA binding affinities. The majority of these tools do not consider the natural preferences of DNA sequences binding to TFs, which could be influenced by chromatin accessibility. In this study, we developed TRAFICA, a deep language model to predict TF-DNA binding affinities by integrating chromatin accessibility from ATAC-seq and known TF-DNA binding data. We pre-trained TRAFICA on an integrated ATAC-seq dataset with over 13 million nucleotide sequences in a self-supervised manner to learn potential TF-DNA binding preferences and contextual relationships within DNA sequences. TRAFICA was fine-tuned using PBM and HT-SELEX datasets to predict in vitro TF-DNA binding affinities. We also implemented AdapterFusion to enhance its ability to predict in vivo TF-DNA binding affinities. We observed TRAFICA significantly outperformed the six existing tools in predicting in vitro TF-DNA binding affinities and was comparable with the best tool on in vivo prediction."
# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags: 
- Transcription factor binding affinitiy
- Genome language models
- In vitro binding
- Chromatin accessibility
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
