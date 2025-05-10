# pca-dimensionality-reduction-hospital-readmission
Principal Component Analysis (PCA) for dimensionality reduction in hospital readmission prediction while maintaining model performance.

## Project Overview
This project investigates whether Principal Component Analysis (PCA) can effectively reduce dataset dimensionality while maintaining comparable predictive performance in logistic regression models that predict patient readmission likelihood. By identifying the optimal number of principal components, we can create more efficient models that require less computational resources without sacrificing predictive power.

## Key Findings
- **Optimal Component Selection**: Three principal components were identified as optimal, capturing approximately 67.4% of the total variance
- **Consistent AUC Performance**: All models (baseline, 3-component PCA, 1-component PCA) achieved identical AUC scores of 0.9988
- **Minimal Accuracy Trade-off**: Maximum accuracy decrease between models was only 2.35% (98.05% baseline vs. 95.70% PC1)
- **Successful Dimensionality Reduction**: Reduced features from 7 dimensions to as few as 1 while maintaining strong predictive performance

## Business Value
Healthcare facilities can benefit from this analysis in several ways:
- **Computational Efficiency**: Reduced dimensionality means faster model training and prediction
- **Resource Optimization**: More efficient analysis of large patient datasets
- **Readmission Reduction**: Better identification of at-risk patients for targeted interventions
- **Cost Savings**: Potential avoidance of Centers for Medicare & Medicaid Services (CMS) penalties for high readmission rates

## Technologies Used
- Python (Pandas, NumPy)
- Scikit-learn for PCA implementation and model building
- Matplotlib & Seaborn for visualization
- Logistic Regression for prediction modeling

## Methodology
1. **Data Preprocessing**: Standardized features to ensure equal contribution to PCA
2. **PCA Implementation**: Applied PCA to the standardized features
3. **Component Selection**: Determined optimal number of components using scree plot and Kaiser criterion
4. **Model Comparison**: Evaluated performance of models built with:
   - All original features (baseline)
   - First three principal components
   - First principal component only
5. **Performance Evaluation**: Compared models using accuracy, AUC, and recall metrics

## Repository Contents
- `pca_dimensionality_reduction.ipynb`: Jupyter notebook containing the complete analysis
- `scaled_data.csv`: DataFrame containing standardized variables
- `medical_clean.csv`: Original dataset (if applicable)
- Images/: Directory containing visualizations (if applicable)

## Key Visualizations
- Principal component matrix heatmap
- Scree plot showing explained variance
- Model performance comparison metrics

## Future Work
- Explore other dimensionality reduction techniques (t-SNE, UMAP)
- Incorporate categorical variables into the analysis
- Investigate clinical interpretations of principal components
- Develop an integrated predictive system for clinical implementation

---

*Note: This analysis was conducted for educational purposes and not for clinical decision-making.*
