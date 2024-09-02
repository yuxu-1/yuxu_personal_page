---
# Leave the homepage title empty to use the site title
title:
date: 2023-08-11
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: Biography
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: yuxu
  - block: experience
    content:
      title: Academic Positions
      # Date format for experience
      #   Refer to https://wowchemy.com/docs/customization/#date-format
      date_format: Jan 2006
      # Experiences.
      #   Add/remove as many `experience` items below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - title: Senior Research Assistant
          company: Hong Kong Baptist University 
          company_url: ''
          company_logo: HKBU_Logo
          location: HKSAR, China
          date_start: '2021-08-15'
          date_end: '2023-08-31'
          description: 'Research topics: Gene regulatory network reconstruction; Disease risk prediction'
    design:
      columns: '2'
  - block: collection
    id: publications
    content:
      title: Recent Publications
      text: |-
        {{% callout note %}}
        Quickly discover relevant content by [filtering publications](./publication/).
        {{% /callout %}}
      filters:
        folders:
          - publication
        exclude_featured: true
    design:
      columns: '2'
      view: citation
#  - block: markdown
#    content:
#      title: Gallery
#      subtitle: ''
#      text: |-
#        {{< gallery album="demo" >}}
#    design:
#      columns: '1'
#  - block: collection
#    id: featured
#    content:
#      title: Featured Publications
#      filters:
#        folders:
#          - publication
#        featured_only: true
#    design:
#      columns: '2'
#      view: card
  - block: accomplishments
    id: academic
    content:
      title: Academic Experiences
      subtitle: ''
      text: ''
      # Date format: https://wowchemy.com/docs/customization/#date-format
      date_format: '2006'
      items:
        - title: 'External reviewer (BIBM 2024)'
          certificate_url: ''
          date_end: ''
          date_start: '2024-09-1'
          description: ''
          organization: International Conference on Bioinformatics and Biomedicine
          organization_url: 
          url: ''
        - title: 'Co-reviewer (training in peer review)'
          certificate_url: ''
          date_end: ''
          date_start: '2023-09-10'
          description: ''
          organization: Nature Communications
          organization_url: https://www.nature.com/ncomms/
          url: ''
        - title: 'External reviewer (BIBM 2023)'
          certificate_url: ''
          date_end: ''
          date_start: '2023-09-01'
          description: ''
          organization: International Conference on Bioinformatics and Biomedicine
          organization_url: https://bidma.cpsc.ucalgary.ca/IEEE-BIBM-2023/
          url: ''
        - title: 'External reviewer (ISBRA 2023)'
          certificate_url: ''
          date_end: ''
          date_start: '2023-08-01'
          description: ''
          organization: 19th International Symposium on Bioinformatics Research and Applications
          organization_url: https://mangul-lab-usc.github.io/ISBRA23/
          url: ''
    design:
      columns: '2'
  - block: accomplishments
    id: teaching
    content:
      title: Teaching Experiences
      subtitle: ''
      text: ''
      # Date format: https://wowchemy.com/docs/customization/#date-format
      date_format: '2006'
      items:
        - title: 'Teaching Assistant'
          certificate_url: ''
          date_end: '2024-05-01'
          date_start: '2024-01-08'
          description: 'COMP7940 Cloud Computing'
          organization: Department of Computer Science, Hong Kong Baptist University
          organization_url: 
          url: ''
        - title: 'Teaching Assistant'
          certificate_url: ''
          date_end: ''
          date_start: '2024-09-02'
          description: 'COMP2035 AI and Data Analytics for Health and Social Innovation I'
          organization: Department of Computer Science, Hong Kong Baptist University
          organization_url: 
          url: ''
    design:
      columns: '2'
  - block: contact
    id: contact
    content:
      title: Contact
      subtitle:
      text: |-
      #Contact (add or remove contact options as necessary)
      email: csyuxu@comp.hkbu.edu.hk
      #appointment_url: 'https://calendly.com'
      address:
        street: David C Lam Building (DLB) 625, Waterloo Rd, Kowloon Tong
        city: Hong Kong
        region: CN
        postcode: ''
        country: China
        country_code: CN
      office_hours:
        - 'Monday 13:00 to 17:00'
        - 'Wednesday 13:00 to 17:00'
      contact_links:
      # Automatically link email and phone or display as text?
      autolink: true
    design:
      columns: '2'
---
