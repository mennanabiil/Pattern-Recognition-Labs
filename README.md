# Pattern Recognition Labs — Image Processing, Classification & PCA

A collection of course laboratory exercises in image processing and pattern recognition, progressing from image enhancement and thresholding to supervised classification and dimensionality reduction.

## Repository structure

| Lab | Focus | Techniques |
| --- | --- | --- |
| **01 — Blood Smear Generation & Enhancement** | Synthetic peripheral blood-smear image generation and enhancement | Grayscale, histograms/CDF, equalization, CLAHE, spatial filtering, Otsu thresholding, morphology and segmentation (per the existing Lab 1 project description) |
| **02 — Image Thresholding** | OpenCV thresholding on an input image | Fixed/global binary threshold, adaptive Gaussian thresholding, Otsu's threshold |
| **03 — Classification Models** | Supervised classification on the `sklearn` breast cancer dataset | KNN, Gaussian Naive Bayes, QDA, feature scaling, stratified cross-validation, hyperparameter tuning, confusion matrices, ROC-AUC |
| **04 — PCA & Dimensionality Reduction** | Analyze variance, feature loadings and classifier performance | PCA, explained variance, 2D projection, PCA+KNN pipelines, cross-validation and sensitivity comparisons |

**Lab 1:** Move the three existing root files (`PatternLab1MennaNabil.pdf`, `PatternLab1_Menna_Nabil.ipynb`, and the old blood-smear `README.md`) into `Lab-1/`. The README at the repository root should describe all four labs.

## Selected results from the uploaded notebooks

- **Lab 3:** Tuned QDA achieved **95.24% malignant-class sensitivity** on a held-out test split (40/42 malignant cases detected); its reported ROC-AUC was **0.9921**. These results describe an educational benchmark on one dataset and split, not a clinically validated diagnostic system.
- **Lab 4:** PCA retained **95.27%** of variance with **10 of 30 components**. In the baseline KNN (`k=5`) comparison, the PCA and no-PCA pipelines both achieved **95.61%** test accuracy, demonstrating that dimensionality reduction did not improve classification accuracy in that comparison.

## Running the notebooks

1. Install Python and Jupyter, then install the dependencies in `requirements.txt`.
2. Open each `.ipynb` notebook in Jupyter, VS Code, or Colab.
3. **Lab 2:** provide an `image.jpg` file in the working directory, or update the `cv2.imread('image.jpg')` path to your own image. The original image was not included in the supplied materials.
4. **Labs 3–4:** use `sklearn.datasets.load_breast_cancer`; no separate dataset download is required.

The notebooks are preserved as supplied; this repository layout does not modify the original experiments or claim additional validation.
