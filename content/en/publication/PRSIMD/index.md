---
title: 'A machine learning model for disease risk prediction by integrating
genetic and non-genetic factors'

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

date: '2022-12-08T00:00:00Z'
doi: '10.1109/BIBM55620.2022.9994925'

# Schedule page publish date (NOT publication's date).
publishDate: '2022-12-08T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['1']

# Publication name and optional abbreviated publication name.
publication: 'IEEE International Conference on Bioinformatics and Biomedicine (BIBM) 2022'
publication_short: ''

abstract: "Polygenic risk score (PRS) has been widely used to 
identify the high-risk individuals from the general population, 
which would be helpful for disease prevention and early treat-
ment. Many methods have been developed to calculate PRS by 
weighting and aggregating the phenotype-associated risk alleles 
from genome-wide association studies. However, only considering 
genetic effects may not be sufﬁcient for risk prediction because 
the disease risk is not only related to genetic factors but also non-
genetic factors, e.g., diet, physical exercise et al. But it is still a 
challenge to integrate these genetic and non-genetic factors into a 
uniﬁed machine learning framework for disease risk prediction. 
In this paper, we proposed PRSIMD (PRS Integrating Multi-
source Data), a machine learning model that applies posterior 
regularization to integrate genetic and non-genetic factors to 
improve disease risk prediction. Also, we applied Mendelian 
Randomization analysis to identify the causal non-genetic risk 
factors for the selected diseases. We applied PRSIMD to predict 
type 2 diabetes and coronary artery disease from UK Biobank 
and observed that PRSIMD was signiﬁcantly better than the 
existing methods to calculate PRS. In addition, we observed 
that PRSIMD achieved the better predictive power than the 
composite risk score. "
# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags: 
- Disease risk prediction
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9994925'
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: 'https://www.bilibili.com/video/BV1wG411M7fh/?share_source=copy_web&vd_source=1fa2f4747202c21b79e5a7bc67c6245d'

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


Supplementary notes can be added here, including [code and data](https://github.com/ericcombiolab/PRSIMD).
