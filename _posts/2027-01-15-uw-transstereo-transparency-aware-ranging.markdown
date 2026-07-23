---
layout: post
title: "Contour-Anchored Transparency-Aware Ranging for Underwater Stereo: Foundation Matchers, Flat-Port Refraction, and a Negative Result for Homogenisation"
date: 2027-01-15 10:00:00 +00:00
image: /images/uwts_e03_headline.png
abstract: /pdfs/pubs/UW-TransStereo_Extended_Abstract.pdf
categories: cv
author: "Aaron Smiles"
authors: "<strong>Aaron Smiles</strong>"
venue: "Journal 2027 (TBC)"
---
Transparent objects defeat stereo matching — a conventional matcher sees through the surface and assigns the object its background disparity, a failure characterised by Wu et al. (ICRA 2023) as a corner case in stereo. Underwater the problem compounds: a flat air–water port refracts the optical path and biases every uncorrected depth estimate, while turbidity and backscatter collapse detection confidence. No published work addresses transparent-object stereo ranging underwater; the nearest neighbours handle underwater stereo without transparency, or transparency in air. This work builds on the <a href="https://zenodo.org/doi/10.5281/zenodo.16753748">UW-TransStereo dataset</a>, to our knowledge the only real-world dataset at that intersection.

We report three connected results over 1,378 stereo frames, evaluated against tape ground truth on held-out transparent bottles in water (n=249, from recordings disjoint from those used for calibration).

**Zero-shot foundation matchers recover transparent surfaces.** FoundationStereo, StereoAnywhere and RAFT-Stereo, applied without fine-tuning, track the true range of transparent bottles underwater where classical block matching does not — correlation against tape ground truth on raw uncorrected depth of r = 0.986, 0.991 and 0.989 respectively, against r = −0.006 for SGBM. The premise that transparent surfaces are unmatchable does not hold for these models.

**A matcher-independent flat-port correction makes the reading metric.** Refraction through the flat port is well modelled by an affine correction with n<sub>eff</sub> ≈ 1.36. Fitted on an opaque control object and transferred leave-one-environment-out across water conditions, it reduces mean absolute error from 97 mm to 12.1 mm, beating the camera SDK's own neural depth at 28.5 mm. All three matchers independently refit n<sub>eff</sub> to 1.35–1.39, and the ratio of in-water to in-air checkerboard focal length (1.325) confirms the same port scale from calibration alone.

**Contour-anchored sampling beats the baseline and halves the tail.** Given a matcher that already reads the surface, the remaining error lies in where on the object the disparity is sampled. Our method segments the bottle, samples the raw dense disparity across its interior, and uses the depth step at the silhouette contour to classify surface-versus-see-through reads before pooling.

| Method | MAE (mm) | p90 (mm) | 600–900 mm band |
|---|---|---|---|
| StereoAnywhere centre-pixel (baseline) | 15.0 | 27.6 | 29.7 |
| Raw interior median (pooling only) | 11.1 | 18.4 | 26.0 |
| TA-Stereo homogenisation | 12.5 | 16.1 | 28.0 |
| **Contour depth-step (ours)** | **9.7** | **15.3** | **24.7** |

The method beats the baseline on 80.7% of frames, with placement-level Wilcoxon p = 1e-4. An ablation ladder separates the mechanisms: robust interior pooling carries 74% of the gain, the depth-step surface classifier the remaining 26%. The improvement is attributable to the estimator rather than auxiliary priors — zeroing the known-dimension offset still yields 10.0 mm MAE, and the refitted n<sub>eff</sub> is unchanged from the baseline's, so it is not a disguised refraction refit.

**A negative result, disclosed.** We reimplemented TA-Stereo homogenisation — masking the transparent region and filling it with boundary statistics so the matcher treats it as opaque — and it does not help, at 12.5 mm MAE against 11.1 mm for simply pooling the raw interior. Adversarial verification corrected our own first-pass explanation: homogenisation does not destroy the signal, but reads systematically nearer, carrying a −11.7 mm bias through the ranging protocol. The lesson generalises. TA-Stereo's premise is to opacify because the matcher fails on transparent surfaces, and that premise is void once the matcher already reads them.

<em>Limitations: results are in-distribution over a 200–800 mm working range on a single camera and port geometry. One water condition ties with rather than beats the baseline, and the 600–900 mm band remains the weakest for every method tested.</em>

<em>Manuscript in preparation. Extends the UW-TransStereo dataset (Zenodo DOI 10.5281/zenodo.16753748), funded by UKRI grant 2601988.</em>
