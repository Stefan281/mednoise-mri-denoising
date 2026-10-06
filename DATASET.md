# Dataset

This project uses version 2 of the [Brain Tumor MRI Dataset](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset), curated by Masoud Nickparvar and published on Kaggle.

The dataset is distributed under the [Creative Commons Attribution 4.0 International license](https://creativecommons.org/licenses/by/4.0/). It combines images from the following public datasets:

- [Figshare brain tumor dataset](https://figshare.com/articles/dataset/brain_tumor_dataset/1512427)
- [SARTAJ Brain Tumor Classification dataset](https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumor-classification-mri)
- [Br35H Brain Tumor Detection dataset](https://www.kaggle.com/datasets/ahmedhamada0/brain-tumor-detection)

## Use in this project

The original dataset is not included in this repository. The notebook downloads it directly from Kaggle, or it can read an existing local copy through the `MEDNOISE_DATA_DIR` environment variable.

The experiment makes the following changes to the source images:

- conversion to single-channel grayscale;
- resizing to 224 × 224 pixels;
- addition of synthetic Rician noise;
- horizontal flips and small rotations for training augmentation;
- generation of denoised comparison figures.

Any example images included in `results/samples/` are derived from the source dataset and remain subject to its CC BY 4.0 license.

The dataset contains medical images and is used here only for research and education. The model and its outputs are not intended for clinical diagnosis.
