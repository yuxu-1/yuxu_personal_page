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

date: '2025-11-1T00:00:00Z'
doi: 'https://doi.org/10.1093/bioinformatics/btaf469'

# Schedule page publish date (NOT publication's date).
publishDate: '2025-11-1T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['2']

# Publication name and optional abbreviated publication name.
publication: 'Bioinformatics'
publication_short: ''

abstract: "In silico transcription factor and DNA (TF–DNA) binding affinity prediction plays a vital role in examining TF binding preferences and understanding gene regulation. The existing tools employ TF–DNA binding profiles from in vitro high-throughput technologies to predict TF–DNA binding affinity. However, TFs tend to bind to sequences in open chromatin regions in vivo, such TF binding preference is seldomly considered by these existing tools. In this study, we developed TRAFICA, an open chromatin language model to predict TF–DNA binding affinity by integrating sequence characteristics of open chromatin regions from ATAC-seq experiments and in vitro TF–DNA binding profiles from high-throughput technologies. We pretrained TRAFICA on over 2.8 million nucleotide sequences in open chromatin regions derived from 197 ATAC-seq experiments (115 cell lines) to learn in vivo TF binding preferences. We further fine-tuned TRAFICA using low-rank adaptation (LoRA) on PBM and HT-SELEX TF-DNA binding profiles to learn intrinsic binding preferences for specific TFs. We systematically evaluated TRAFICA and compared its predictive performance with existing prediction tools and advanced DNA language models. The experimental results demonstrated that TRAFICA significantly outperformed the others in predicting in vitro and in vivo TF–DNA binding affinity, achieving state-of-the-art performance. These findings indicate that considering the sequence characteristics from open chromatin regions could significantly improve TF–DNA binding affinity prediction."
# Summary. An optional shortened abstract.
summary: An open chromatin language model for transcription factor-DNA binding affinity prediction by integrating ATAC-seq data and in vitro binding profiles, achieving state-of-the-art performance.

tags: 
- Transcription factor - DNA binding affinity
- DNA language models
- Deep learning in Genomics
- Open chromatin language model
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://watermark02.silverchair.com/btaf469.pdf?token=AQECAHi208BE49Ooan9kkhW_Ercy7Dm3ZL_9Cf3qfKAc485ysgAAA3QwggNwBgkqhkiG9w0BBwagggNhMIIDXQIBADCCA1YGCSqGSIb3DQEHATAeBglghkgBZQMEAS4wEQQMlKS2dgIlDsW2ky9YAgEQgIIDJ0ZDQCtqjmYsyOkhqVqFFkhdPZ3UmsvxafeNzmeodhV7jiZlnxJDVyQ5j10cZTna42p10cKS5r5IuAAICn9qUe39yDIBv50IQFRgWs4kd5huNej6M06KKbw8OV8emGD8OVpxx2V14odhfC4qq_dyNWq566XyX23rZdzNZXRTsydtEIwP8BOcr9YI3qU6gfc54Dq0kF02BXBmh68gIvCWNgcTa_E1gUP8ParSz7qM4ahTbiduQzjUspamXmSPx-F42AHRfG6aWIdTZvUj0BWOIskKzfXODvjyu9JS9OjXozJ1DQx0Y6gWx8hzYRR3gZTwcMWDNl1sUB2x2pTlnAG1Mvcxx4p7zJsDiLS2k0crUMX-lxUKSMtWptm5FsWDfR_MlH3xF5tvZRVVpSZUNJqtQ8Rla7IGQFklKZ9liCSZN63lpnEP_7Lu42Gp87dmGRQPCV1Y_QDuFrTkYclDvH22UpIW7g6t1953qTLSfjOxcdebN3RbjCHWfeaWtdWFoIq21roK9eGDbORdgDbxOOFEXEcxPsCvNwjHu2E4fhwDx7iwZcJqMYz5ngDHiO8GVPP__rLSusnze7m4vNFyPMAfAWdsdFAVfKi29ZzpKAsE-JpZoz9hvevGL0kBkPntRvtSsLq_ZSjwiuQ_Ae20rnQvhQIBUBPeVilroMul9jk4sSnmwQ_xy-4yC0vTwoEEcY772xUXqW1a62WDChc9uWjsXhwHUxOJlUdFxZD8J8tfuZm7l3ikE7NaEShkwVzMYC5EwdMcXtWSvUpJML1L1O_BoC0oJnJQ0gMrumkmGES97HMOFNuPvNmgOZEvJP7awGtzjG1ik3vP3zAPnBJ1vustIhLqBINUt5Y2ZGPE89smT2nwiasH__U-mNcSz5XV3wQd_wdIZk7rAuoN_s2puQj_isKu-TOadsHlEmuUuK1ZBs_bL2WuOQHBsQzqrpSnfrg4kwlEitFM3Gnvecre-RaJIaXXLV0pSTqnZb8EIgD-OPjgqMdWrfNz99UHuBj9ftjQ9OtqSgqGEMLwMC7TUxF1l9s4bEdq1AyviRaDJKbvgDGgB7C5Vq6bWg'
url_code: 'https://github.com/ericcombiolab/TRAFICA'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: 'TRAFICA framework'
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

![TRAFICA Framework](/uploads/trafica_framework.png)

Supplementary notes can be added here, including [code](https://github.com/ericcombiolab/TRAFICA), [model](https://huggingface.co/collections/Allanxu/trafica) and [data](https://zenodo.org/records/15781226).
