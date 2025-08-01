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
    content:
      title: Our research
      subtitle: See what's up 
      text: 
      count: 3
      filters:
        # folders: 
        #   - pages
        author: ''
        # categories: 'research'
        exclude_featured: false
        # tag: 'research'
      offset: 0
      order: desc
      page_type: research
    design:
      view: card
      columns: '3'

  - block: collection
    content:
      title: Latest News
      subtitle:
      text:
      count: 5
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
      view: card
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

  # - block: collection
  #   content:
  #     title: Latest Preprints
  #     text: ""
  #     count: 5
  #     filters:
  #       folders:
  #         - publication
  #       publication_type: 'article'
  #   design:
  #     view: citation
  #     columns: '1'
---
