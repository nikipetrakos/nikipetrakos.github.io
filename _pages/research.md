---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
redirect_from:
  - /research
---

For a full list of my publications, please refer to my [Google scholar](https://scholar.google.com/citations?user=m9bPEe0AAAAJ&hl=en).

## Realistic Synthetic Data for Trial Design
My PhD research was centered on developing frameworks for generating complex and realistic synthetic data in the context of randomized controlled trials (RCTs) in order to better inform trial design. With the ultimate goal of more flexibly powering Sequential Multiple Assignment Randomized Trials (SMARTs), which have great utility in informing personalized medicine, the first step was to determine how best to generate realistic trial data, which could then be harnessed to power trial designs in simulation.

### Generating Realistic RCT Data
By comparing different generative algorithms (deep learning or otherwise) as well as different decisions regarding data pre-processing, simultaneous or sequential modeling, and ways to induce further randomness in the generated data, I compared several data generation frameworks and end with a recommendation for generating realistic RCT data. This work has been published and can be read [here](https://onlinelibrary.wiley.com/doi/full/10.1002/sim.70227). The code is also readily available on my [Github repository](https://github.com/nikipetrakos/SyntheticDataGeneration).

### Accounting for Missingness Mechanisms in Synthetic RCT Data
After a deep dive into the data generation literature, it became clear that completely ignoring the role of missing data in the generation of synthetic data (RCT or not) was common practice. However, this is inherently problematic in the trial setting since it is generally understood that missingness in trials is non-ignorable. Thus, fitting generative models to only the subset of real data that is completely observed will generate synthetic data representing a cohort of participants that is systematically different from the entire study population, and thus from the population of interest as well. I tackled this issue by further extending my proposed framework to handle Missing at Random mechanisms. This work is under review but the [preprint is accessible](https://arxiv.org/abs/2512.00183).

### Simulation-based Design of Sequential Multiple Assignment Randomized Trials (SMARTs)
Now equipped with a way to generate adequately realistic synthetic trial data while also accounting for missing data mechanisms, I tackled the problem of powering SMARTs for the comparison of embedded dynamic treatment regimes (also referred to as adaptive interventions or strategies). The most user-friendly approach to powering SMARTs with the aim of comparing entire treatment strategies (and not just single-stage, static treatment options) is to use rather simplistic formulae implemented through sample size calculators, however these formulae require strong assumptions. To sidestep these assumptions, I developed a method that fits generative models to pilot SMART data such that multiple competing designs can be compared in simulation. While this paper is under review, it is also available as a [preprint](https://arxiv.org/abs/2607.21751).
