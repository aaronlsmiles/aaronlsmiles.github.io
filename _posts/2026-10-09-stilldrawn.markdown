---
layout: post
title: "StillDrawn: Measuring the Stability of Inked Line Art under Image-to-Video Generation"
date: 2026-10-09 09:00:00 +00:00
image: /images/stilldrawn-violin-drift.jpg
categories: cv
author: "Aaron Smiles"
authors: "<strong>Aaron Smiles</strong>"
venue: "Submitted to arXiv (cs.CV, cross-listed cs.GR), 9 October 2026; in moderation"
code: https://github.com/aaronlsmiles/stilldrawn
video: https://media.studionephele.com/films/v1/stilldrawn-explorer/16x9.mp4
---
A benchmark for one narrow question: when an image-to-video model animates an inked comic or manga panel, does the result still look drawn? StillDrawn pairs a 29-panel dataset (each panel with its line-art layer and generation recipe) with five automatic line-stability metrics and a pre-registered study of five video engines, two open-weights and three hosted. The pre-registered hypothesis returned null and is reported as registered. The failure taxonomy that emerged instead includes modes that stay in ink to a human eye while the metrics flag them, and modes the metrics barely see. A six-rater human check supports the metrics on content preservation; the absolute ink-register judgement proved weaker. An optical-flow control shows that engine rankings largely track how much each engine moves. The dataset, recipes and metrics are public on <a href="https://doi.org/10.5281/zenodo.23072784">Zenodo</a> and <a href="https://github.com/aaronlsmiles/stilldrawn">GitHub</a>.
