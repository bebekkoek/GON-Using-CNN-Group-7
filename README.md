# Quality-Aware Convolutional Neural Network for Glaucoma Detection

This repository contains the code and methodology for detecting Glaucomatous Optic Neuropathy (GON) using retinal fundus images. This project was developed as a group assignment for the **MAA62052** course at Universitas Brawijaya.

## Overview
The goal of this project is to build a Deep Learning pipeline that classifies fundus images into **GON+** and **GON-**. We explicitly explore a **Quality-Aware Modeling Strategy** by utilizing image quality scores to handle noisy and low-quality data. 

## Prerequisites
To reproduce the results, ensure you have Python 3.8+ installed. Install the required dependencies using the following command in your terminal:

    pip install -r requirements.txt

## Dataset Preparation
This project uses the **Hillel Yaffe Glaucoma Dataset (HYGD)**.
1. Download the dataset (version 1.0.0) from [PhysioNet HYGD](https://physionet.org/content/hillel-yaffe-glaucoma-dataset/1.0.0/).
2. Extract the `.zip` file.
3. Place the extracted `Images/` folder and `Labels.csv` file into the `data/` directory, or upload the `.zip` directly if running via Google Colab.

## How to Run (Reproducibility)
The entire pipeline is consolidated into a Jupyter Notebook (`PPM_Group 7.ipynb`).
1. Open the notebook using Jupyter, JupyterLab, or Google Colab.
2. **If using Google Colab:** Ensure the runtime is set to **GPU (T4)** for faster training.
3. Run the notebook sequentially. It will automatically handle the patient-level split (70/15/15), start the training loop, and output the metrics.
4. All generated plots (EDA, Confusion Matrix) will be saved in `outputs/figures/`, and trained model weights will be saved in `outputs/models/`.

## Repository Structure
* `PPM_Group 7.ipynb`: The main notebook containing preprocessing, modeling, training loops, and evaluation.
* `requirements.txt`: Python package dependencies.
* `data/`: Folder to store the dataset (not tracked by git, place your extracted dataset here).
* `outputs/`: Directory where generated files and model weights are saved.

## References
Abramovich, O., Pizem, H., Fhima, J., Berkowitz, E., Gofrit, B., Van Eijgen, J., Blumenthal, E., & Behar, J. (2025). *Hillel Yaffe Glaucoma Dataset (HYGD): A Gold-Standard Annotated Fundus Dataset for Glaucoma Detection* (version 1.0.0). PhysioNet. https://doi.org/10.13026/z0ak-km33
