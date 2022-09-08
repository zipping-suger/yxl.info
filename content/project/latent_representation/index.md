---
title: Learning Latent Object-Centric Representations for Visual-Based Robot Manipulation
summary:  Object-Centric representations for learning manipulation skills.
tags:
  - Robert Learning
date: '2021-03-27T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Photo by rawpixel on Unsplash
  focal_point: Smart

# links:
#  - icon: twitter
#    icon_pack: fab
#    name: Follow
#    url: https://twitter.com/georgecushen
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

For multi-step robotic manipulation, it is important but challenging to predict the future state of the object conditioned on the applied action, especially from the original sensory observation such as images. Successful robotic manipulation requires an accurate predictive model as well as an intricate understanding of the object-environment interactions from high-dimensional images. 

This paper proposes a latent object-centric representation (LOR) that can encode implicit visual features from raw RGB images into a compact and generalizable representation of the object states suitable for future-state prediction. Based on LOR, LOR dynamic neural network (LOR-DNN) is proposed to simultaneously encode object states and predicts the future states with the applied actions of a robot. The learned LOR-DNN can generalize effectively to new situations and can even directly transfer from simulation to the real world. LOR-DNN can be used to plan action sequences to manipulate the object to achieve the target state, allowing the robot to perform multi-step manipulation tasks such as planar pushing. 

Real-world experiments on pushing tasks demonstrate that the proposed method can achieve a high
success rate on pushing previously unseen objects with diverse shapes and scales, outperforming state-of-the-art model-based and end-to-end methods including baselines that use ground-truth object poses. The proposed approach is an important step toward fully autonomous and generalizable visual-based robotic manipulation.