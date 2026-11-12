---
layout: page
title: MRover Rock-pick Annotation
permalink: /projects/mrover-rockpick/
description: CoTracker3-assisted five-keypoint video annotation, human review, and YOLO Pose dataset export for a rover perception task.
img:
importance: 2
category: research
---

A data preparation workflow for the University of Michigan Mars Rover team's rock-pick perception task. The aim is to prepare five-landmark annotations for downstream pose-model training that can support autonomous grasping.

[Source code](https://github.com/7henghhhy/Mrover-rockpick-detection) · [Open annotation notebook in Colab](https://colab.research.google.com/github/7henghhhy/Mrover-rockpick-detection/blob/main/notebooks/rock_pick_autolabel.ipynb)

The workflow starts with five manually selected landmarks in a video frame, propagates them with pretrained **CoTracker3**, and exports reviewed image/label pairs in **YOLO Pose** format. It handles frame sampling, black-border cropping, coordinate conversion, 640 × 480 output crops, and per-clip ZIP export to Google Drive.

The organized repository includes input and output checks, human rejection of incorrect frames, a final five-visible-landmark rule, a pinned tracker revision, and CPU tests for geometry, label validation, review, and export. Dataset preparation keeps train/validation/test partitions separate by source recording or capture session to avoid leakage between nearby frames.

**Current scope:** annotation tooling and dataset preparation. The public repository does not contain a trained YOLO detector, model accuracy results, or a completed robot deployment. A fresh end-to-end Colab GPU run remains a verification step for the organized notebook.

**Technologies:** Python, PyTorch, CoTracker3, OpenCV, Google Colab, YOLO Pose annotation format.
