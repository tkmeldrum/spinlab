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
  

  - block: markdown
    id: research
    content:
      title: Our research
      text: |
        Research in the spinlab centers around single-sided nuclear magnetic resonance. We focus on methods and instrumentations development, data and computational models, and a range a applications. 
        {{% cta cta_link="./research/" cta_text="Learn more →" %}}

  - block: people
    id: people
    content:
      title: Meet the Team
      # Choose which groups/teams of users to display.
      #   Edit `user_groups` in each user's profile to add them to one or more of these groups.
      user_groups:
          - Principal Investigator
          - Researchers
          - Graduate Students
          - Undergraduate Students
          - Administration
          - Visitors
          - Alumni
      sort_by: Params.last_name
      sort_ascending: true
    design:
      show_interests: false
      show_role: true
      show_social: true

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
