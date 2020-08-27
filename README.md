# PigmentedSkinLesion-Classification

## About
- This repository uses the [HAM10000 dataset](https://doi.org/10.7910/DVN/DBW86T) for classification of Pigmented Skin Lesions into one of the seven categories: Actinic keratoses and intraepithelial carcinoma / Bowen's disease (`akiec`), basal cell carcinoma (`bcc`), benign keratosis-like lesions (solar lentigines / seborrheic keratoses and lichen-planus like keratoses- `bkl`), dermatofibroma (`df`), melanoma (`mel`), melanocytic nevi (`nv`) and vascular lesions (angiomas, angiokeratomas, pyogenic granulomas and hemorrhage - `vasc`)
- The `skin_cancer_detection.ipynb` notebook contains comprehensive documentation in support of the code and contains a "Conclusion" section at the end to sum up the Accuracy and F1 scores achieved using various architectures and methodologies.
- Best score achieved: Training Accuracy: 99.29%, Testing Accuracy: 98.89%; Training F1 Score: 97.51%, Testing F1 Score: 96.10%
- Architecture for Best Score: `DenseNet-121` trained for epochs = 50 using learning rate annealing for loss optimization, on the Image Tensor data and then using `LightGBM` for classification into 7 classes using features as P(Class / Image Tensor) + Meta-Data of Patient.

## Data
- Download the [Data](https://doi.org/10.7910/DVN/DBW86T) from here and combine both the .zip files (HAM10000_images_part1.zip (5000 JPEG files), HAM10000_images_part2.zip (5015 JPEG files)) into one folder named `HAM10000_images`
