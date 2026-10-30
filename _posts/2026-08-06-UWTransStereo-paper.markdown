---
layout: post
title: "Descriptor: Underwater Stereo Vision Dataset for Transparent Object Detection & Ranging (UW-TransStereo)"
date: 2026-08-06 22:21:59 +00:00
image: /images/bottle_rmse_heatmaps.png
paper: /pdfs/phd_pubs/IEEE_DATA_Descriptor__Underwater_Stereo_Vision_Dataset_for_Transparent_Object_Detection___Ranging__UW_TransStereo_.pdf
categories: cv
author: "Aaron Smiles, Changjae Oh, and Ildar Farkhatdinov"
authors: "<strong>Aaron Smiles</strong>, Changjae Oh, Ildar Farkhatdinov"
venue: "IEEE Data Descriptions, vol. 3, pp. 638–645, 2026"
doi: https://doi.org/10.1109/IEEEDATA.2026.3721416
---
Robust detection and ranging of transparent debris in water is challenging due to refraction, low contrast, backscatter, and turbidity. We present a paired, multi-environment stereo dataset acquired with a stereo camera, comprising 25 recordings totalling over 9,000 stereo frame pairs of three bottle targets (two transparent plastic bottles with filled/unfilled variants and a brown glass medicine bottle) across air and four underwater conditions (freshwater, freshwater with enhancement, saltwater, and saltwater with suspended pellets), along with analysis-ready detector spreadsheets and scripts. To promote reproducible use, we provide a standard evaluation protocol with well-defined accuracy measures (MAE, RMSE, R², and mean signed error) and report the proportion of frames with valid estimates, including vertical region-of-interest sampling. We include a lightweight vision enhancement variant, "basicEnhance", to illustrate how pre-processing can be benchmarked against the same protocol without retraining models. The release is intended as a neutral testbed for benchmarking underwater transparent-object perception and for stress-testing stereo ranging under refractive media. We release all raw stereo streams, detector outputs, qualitative screenshots, and analysis scripts.
