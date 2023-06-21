---
layout: post
title:  "Stereo Vision for Mixed Reality Human-Robot Perception"
date:   2022-11-02 22:21:59 +00:00
image: /images/sv1.png
image2: /images/matScatter.png
categories: cv
author: "Aaron Smiles"
authors: "<strong>Aaron Smiles</strong>"
code: https://github.com/aaronlsmiles/StereoPerception
---
Using an experimental stereo vision camera rig to obtain object depth in land-based and underwater experiments for providing mixed reality feedback to remote robot operators on distance from the end effector to objects for assisted grasping. Scenarios that are considered include search and rescue, nuclear engineering, subsea engineering, and space robotics.

Various objects and backgrounds are tested during experiments and found that environments that are dense in keypoints perform better for block-matching. Scenes and/or objects with few keypoints are more difficult to estimate depth. Masks can be used to avoid this problem for objects. However, scenes with few keypoints or limited keypoint diversity appear to be the biggest contributor to poor depth estimation. 

Such scenes, with few keypoints, are common in underwater worlds, so future work would investigate SOTA vision transformers for stereo matching for improving block-matching in scenes with limited keypoints. 
