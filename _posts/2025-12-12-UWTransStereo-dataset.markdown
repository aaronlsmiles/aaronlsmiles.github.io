---
layout: post
title: "UW-TransStereo: Underwater Stereo Vision Dataset for Transparent Object Detection & Ranging"
date: 2025-12-12 22:21:59 +00:00
image: /images/TODO-add-dataset-thumbnail.jpg  # TODO: Add thumbnail image for dataset
categories: datasets
author: "Aaron Smiles, Ildar Farkhatdinov, and Changjae Oh"
authors: "<strong>Aaron Smiles</strong>, Ildar Farkhatdinov, Changjae Oh"
venue: "Zenodo"
doi: https://zenodo.org/doi/10.5281/zenodo.16753748
paper: /pdfs/phd_pubs/IEEE_DATA_Descriptor__Underwater_Stereo_Vision_Dataset_for_Transparent_Object_Detection___Ranging__UW_TransStereo_.pdf
---
This stereo vision dataset addresses the challenge of detecting transparent underwater debris. The collection includes 25 paired stereo vision recordings totalling over 9,000 stereo frame pairs across air and four aquatic environments. Coverage encompasses three bottle types tested under various conditions (freshwater, freshwater with enhancement, saltwater, saltwater with suspended pellets). The dataset provides over 5,000 labeled measurements, per-frame detections, and dimension estimates (height x width x depth). A standardized evaluation protocol uses MAE, RMSE, R-squared, and bias metrics. The system features real-time YOLO-based object detection (YOLOv5/YOLOv8), 3D depth integration with ZED stereo cameras, object dimension measurement capabilities, multi-point distance sampling, real-time Excel export with timestamps, screenshot capture with distance markers, SVO recording support, and OpenGL 3D visualization.
