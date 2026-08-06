---
title: Computational Modeling and Analysis
weight: 2
summary: |
    *Connecting molecular behavior and macroscopic measurements*

    We use computational methods to predict and interpret relaxometry and other measurements done using single-sided magnets. We also actively pursue better methods to analyze relaxometry data in context of particular applications.
subtitle: Connecting molecular behavior and macroscopic measurements
show_date: false
image:
    preview_only: true
    # Use Hugo's image processing
    # This will output a 400px-wide image (maintains aspect ratio)
    filename: featured.webp
---

Single-sided NMR relaxometry gives decay curves, not spectra. A single decay is easy to interpret, but real samples usually produce several overlapping decays at once, and separating them in the presence of noise doesn't have one single best answer. For single-sided measurements, it's usually the *interpretation* of the data that limits what we can conclude, not the instrument itself — which is what this branch of the lab is about, from three angles: extracting more from the data we measure, predicting what that data should look like in the first place, and using those predictions to classify unknown samples.

Working with Prof. Daniel Vasiliu (W&M Data Science), we've developed and implemented an analysis method based on the penalized Euclidean distance (PED) algorithm, which needs no human decision-making to handle noisy data and finds the sparsest fit that remains accurate.

The second turns the problem around: rather than extract more from a decay we measured, we try to predict what the decay *should* look like in the first place. Since 2022, we've developed molecular dynamics (MD) code that predicts the NMR relaxation behavior of small molecules, alone or in mixtures, extending it to handle the strongly inhomogeneous magnetic fields of single-sided instrumentation. Along the way, this code has turned up physics we weren't looking for: relaxation properties vary non-linearly with mixture composition in a way that closely parallels classic thermodynamic data on the enthalpy of mixing — suggesting that intermolecular forces show up similarly in calorimetry and in NMR relaxometry. We're actively pursuing that connection now.

Our primary computational direction now is using these predictions for broad chemical classification — correlating our MD results with machine-learning models, with support from a three-year grant from the American Chemical Society's Petroleum Research Fund.