---
# Leave the homepage title empty to use the site title
title:
date: 2025-08-01
type: landing

sections:
  - block: hero
    content:
      title: |
      image:
        filename: logo.jpg
        focal_point: Left
        align: Left
        alt_text: "spinlab logo"
        width: 240
      text: |
        <br>
        
        **spinlab** at William & Mary is a student-driven, NMR-focused research group investigating physical properties of materials.
  
  - block: collection
    id: research
    content:
      title: Our Research
      subtitle:
      text: |
        <p class="research-intro">Our research addresses problems in physical chemistry and materials science using both experimental and computational methods, centered on single-sided nuclear magnetic resonance (NMR) relaxometry — trading the atom-specific signal of a million-dollar spectrometer for something far cheaper and more flexible. What we do: instrumentation and methods that make better measurements possible, computational work that makes sense of what we measure, and applications that put both to use on real materials.</p>
      count: 4
      # filters:
      #   author: ''
      #   category: ''
      #   exclude_featured: false
      #   publication_type: ''
      #   tag: ''
      # offset: 0
      sort_by: Weight
      sort_ascending: true
      page_type: research
    design:
      view: showcase
      columns: '1'

  - block: collection
    id: publications
    content:
      title: Recent Publications
      subtitle:
      count: 5
      filters:
        exclude_featured: false
      page_type: publications
      order: desc
      archive:
        text: "See all publications"
    design:
      view: citation
      columns: '1'

  - block: markdown
    content:
      title: Group
      text: |
        <img src="/media/groupphoto_2026.jpg" alt="Spinlab group photo, 2026" style="width:70%; max-width:70%; display:block; margin:0 auto;">
        <p style="font-size: 0.85em; font-style: italic; text-align: center;">Spring 2026</p>
    design:
      columns: '1'
      css_style: "padding-bottom: 20px;"

  - block: people
    id: people
    content:
      title:
      # Choose which groups/teams of users to display.
      #   Edit `user_groups` in each user's profile to add them to one or more of these groups.
      user_groups:
          - Principal Investigator
          - Researchers
          - Graduate Student
          - Undergraduate Students
      sort_by: Params.last_name
      sort_ascending: true
      footer_text: |
        {{% cta cta_alt_link="/people/" cta_alt_text="See the full roster, including alumni" %}}
    design:
      show_interests: false
      show_role: true
      show_social: true
      css_class: "pt-0"

  - block: collection
    id: news
    content:
      title: Latest News
      subtitle:
      text:
      count: 3
      filters:
        author: ''
        category: ''
        exclude_featured: false
        publication_type: ''
        tag: ''
      offset: 0
      order: desc
      page_type: post
    design:
      view: compact
      columns: '2'
  
  # - block: markdown
  #   content:
  #     title:
  #     subtitle:
  #     text: |
  #       {{% cta cta_link="./people/" cta_text="Meet the group →" %}}
  #   design:
  #     columns: '2'
  
  # - block: markdown
  #   content:
  #     title: 
  #     subtitle: ''
  #     text:
  #   design:
  #     columns: '1'
  #     background:
  #       image: 
  #         filename: coders.jpg
  #         filters:
  #           brightness: 0
  #         parallax: false
  #         position: center
  #         size: cover
  #         text_color_light: true
  #     spacing:
  #       padding: ['20px', '0', '20px', '0']
  #     css_class: fullscreen

  # - block: markdown
  #   content: 
  #     title: tour
  #     text: ""
  #     count: 1
  #     page_type: 
  #     filters:
  #       folders:
  #         - tour
  #       publication_type: 'article'
  #   design:
  #     view: citation
  #     columns: '1'
---
