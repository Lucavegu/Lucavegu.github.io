---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2026-10-06
type: landing

sections:
  # ── Photo, name, bio, interests, education (all read from data/authors/me.yaml)
  - block: resume-biography-3
    content:
      username: me
      text: ''
      # To offer your CV as a download: upload the PDF as static/uploads/cv.pdf,
      # then remove the "#" from the three lines below.
      # button:
      #   text: Download CV
      #   url: uploads/cv.pdf
      headings:
        about: ''
        education: ''
        interests: ''
    design:
      background:
        gradient_mesh:
          enable: true
      name:
        size: sm # Options: xs, sm, md, lg, xl
      avatar:
        size: medium
        shape: circle

  # ── Publications (one folder per paper in content/publications/)
  - block: collection
    id: papers
    content:
      title: Publications
      text: ''
      # 0 = show all
      count: 0
      filters:
        folders:
          - publications
        exclude_featured: false
    design:
      view: citation

  # ── Manuscripts not yet published
  - block: markdown
    id: in-progress
    content:
      title: Manuscripts in Progress
      subtitle: ''
      text: |-
        - **Venegas, L.**, Small, C.M., Yáñez, J.M., Espinoza, J., Lhorente, J.P., Derome, N. Assessment of skin mucus microbiota as predictor of sea lice (*Caligus rogercresseyi*) burden in Atlantic salmon (*Salmo salar*) using machine learning approaches. 2026. *Animal Microbiome*. Under review. [Code](https://github.com/Lucavegu/Caligus)
        - Contreras-Orellana, M., Aldea, C., Andrade, C., Filipsson, H.L., Kalantari, Z., Kåresdotter, E., **Venegas, L.**, Wacyk, J., Williams, M.E. Fjords as Ecosystem Providers and Their Role as a Biome. In preparation.
    design:
      columns: '1'

  # ── Conference presentations (one folder per talk in content/events/)
  - block: collection
    id: talks
    content:
      title: Presentations
      filters:
        folders:
          - events
    design:
      view: date-title-summary

  # ── Contact: phone number and institutional email
  - block: contact-info
    id: contact
    content:
      title: Contact
      subtitle: ''
      connect_title: Get in Touch
      text: For collaborations, questions about my research, or review requests.
      # TODO: replace the two placeholders below with your real details.
      email: your.name@institution.edu
      phone: '+1 000 000 0000'
      social:
        - icon: academicons/orcid
          url: https://orcid.org/0000-0003-3668-5681
        - icon: academicons/researchgate
          url: https://www.researchgate.net/profile/Lucas-Venegas
        - icon: brands/linkedin
          url: https://www.linkedin.com/in/lucas-venegas-9a9939124/
        - icon: brands/github
          url: https://github.com/Lucavegu
        - icon: brands/bluesky
          url: https://bsky.app/profile/lucavegu.bsky.social
      show_form: false
---
