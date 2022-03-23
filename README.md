## :hospital: Breast cancer classification
The goal of this project is to achieve a binary classification: 
- M (malignant)
- B (benign)

Of breast cancer cases according to several characteristics such as size, circumference, texture... This project is available on Kaggle at this [link](https://www.kaggle.com/uciml/breast-cancer-wisconsin-data).

## :white_check_mark: Repository layout
* cancer-notebook.ipynb : Contains the whole project
* data.csv : Dataset available on Kaggle
## :memo: Software requirements 
Python 3.8 and up
As well as the following packages : 
- Numpy
- Pandas
- Seaborn
- Scikit-learn
- Matplotlib
- Scipy
## :scroll: Content of the project
1. Data loading
2. Global analysis of the dataset
3. Data visualization set and analysis of the correlation between the different variables
4. Application of a set of classification algorithms by analyzing the test performance on the basic variables: 
    - KNN
    - SVM 
    - MLP
5. Application of a principal component analysis and classification following the same models and comparative study
6. Application of several feature selection methods and comparative study with the previous methods

## :straight_ruler: Performance achieved
### With the basic features
|   Algorithm    |   Accuracy (%)|  F1 score (%) |
|---      |:-:        |:-:        |
|   KNN   |   94.15   |   93.63   |
|   SVM   |   94.15   |   93.53   |
|   MLP   |   94.15   |   93.72   |
### With a principal component analysis
We kept the first 7 principal components representing 91% of the information, and we found better results than with the original variables
|   Algorithm    |   Accuracy (%)|  F1 score (%) |
|---      |:-:        |:-:        |
|   KNN   |   97.07   |   96.87   |
|   SVM   |   98.24   |   98.12   |
|   MLP   |   98.25   |   98.11   |
### With a selection of parameters
#### On-board parameter selection (Random Forest)
|   Algorithm    |   Accuracy (%)|  F1 score (%) |
|---      |:-:        |:-:        |
|   Random Forest  |   98.25  |   98.11   |
|   Random Forest + PCA   |   97.08   |   96.83  |
#### Selection of statistical parameters
1) **$\Chi^2$** test

|   Algorithm    |   Accuracy (%)|  F1 score (%) |
|---      |:-:        |:-:        |
|   KNN   |   94.15   |   93.63   |
|   SVM   |   94.15   |   93.53   |
|   MLP   |   91.81   |   91.20   |
2) **Mutual information**

|   Algorithm    |   Accuracy (%)|  F1 score (%) |
|---      |:-:        |:-:        |
|   KNN   |   91.23   |   89.88   |
|   SVM   |   94.15   |   93.58   |
|   MLP   |   96.49   |   96.20   |
3) **ANOVA**

|   Algorithm    |   Accuracy (%)|  F1 score (%) |
|---      |:-:        |:-:        |
|   KNN   |   90.64   |   90.48   |
|   SVM   |   94.15   |   93.58   |
|   MLP   |   95.32   |   95.01   |
## :pushpin: Remarks
- We have seen through this project the interest of the choice of the parameters to be used in a classifier by decreasing the dimensionality intelligently we can greatly optimize our classification model
- We have seen the power of the Random Forest which embeds within it, an extremely efficient parameter selection algorithm giving us the best results on this dataset
- Statistical tests each have advantages and disadvantages and improve or penalize slightly different models and therefore their choice depends greatly on the situation we are dealing with. 
## :page_facing_up: Conclusion
We can see through this project that the best results were obtained with the SVM and the MLP with the application of a principal component analysis or with the use of Random Forrest coupled with its embedded feature selection algorithm 
