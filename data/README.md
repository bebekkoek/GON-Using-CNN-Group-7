## Overview

This dataset contains 747 Deep Fundus Images (DFIs) annotated for glaucomatous optic neuropathy (GON) and accompanied by quality scores.
The dataset is structured into an image folder and a labels file providing metadata and annotations.

## Dataset Structure

### 1. Images

- Located in the `Images/` folder.
- Contains 747 DFIs in JPG format with a 1:1 aspect ratio.
- Image naming convention: `x_y.jpg`
  - `x`: Patient ID (starting from 1)
  - `y`: Image number per patient (starting from 0)
  - Example: `188_1.jpg` → Second image of patient 188.

### 2. Labels File (`Labels.csv`)

A CSV file containing metadata and annotations for each image. It includes the following columns:

| Column Name   | Description                                                                |
| ------------- | -------------------------------------------------------------------------- |
| Image Name    | Filename of the DFI (e.g., `188_1.jpg`).                                   |
| Patient       | Unique patient ID.                                                         |
| Label         | Binary classification: `GON+` (glaucomatous) or `GON-` (non-glaucomatous). |
| Quality Score | Score ranging from 1 to 10.              				     |

## Dataset Statistics

- Total Images: 747
- Glaucomatous DFIs (GON+): 548
- Non-Glaucomatous DFIs (GON-): 199

## Citation

If you use this dataset in your research, please cite the following:

"Abramovich O, Pizem H, Fhima J, Berkowitz E, Gofrit B, Meisel M, et al. (2025). Hillel Yaffe Glaucoma Dataset (HYGD) (version 1.0.0). PhysioNet. https://doi.org/10.13026/z0ak-km33
"Abramovich O, Pizem H, Fhima J, Berkowitz E, Gofrit B, Meisel M, et al. GONet: A Generalizable Deep Learning Model for Glaucoma Detection [Internet]. arXiv.org. 2025."

Additionally, if you use the quality scores in your research, please cite the following:
"Abramovich O, Pizem H, Eijgen JV, Oren I, Melamed J, Stalmans I, et al. FundusQ-Net: A regression quality assessment deep learning algorithm for fundus images quality grading. Comput Methods Programs Biomed. 2023;239:Art. no. 107522."

## Contact

For any inquiries, please contact the corresponding author at orabramovich@campus.technion.ac.il.

## Dataset Preparation
This project uses the Hillel Yaffe Glaucoma Dataset (HYGD).
1. Download the dataset (version 1.0.0) from PhysioNet HYGD.
2. Extract the .zip file.
3. Place the extracted Images/ folder and Labels.csv file into the data/ directory, or upload the .zip directly if running via Google Colab.

## How to Run (Reproducibility)
The entire pipeline is consolidated into a Jupyter Notebook (PPM_Group 7.ipynb).
1. Open the notebook using Jupyter, JupyterLab, or Google Colab.
2. If using Google Colab: Ensure the runtime is set to GPU (T4) for faster training.
3. Run the notebook sequentially. It will automatically handle the patient-level split (70/15/15), start the training loop, and output the metrics.
4. All generated plots (EDA, Confusion Matrix) will be saved in outputs/figures/, and trained model weights will be saved in outputs/models/.

## Repository Structure
- PPM_Group 7.ipynb: The main notebook containing preprocessing, modeling, training, and evaluation.
- requirements.txt: Python package dependencies.
- data/: Folder to store the dataset (not tracked by git).
- outputs/: Directory where generated files and model weights are saved.

References
Abramovich, O., Pizem, H., Fhima, J., Berkowitz, E., Gofrit, B., Van Eijgen, J., Blumenthal, E., & Behar, J. (2025). Hillel Yaffe Glaucoma Dataset (HYGD): A Gold-Standard Annotated Fundus Dataset for Glaucoma Detection (version 1.0.0). PhysioNet.
