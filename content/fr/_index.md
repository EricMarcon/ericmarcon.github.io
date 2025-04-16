---
# Leave the homepage title empty to use the site title
title: ''
date: 2022-10-24
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: Biographie
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
        - title: "Directeur de l'Unité Mixte de Recherche Ecologie des Forêts de Guyane (UMR EcoFoG)"
          company: "AgroParisTech"
          company_url: "https://www.ecofog.gf"
          company_logo: ecofog
          location: "Kourou, Guyane française"
          date_start: "2010-01-01"
          date_end: "2020-08-31"
          description: |2-
            Responsabilités:
              * Administration de la Recherche
              * Encadrement
              * Enseignement (niveaux bac+5 et plus)
              * Recherche
  - block: collection
    id: featured
    content:
      title: Publications sélectionnées
      text: |-
        {{% callout note %}}
        Afficher [toutes les publications](./publication/).
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
      title: Publications récentes
      filters:
        folders:
          - publication
        exclude_featured: true
    design:
      columns: '2'
      view: card
  - block: collection
    id: talks
    content:
      title: Commnunications
      filters:
        folders:
          - event
    design:
      columns: '2'
      view: compact
  - block: portfolio
    id: software
    content:
      title: Logiciels
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
      title: Cours
      filters:
        folders:
          - course
      # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
      default_button_index: 0
      # Filter toolbar (optional).
      # Add or remove as many filters (`filter_button` instances) as you like.
      # To show all items, set `tag` to "*".
      # To filter by a specific tag, set `tag` to an existing tag name.
      # To remove the toolbar, delete the entire `filter_button` block.
      buttons:
        - name: Tous
          tag: '*'
        - name: Ecologie
          tag: ecologie
        - name: R
          tag: r
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      view: showcase
      # For Showcase view, flip alternate rows?
      flip_alt_rows: true
  - block: collection
    id: posts
    content:
      title: "Articles Récents"
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
