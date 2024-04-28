---
# Leave the homepage title empty to use the site title
title: ''
date: 2022-10-24
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: Biography
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
  - block: experience
    content:
      title: Experience
      # Date format for experience
      #   Refer to https://docs.hugoblox.com/customization/#date-format
      date_format: Jan 2006
      # Experiences.
      #   Add/remove as many `experience` items below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - title: "Head of the Joint Research Unit Ecology of Guianan Forests (UMR EcoFoG"
          company: "AgroParisTech"
          company_url: "https://www.ecofog.gf"
          company_logo: ecofog
          location: "Kourou, French Guiana"
          date_start: "2010-01-01"
          date_end: "2020-08-31"
          description: |2-
            Responsibilities included:
              * Administration of research 
              * Management
              * Teaching (graduate and post-graduate students)
              * Research
    design:
      columns: '2'
  - block: collection
    id: featured
    content:
      title: Featured Publications
      text: |-
        {{% callout note %}}
        Show [all publications](./publication/).
        {{% /callout %}}
      filters:
        folders:
          - publication
        featured_only: true
    design:
      columns: '2'
      view: card
  - block: collection
    content:
      title: Recent Publications
      filters:
        folders:
          - publication
        exclude_featured: true
    design:
      columns: '2'
      view: citation
  - block: collection
    id: talks
    content:
      title: Talks
      filters:
        folders:
          - event
    design:
      columns: '2'
      view: compact
  - block: portfolio
    id: software
    content:
      title: Software
      filters:
        folders:
          - software
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      view: showcase
      # For Showcase view, flip alternate rows?
      flip_alt_rows: true
  - block: portfolio
    id: course
    content:
      title: Courses
      filters:
        folders:
          - course
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      view: showcase
      # For Showcase view, flip alternate rows?
      flip_alt_rows: true
  - block: collection
    id: posts
    content:
      title: "Recent Posts"
      subtitle: ''
      text: ''
      # Choose how many pages you would like to display (0 = all pages)
      count: 5
      # Filter on criteria
      filters:
        folders:
          - post
        author: ""
        category: ""
        tag: ""
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ""
      # Choose how many pages you would like to offset by
      offset: 0
      # Page order: descending (desc) or ascending (asc) date.
      order: desc
    design:
      # Choose a layout view
      view: compact
      columns: '2'
  - block: contact
    id: contact
    content:
      title: Contact
      # Choose a map provider in `params.yaml` to show a map from these coordinates
      coordinates:
        latitude: '43.646438'
        longitude: '3.878938'  
      # Automatically link email and phone or display as text?
      autolink: true
      # Email form provider
      form:
        provider: formspree
        formspree:
          id: eric.marcon@agroparistech.fr
    design:
      columns: '2'
---
