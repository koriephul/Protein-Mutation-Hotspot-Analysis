# Protein-Mutation-Hotspot-Analysis

## Overview
This project explores mutation-prone amino acid residues (hotspots) within the SARS-CoV-2 Wuhan reference spike protein sequence (YP_009724390.1__) obtained from the NCBI Protein database. A dataset of 50 SARS-CoV-2 spike protein sequences was aligned to the Wuhan reference sequence to identify amino acid positions containing mutations. Residues with one or more observed mutations relative to the reference sequence were classified as mutation hotspots.

Multiple machine learning models were developed and evaluated for hotspot prediction, including Logistic Regression, Elastic Net, Random Forest, XGBoost, and a Convolutional Neural Network (CNN). Model performance was compared using standard classification metrics, with the Random Forest model selected for interactive visualization.

The selected model's predictions are displayed through an interactive protein visualization, where residues are colored according to their predicted hotspot probability. Users can explore the protein by selecting individual residues to view prediction probabilities, predicted and actual classifications, and model performance.


## Features 
- Identifies mutation hotspot residues relative to the SARS-CoV-2 Wuhan reference sequence.
- Generates residue-level hotspot classifications from sequence alignment data.
- Trains and compares multiple machine learning models for hotspot prediction.
- Evaluates model performance using standard classification metrics.
- Provides an interactive protein visualization of Random Forest hotspot predictions.

## Live Demo
Explore the interactive protein visualization here:

[Interactive Protein Hotspot Viewer](https://koriephul.github.io/Protein-Mutation-Hotspot-Analysis/)

## Repository Contents
- Data preprocessing and hotspot labeling
- Machine learning model development and evaluation
- Interactive protein visualization
- Jupyter notebooks used throughout the analysis
- Supporting figures and project assets

## Technologies Used

### Programming Language
- Python

### Machine Learning
- Scikit-learn
- XGBoost
- TensorFlow / Keras

### Data Processing
- Pandas
- NumPy

### Data Visualization
- Matplotlib
- Seaborn

### Protein Visualization
- PyMOL
- 3Dmol.js

### Web Technologies
- HTML
- CSS
- JavaScript

### Deployment
- GitHub Pages

## Results
The table below summarizes the performance of the evaluated machine learning models for mutation hotspot prediction.

| Model | ROC-AUC | PR-AUC| F1 Score | 
|--------|---------:|----------:|--------:|
| Logistic Regression | 0.547  | 0.117 | 0.194 |  
| Reduced Logistic Regression | 0.575 | 0.132 | 0.224 |  
| Elastic Net | 0.535 | 0.117 | 0.180 |  
| Random Forest | 0.624 | 0.249 | 0.143 | 
| XGBoost | 0.603 | 0.199 | 0.071 | 
| CNN | 0.404 | 0.04 | 0.044 | 

### Precision-Recall Curves
<p align="center">
  <img width="613" height="470" alt="image" src="https://github.com/user-attachments/assets/3562b7fd-acca-44f4-8f29-4a2f20445cd3" />
</p>

<p align="center">
  <img width="613" height="470" alt="image" src="https://github.com/user-attachments/assets/a605a8e3-7445-4329-89af-508a829ae76b" />
</p>

Random Forest achieved the highest ROC-AUC and PR-AUC among the evaluated models, while Reduced Logistic Regression produced the highest F1 score. Overall, tree-based models outperformed the linear and deep learning approaches for this dataset.

## Future Improvements
- Expand the dataset to include additional SARS-CoV-2 sequences.
- Investigate additional structural and evolutionary features for hotspot prediction.
- Explore alternative deep learning architectures.
- Evaluate the workflow using additional viral proteins.

## Acknowledgements
This project made use of the following resources:

- NCBI Protein Database for the SARS-CoV-2 spike protein sequence data.
- Scikit-learn for machine learning model development.
- XGBoost for gradient boosting classification.
- TensorFlow/Keras for the convolutional neural network implementation.
- PyMOL for protein structure visualization.
- 3Dmol.js for the interactive protein visualization.

I would like to thank Professor Lafler for his guidance and support throughout this project.

## License

This project is intended for educational and portfolio purposes.

## Troubleshooting
If the interactive protein viewer does not render, your browser may have WebGL or hardware acceleration disabled.

For Google Chrome:

1. Open **Settings → System**.
2. Enable **Use graphics acceleration when available**.
3. Restart Chrome and refresh the page.
