---
layout: about
title: about
permalink: /
subtitle: Computer Engineering junior at U-M · Robot perception and 3D vision

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>Ann Arbor, MI 48105</p>
    <p><a href="mailto:hyzh@umich.edu">hyzh@umich.edu</a></p>

selected_papers: false # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: false # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

I am a Computer Engineering junior at the University of Michigan and an Electrical and Computer Engineering student at Shanghai Jiao Tong University through the UM-SJTU Joint Institute. My interests include robot perception, visual SLAM, and 3D scene representations.

At Michigan Mars Rover (MRover), I work on the rock-pick perception task. My recent work focuses on CoTracker3-assisted keypoint annotation, human review, and preparing data for pose-model training. [MRover project and code]({{ '/projects/mrover-rockpick/' | relative_url }}).

My 3D vision work includes Dinosaur SfM, an incremental reconstruction pipeline using SIFT matching, RANSAC, PnP, triangulation, and sparse bundle adjustment. The recorded reconstruction registers all 62 cameras, and I evaluated the effects of bundle adjustment, image sampling, and pose-estimation choices. [Project and code]({{ '/projects/incremental-3d-reconstruction/' | relative_url }}) · [Interactive 3D demo](https://7henghhhy.github.io/reconstrct-dino/).

I previously developed C2-MANS, a neuro-symbolic multi-agent system for long-form narrative generation. It combines LLMs with structured state models to maintain consistency across chapters, using CrewAI and Pydantic. [C2-MANS project]({{ '/projects/c2-mans/' | relative_url }}).

I work primarily with Python and C/C++, using OpenCV, NumPy/SciPy, PyTorch, Git, and Linux.
