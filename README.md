# Quality-Aware Convolutional Neural Network for Glaucoma Detection

This repository contains the code and methodology for detecting Glaucomatous Optic Neuropathy (GON) using retinal fundus images. This project was developed as a group assignment for the **MAA62052** course at Universitas Brawijaya.

## Overview
The goal of this project is to build a Deep Learning pipeline that classifies fundus images into **GON+** and **GON-**. We explicitly explore a **Quality-Aware Modeling Strategy** by utilizing image quality scores to handle noisy and low-quality data. 

The repository implements:
1. Patient-level dataset splitting to prevent data leakage.
2. A Custom CNN (Baseline).
3. A Quality-Aware Custom CNN (using sample weighting based on quality scores).
4. A pre-trained ResNet18 model for transfer learning comparison.

## Prerequisites
To reproduce the results, ensure you have Python 3.8+ installed. Install the required dependencies using:
```bash
pip install -r requirements.txt
