## Breast cancer classification
Le but de ce projet est de parvenir à mettre en place une classification binaire : 
- M (malin)
- B (bénin)

De cas de cancer du sein suivant plusieurs caractéristiques tels que la taille, la circonférence, la texture... Ce projet est disponible sur Kaggle à ce [lien](https://www.kaggle.com/uciml/breast-cancer-wisconsin-data).

## Disposition du dépôt
* cancer-notebook.ipynb : Contient la totalité du projet réalisé
* data.csv : Dataset disponible sur Kaggle
## Pré-requis logiciels 
Python 3.8 et +
Ainsi que les packages suivant : 
- Numpy
- Pandas
- Seaborn
- Scikit-learn
- Matplotlib
- Scipy
## Contenu du projet
1. Chargement des données
2. Analyse globale des données du dataset
3. Ensemble de visualisation des données et analyse de la corrélation entre les différentes variables
4. Application d'un ensemble d'algorithme de classification en analysant les performances en test sur les variables de bases: 
    - KNN
    - SVM 
    - MLP
5. 

## Performances atteintes
### Avec les caractéristiques de base
|   Algorithme choisi    |   Précision en test (%)|  F1 score (%) |
|---      |:-:        |:-:        |
|   KNN   |   94.15   |   94.11   |
|   SVM   |   94.15   |   94.06   |
|   MLP   |   94.15   |   94.15   |

## Remarques
