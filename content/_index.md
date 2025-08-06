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
    id: research_overview
    content:
      title: Our research
      subtitle: ''
      text: ''
      # Choose how many pages you would like to display (0 = all pages)
      count: 3
      # Filter on criteria
      filters:
        # The folders to display content from
        folders:
          - research_overview
        author: ""
        category: ""
        tag: ""
        publication_type: ""
        featured_only: false
        exclude_featured: false
        exclude_future: false
        exclude_past: false
      # Choose how many pages you would like to offset by
      # Useful if you wish to show the first item in the Featured widget
      offset: 0
      # Field to sort by, such as Date or Title
      sort_by: 'Title'
      sort_ascending: false
    design:
      # Choose a listing view
      view: card


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
