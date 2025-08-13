---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing

sections:
  - block: hero
    content:
      title: |
        LinS Lab
      image:
        filename: welcome.jpg
      text: |
        <br>

        LinSLab at the National University of Singapore advances robotics and AI through research in vision-language modeling, manipulation, and planning. Our work spans from frameworks like FLIP to foundational models such as ManiFM, bridging theory and real-world robotic systems.

  - block: collection
    content:
      title: Latest News
      subtitle:
      text:
      count: 2
      filters:
        author: ""
        category: ""
        exclude_featured: false
        publication_type: ""
        tag: ""
      offset: 0
      order: desc
      page_type: post
    design:
      view: card
      columns: "1"

  # - block: markdown
  #   content:
  #     title:
  #     subtitle: ""
  #     text:
  #   design:
  #     columns: "1"
  #     background:
  #       image:
  #         filename: coders.jpg
  #         filters:
  #           brightness: 1
  #         parallax: false
  #         position: center
  #         size: cover
  #         text_color_light: true
  #     spacing:
  #       padding: ["20px", "0", "20px", "0"]
  #     css_class: fullscreen

  - block: collection
    content:
      title: Latest Preprints
      text: ""
      count: 2
      filters:
        folders:
          - publication
        publication_type: "article"
    design:
      view: citation
      columns: "1"

  - block: markdown
    content:
      title:
      subtitle:
      text: |
        {{% cta cta_link="./people/" cta_text="Meet the team →" %}}
    design:
      columns: "1"
---
