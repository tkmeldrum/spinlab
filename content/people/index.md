---
title: People
date: 2022-10-24

type: landing

sections:
  - block: people
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
  
  # - block: collection
  #   content:
  #     title: Group antics
  #     subtitle:
  #     text:
  #     count: 2
  #     filters:
  #       author: ''
  #       category: ''
  #       exclude_featured: false
  #       publication_type: ''
  #       tag: ''
  #     offset: 0
  #     order: desc
  #     page_type: antics
  #   design:
  #     view: card
  #     columns: '1'
  #     show_interests: false
  #     show_role: false
  #     show_social: false
 
  # - block: markdown
  #   content:
  #     title: 
  #     text: |
  #       {{% cta cta_link="/people/" cta_text="Learn more →" %}}
---