---
layout: page
title: MRover Rock-pick Perception
permalink: /projects/mrover-rockpick/
description: YOLO-based rock-pick detection and keypoint estimation, with CoTracker-assisted annotation and ongoing ROS integration.
img:
importance: 2
category: research
---

Keypoint-based perception for the University of Michigan Mars Rover team's autonomous rock-pick retrieval task. A downward-facing USB camera provides images, and the model produces position and keypoint outputs for the grasping subsystem.

[Source code](https://github.com/7henghhhy/Mrover-rockpick-detection) · [Open annotation notebook in Colab](https://colab.research.google.com/github/7henghhhy/Mrover-rockpick-detection/blob/main/notebooks/rock_pick_autolabel.ipynb)

I built an approximately **10,000-frame dataset** using CoTracker-assisted auto-labeling and am training a **YOLO-based keypoint model for rock-pick detection**. Integration with the rover software stack is ongoing through ROS topics and the TF tree.

The workflow starts with five manually selected landmarks in a video frame, propagates them with pretrained **CoTracker3**, and exports reviewed image/label pairs in **YOLO Pose** format. It handles frame sampling, black-border cropping, coordinate conversion, 640 × 480 output crops, and per-clip ZIP export to Google Drive.

The public repository documents the annotation and data preparation workflow, including input and output checks, human rejection of incorrect frames, a final five-visible-landmark rule, a pinned tracker revision, and CPU tests for geometry, label validation, review, and export.

**Technologies:** Python, PyTorch, YOLO, CoTracker3, OpenCV, ROS, TF, Google Colab.
