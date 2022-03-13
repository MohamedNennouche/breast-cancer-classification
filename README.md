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
5. Application d'une analyse en composante principales et classification suivant les même modèles et étude comparative
6. Application de plusieurs méthodes de sélection de caractéristiques et étude comparative avec les méthodes précédentes

## Performances atteintes
### Avec les caractéristiques de base
|   Algorithme choisi    |   Précision en test (%)|  F1 score (%) |
|---      |:-:        |:-:        |
|   KNN   |   94.15   |   94.11   |
|   SVM   |   94.15   |   94.06   |
|   MLP   |   94.15   |   94.15   |
### Avec une analyse en composantes principales
On a gardé les 7 premières composantes principales représentant 91% de l'information, et on a retrouvé de meilleurs résultats qu'avec les variables originales
|   Algorithme choisi    |   Précision en test (%)|  F1 score (%) |
|---      |:-:        |:-:        |
|   KNN   |   97.07   |   97.08   |
|   SVM   |   98.24   |   98.25   |
|   MLP   |   98.24   |   98.24   |
### Avec une sélection de paramètres
#### Sélection de paramètres embarquées (Random Forrest)
|   Algorithme choisi    |   Précision en test (%)|  F1 score (%) |
|---      |:-:        |:-:        |
|   Random Forrest  |   98.25  |   98.24   |
|   Random Forrest + PCA   |   97.08   |   97.06  |
#### Sélection de paramètres statistiques
1) **Test $\chi^2$**

|   Algorithme choisi    |   Précision en test (%)|  F1 score (%) |
|---      |:-:        |:-:        |
|   KNN   |   94.15   |   94.10   |
|   SVM   |   94.15   |   94.06   |
|   MLP   |   91.81   |   91.81   |
2) **Information mutuelle**

|   Algorithme choisi    |   Précision en test (%)|  F1 score (%) |
|---      |:-:        |:-:        |
|   KNN   |   91.23   |   91.18   |
|   SVM   |   94.15   |   94.08   |
|   MLP   |   96.49   |   96.48   |
3) **ANOVA**

|   Algorithme choisi    |   Précision en test (%)|  F1 score (%) |
|---      |:-:        |:-:        |
|   KNN   |   90.64   |   90.61   |
|   SVM   |   94.15   |   94.08   |
|   MLP   |   95.32   |   95.34   |
## Remarques
- On a vu à travers ce projet l'intérêt du choix des paramètres à utiliser dans un classifieur en diminuant la dimensionnalité intelligemment on peut optimiser grandement notre modèle de classification
- On a vu la puissance du Random Forrest qui embarque en son sein, un algorithme de sélection de paramètres extrêmement efficace nous donnant les meilleurs résultats sur ce dataset
- Les tests statistiques ont chacun des avantages et inconvéniants et améliorent ou pénalisent légèrement des modèles différents et donc leurs choix dépend énormément de la situation qu'on traite. 
