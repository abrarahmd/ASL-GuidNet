# ASL-GuidNet

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)]()
[![Python](https://img.shields.io/badge/python-3.10%2B-orange.svg)]()
[![Status](https://img.shields.io/badge/status-experimental-yellow.svg)]()

**ASL-GuidNet** — a vision-based deep learning framework for real-time ASL hand detection and interactive guidance.  
This repository contains code, models, datasets pointers, and evaluation scripts used in the paper:

> *ASL-GuidNet: A Vision-Based Deep Learning Framework for Hand Detection and Sign Language Guidance*

## Quick links
- Paper: `paper/` (PDF)
- Notebooks: `notebooks/` (exploratory experiments)
- Demos: `demo/` (real-time demo app)
- Models: `models/` (trained checkpoints)
- Data: `data/` (scripts to download / preprocess)

## Features
- Real-time hand detection optimized for ASL gestures
- Sign classification + corrective guidance module
- Data augmentation and hand-centric tracking pipeline
- Reproducible training and evaluation scripts

## Quickstart (for reviewers)
```bash
# clone
git clone https://github.com/<username>/ASL-GuidNet.git
cd ASL-GuidNet

# create env
python -m venv venv
source venv/bin/activate        # or `venv\Scripts\activate` on Windows
pip install -r requirements.txt

# download sample dataset (small)
bash scripts/download_sample_data.sh

# run a quick demo on webcam (CPU/GPU fallback)
python demo/webcam_demo.py --weights models/checkpoint_best.pth --device cpu
