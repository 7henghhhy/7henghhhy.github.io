---
layout: page
title: Dinosaur SfM
permalink: /projects/incremental-3d-reconstruction/
description: 62-view 3D reconstruction with sparse bundle adjustment, measured ablations, and an interactive viewer.
img: assets/img/projects/dino-reconstruction.png
importance: 1
category: research
---

An incremental **Structure from Motion (SfM)** course project that reconstructs a dinosaur exhibit from 62 calibrated photographs.

[Interactive 3D demo](https://7henghhhy.github.io/reconstrct-dino/) · [Source code](https://github.com/7henghhhy/reconstrct-dino) · [Dataset](https://github.com/7henghhhy/reconstrct-dino/releases/tag/dinosaur-data-v1)

![Reconstructed dinosaur exhibit with camera and point-cloud controls]({{ '/assets/img/projects/dino-reconstruction.png' | relative_url }})

The modular Python pipeline uses OpenCV SIFT features, mutual ratio matching and RANSAC, essential-matrix initialization, incremental PnP registration, triangulation, and sparse bundle adjustment in SciPy. The viewer lets visitors inspect reconstruction stages, camera poses, and input photographs, and download the recovered geometry.

**Recorded results:** 62/62 registered cameras and 33,383 exported points. On the same 166,948 observations at 1600 × 1200 resolution, bundle adjustment reduced mean reprojection error from **0.648 to 0.345 pixels**. The solver reached its `ftol` stopping criterion after 80 evaluations. The repository also compares runs without BA, with half the images, and with chained essential-matrix poses.

**What the measurements establish:** improved image-space consistency for this reconstruction. The sparse point cloud has arbitrary scale and limited surface coverage; no ground-truth poses or geometry were available to measure absolute 3D accuracy. This project does not provide a dense surface reconstruction or a complete SLAM system.

**Technologies:** Python, OpenCV, NumPy, SciPy, Open3D, multi-view geometry, sparse bundle adjustment, JavaScript.
