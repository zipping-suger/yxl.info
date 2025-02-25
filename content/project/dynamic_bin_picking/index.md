---
title: A Framework for Efficient and Robust Dynamic Bin-Picking
summary: Robot dynamic Bin-Picking
tags:
  - dbq
date: '2023-03-10T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: demo
  focal_point: Smart

# links:
#   - icon: twitter
#     icon_pack: fab
#     name: Follow
#     url: https://twitter.com/georgecushen
url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides: example
---
The efficiency and reliability of robotic bin-picking are crucial as it directly affects the productivity of automated in- dustrial processes. However, traditional bin-picking approaches necessitate prerequisites of static objects and fixed collisions. It leads to limitations in deployment, inefficiency during oper- ation, and unreliability under unforeseen disruptions. 

We aim to achieve dynamic bin-picking, breaking the static assumptions in traditional bin-picking. We present a Dynamic Bin-Picking Framework (DBPF) equipping manip- ulators with strong reactivity to handle dynamic targets and obstacles simultaneously. The horizon-based discrete trajectory optimization solves the optimal action in a close-loop manner to support real-time feasible motion. Given 6D poses from suction planning at each timestep, the optimal target pose is selected with consideration of picking consistency and neural network-based tendency-aware-manipulability scores. Heuristic task-specific designs within modules and the pipeline highly con- tribute to the picking success. Through empirical experiments, our method demonstrates superior performance in terms of success rate, efficiency, and reliability than baseline approaches, showcasing a promising solution for the next generation of robotic bin-picking.
{{< youtube UGZTbHR1PPE >}}
