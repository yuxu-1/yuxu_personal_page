---
# Leave the homepage title empty to use the site title
title:
date: 2023-08-11
type: landing

sections:
  - block: markdown
    id: disclaimer
    content:
      title: ''
      text: |-
        > ⚠️ **声明**：本中文页面内容由 AI 自动生成，可能存在翻译不准确或语义误差，建议以[英文页面](/)为准。如有疑问，欢迎通过邮件联系确认。
    design:
      columns: '2'
      background:
        color: '#fff3cd'
  - block: about.biography
    id: about
    content:
      title: 个人简介
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: yuxu
  - block: collection
    id: featured
    content:
      title: 精选论文
      filters:
        folders:
          - publication
        featured_only: true
    design:
      columns: '2'
      view: card
  - block: collection
    id: publications
    content:
      title: 近期论文
      text: |-
        {{% callout note %}}
        可通过[筛选论文](./publication/)快速查找相关内容。
        {{% /callout %}}
      filters:
        folders:
          - publication
        exclude_featured: false
    design:
      columns: '2'
      view: citation
  - block: experience
    id: positions
    content:
      title: 学术职位
      # Date format for experience
      #   Refer to https://wowchemy.com/docs/customization/#date-format
      date_format: Jan 2006
      # Experiences.
      #   Add/remove as many `experience` items below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - title: 高级研究助理
          company: 香港浸会大学
          company_url: ''
          company_logo: HKBU_Logo
          location: 中国香港特别行政区
          date_start: '2021-08-15'
          date_end: '2023-08-31'
          description: '研究方向：基因调控网络重建；疾病风险预测'
    design:
      columns: '2'
  - block: accomplishments
    id: academic
    content:
      title: 学术活动
      subtitle: ''
      text: ''
      # Date format: https://wowchemy.com/docs/customization/#date-format
      date_format: '2006'
      items:
        - title: '外部审稿人 (Bioinformatics)'
          certificate_url: ''
          date_end: ''
          date_start: '2026-01-01'
          description: ''
          organization: Bioinformatics
          organization_url: https://academic.oup.com/bioinformatics
          url: ''
        - title: '外部审稿人 (BIBM 2024)'
          certificate_url: ''
          date_end: ''
          date_start: '2024-09-01'
          description: ''
          organization: International Conference on Bioinformatics and Biomedicine
          organization_url: 
          url: ''
        - title: '联合审稿人（同行评审培训）'
          certificate_url: ''
          date_end: ''
          date_start: '2023-09-10'
          description: ''
          organization: Nature Communications
          organization_url: https://www.nature.com/ncomms/
          url: ''
        - title: '外部审稿人 (BIBM 2023)'
          certificate_url: ''
          date_end: ''
          date_start: '2023-09-01'
          description: ''
          organization: International Conference on Bioinformatics and Biomedicine
          organization_url: https://bidma.cpsc.ucalgary.ca/IEEE-BIBM-2023/
          url: ''
        - title: '外部审稿人 (ISBRA 2023)'
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
      title: 教学经历
      subtitle: ''
      text: ''
      # Date format: https://wowchemy.com/docs/customization/#date-format
      date_format: '2006'
      items:
        - title: '助教'
          certificate_url: ''
          date_end: '2024-05-01'
          date_start: '2024-01-08'
          description: 'COMP7940 云计算'
          organization: 香港浸会大学计算机科学系
          organization_url: 
          url: ''
        - title: '助教'
          certificate_url: ''
          date_end: '2024-12-22'
          date_start: '2024-09-02'
          description: 'COMP2035 健康与社会创新人工智能与数据分析 I'
          organization: 香港浸会大学计算机科学系
          organization_url: 
          url: ''
        - title: '助教'
          certificate_url: ''
          date_end: '2025-05-01'
          date_start: '2025-01-08'
          description: 'COMP7940 云计算'
          organization: 香港浸会大学计算机科学系
          organization_url: 
          url: ''
        - title: '助教'
          certificate_url: ''
          date_end: '2025-12-22'
          date_start: '2025-09-02'
          description: 'COMP7510 互联网计算与编程'
          organization: 香港浸会大学计算机科学系
          organization_url: 
          url: ''
        - title: '助教'
          certificate_url: ''
          date_start: '2026-01-08'
          description: 'COMP7800 IT 管理中的分析模型'
          organization: 香港浸会大学计算机科学系
          organization_url: 
          url: ''
    design:
      columns: '2'
  - block: contact
    id: contact
    content:
      title: 联系方式
      subtitle:
      text: |-
      email: csyuxu@comp.hkbu.edu.hk
      address:
        street: 九龙塘窝打老道 David C Lam 大楼 (DLB) 625
        city: 香港
        region: CN
        postcode: ''
        country: 中国
        country_code: CN
      office_hours:
        - '周一 13:00-17:00'
        - '周三 13:00-17:00'
      contact_links:
      autolink: true
    design:
      columns: '2'
---
