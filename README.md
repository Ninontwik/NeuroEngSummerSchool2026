# Hands-on: Building Digital Twins of hiPSC Neuronal Networks

**Neuroengineering Summer School "Massimo Grattarola", Camogli — June 2026**
*Session: Digital Twins — Multiscale Computational Models*

---

## Overview

This repository contains the hands-on material for the computational modelling
session of the summer school. The session is part of the broader theme of
building digital twins of patient-derived neural models — here applied to
**hiPSC-derived neuronal networks on multi-electrode arrays (MEAs)**.

We build a biophysical network model that reproduces the spontaneous bursting
activity characteristic of these cultures, compare simulated and experimental
MEA recordings, and use **Simulation-Based Inference (SBI)** to infer
biological parameters directly from the data — a key step toward
personalised computational models.

No local installation is required. Everything runs in Google Colab in your browser.

---

## Contents

```
notebook_1_model.ipynb      Part 1: Exploring the network model
notebook_2_sbi.ipynb        Part 2: Simulation-Based Inference
data/
    spike_data_healthy.csv  Spike-sorted MEA recording — healthy culture
    spike_data_disease.csv  Spike-sorted MEA recording — disease culture
    inference.pkl           Pre-trained NPE posterior
```

---

## Open in Colab

Click the buttons below to open each notebook directly in Google Colab.
You will need a Google account. No other setup is required — all dependencies
are installed automatically when you run the first cell.

**Part 1 — Exploring the network model**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ninontwik/NeuroEngSummerSchool2026/blob/main/notebook_1_model.ipynb)

Build and run an Adaptive Exponential Integrate-and-Fire network, explore how
biological parameters shape network dynamics, compare simulations to
experimental MEA recordings, and try to find the parameters that reproduce
a disease phenotype.

**Part 2 — Simulation-Based Inference**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ninontwik/NeuroEngSummerSchool2026/blob/main/notebook_2_sbi.ipynb)

Use a pre-trained Neural Posterior Estimator (NPE) to infer network parameters
from experimental recordings. Explore how feature choice affects the posterior,
and investigate what each summary feature encodes about the underlying biology.

---

## Background

The hands-on session is part of the summer school
**"Bridge the Gap: Multiscale Approaches in Neurodevelopmental Disorders"**,
which offers multidisciplinary training on the study of neurodevelopmental
disorders using patient-derived in vitro models, in vivo platforms, and
computational approaches. This session focuses on the computational modelling
component — specifically how biophysical models of hiPSC neuronal networks
can be combined with modern inference methods to extract biological insight
from MEA recordings.

---

## Dependencies

All dependencies are installed automatically in Colab. 

If you prefer to work locally rather than in Colab:

    conda env create -f environment.yml
    conda activate summerSchool2026
    jupyter notebook

Then download the notebooks and data files from this repository and skip
the setup cell at the top of each notebook.

---

## Contact

Nina Doorn
Postdoctoral Researcher at ETH Zürich
Laboratory of Biosensors and Bioelectronics (LBB)
ndoorn@ethz.ch
