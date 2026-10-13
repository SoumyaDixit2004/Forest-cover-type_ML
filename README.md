# Forest-cover-type_ML
# Forest Cover Type Classification Using Machine Learning

## Project Overview
This project uses machine learning to predict forest cover types based on cartographic and environmental features. It follows the Knowledge Discovery in Databases (KDD) process, from data understanding and preprocessing to model development, evaluation, and interpretation.

## Problem Statement
Forest cover types vary according to environmental and geographical characteristics. The objective is to develop a classification model that predicts the forest cover type using features such as elevation, slope, distances to water bodies and roads, hillshade measurements, soil types, and wilderness areas.

## Objectives
- Understand and preprocess the forest cover dataset.
- Perform exploratory data analysis and visualize feature patterns.
- Train and compare multiple classification algorithms.
- Evaluate models using appropriate classification metrics.
- Identify important features and interpret model predictions.

## Dataset
**Name:** UCI Covertype Dataset

**Source:** https://archive.ics.uci.edu/dataset/31/covertype

The dataset contains cartographic features and seven forest cover classes. The target variable represents the predicted forest cover type.

The notebook loads the dataset using Scikit-learn's `fetch_covtype` function. An internet connection may be required for the initial download.

## Methodology: KDD Process
1. **Data Selection:** Load the UCI Covertype dataset.
2. **Data Understanding:** Examine features, data types, missing values, duplicates, and class distribution.
3. **Data Preprocessing:** Prepare input features and target labels, and split the data into training and testing sets.
4. **Exploratory Data Analysis:** Visualize class distribution and relationships between environmental features.
5. **Model Development:** Train a Dummy Classifier, Decision Tree, Random Forest, and K-Nearest Neighbors (KNN).
6. **Evaluation:** Compare accuracy, macro precision, macro recall, macro F1-score, and confusion matrices.
7. **Interpretation:** Examine class-wise performance and feature importance.

## Algorithms Used
- Dummy Classifier — baseline comparison
- Decision Tree Classifier
- Random Forest Classifier
- K-Nearest Neighbors (KNN)

## Evaluation Metrics
- Accuracy
- Macro-averaged Precision
- Macro-averaged Recall
- Macro F1-score
- Confusion Matrix

## Project Structure
```text
Forest-cover-type_ML/
├── Forest_Cover_Type_Classification.ipynb
├── README.md
├── requirements.txt
└── data/
    └── README.md
```

The dataset can be downloaded automatically through Scikit-learn or obtained from the official UCI source. Large dataset files do not need to be committed to GitHub.

## Installation and Execution

1. Install Python 3.10 or a compatible version supported by the installed Scikit-learn release.
2. Clone or download this repository.
3. Install the required libraries:

   ```bash
   pip install -r requirements.txt
   ```

4. Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

5. Open `Forest_Cover_Type_Classification.ipynb` and run the cells in order.

The notebook uses a stratified sample of 80,000 records by default to reduce computation time. The reported evaluation results should be described as results on that sample unless the experiment is rerun on the complete dataset.

## Results and Discussion
After executing the notebook, record the actual model evaluation scores and identify the best-performing model based on the selected metric. Discuss class-wise errors, the confusion matrix, and important features.

No performance values are reported here because they must be obtained by running the experiments.

## Limitations
- Results depend on the selected training and test data.
- Some forest cover classes may be more difficult to distinguish than others.
- Training time and memory requirements vary by algorithm.
- Performance on this dataset does not guarantee generalization to other geographical regions.

## Conclusion
This project demonstrates an end-to-end predictive analytics workflow for forest cover classification. It applies the KDD process, compares machine learning algorithms, evaluates classification performance, and interprets the model's findings.

## References
1. UCI Machine Learning Repository. Covertype Dataset. https://archive.ics.uci.edu/dataset/31/covertype
2. Scikit-learn Developers. `fetch_covtype` documentation. https://scikit-learn.org/stable/modules/generated/sklearn.datasets.fetch_covtype.html
3. Blackard, J. A., & Dean, D. J. (1999). Comparative accuracies of artificial neural networks and discriminant analysis in predicting forest cover types from cartographic variables. *Computers and Electronics in Agriculture, 24*(3), 131–151.
