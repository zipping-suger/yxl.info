---
title: "Learning Tool-aware Motion Planning with Analytical Policy Gradient"
summary: A neural motion planner that leverages differentiable simulation to adapt to new environments without expert demonstrations, while explicitly handling tool geometry.
tags:
  - Neural Motion Planning
  - Analytical Policy Gradient
  - Robot Manipulation
  - Tool-Aware
date: '2025-11-25T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Method Overview
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

Collision-free motion generation is a core building block for robot manipulation, yet it remains a significant challenge. Traditional methods like RRT or optimization-based planners (e.g., CuRobo) are often computationally expensive and struggle with real-time requirements in cluttered environments. While emerging Neural Motion Planners promise faster inference, they suffer from compounding errors, poor generalization to new environments, and a heavy reliance on expensive expert demonstrations.

To address these limitations, this project introduces a **Tool-Aware Neural Motion Planner** trained via **Analytical Policy Gradient (APG)**. Developed at the Robotic Systems Lab (RSL) at ETH Zürich, this method replaces the complex, multi-step planning pipeline with a single end-to-end network.

### Key Innovations

1.  **Tool-Awareness:** Unlike standard neural planners that only check for robot body collisions, our policy explicitly encodes the tool shape as a point cloud. This ensures that the attached tool does not interfere with the environment, a critical requirement for practical manipulation tasks.
2.  **Analytical Policy Gradient (APG) Fine-tuning:** The most significant contribution is a fine-tuning stage that **eliminates the need for expert data**. By leveraging a differentiable simulation with a privileged Signed Distance Field (SDF), we can optimize the policy directly for collision avoidance, target accuracy, and smoothness.

### Results and Impact

We benchmarked this approach against state-of-the-art planners, demonstrating significant improvements:
*   **Speed:** Generating solutions in just **0.48 seconds**, compared to 3.46 seconds for CuRobo.
*   **Data Efficiency:** Achieved higher success rates (81.7%) than leading neural planners (MPINet) while using only **30%** of the pre-training data.
*   **Adaptation:** The system can adapt to completely out-of-distribution scenarios (such as cabinets or bins) without collecting new expert demonstrations. By simply sampling random problems and applying APG, the policy learns to navigate new constraints 150x faster than generating expert datasets.

We deployed the policy on a physical Franka Emika arm using a single RealSense depth camera. The system successfully navigated cluttered environments and reacted instantly to dynamic obstacles, highlighting the potential of differentiable simulation for real-world robotic autonomy.
{{< youtube a3wsjeLreCs >}}
