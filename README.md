# Projet Anémie

Ce projet porte sur la classification des types d’anémie à partir d’un jeu de données de résultats de bilan sanguin (CBC). Il s’inscrit dans le cadre du module Data Mining / Machine Learning.

## Objectif

L’objectif principal est de développer un modèle de machine learning capable de prédire la catégorie d’anémie à partir des paramètres hématologiques disponibles.

Les classes présentes dans le dataset incluent notamment :
- Anémie microcytaire hypochromique
- Anémie ferriprive
- Autres anémies microcytaires
- Leucémie
- Santé / Healthy

## Structure du projet

- `projet-anemie.ipynb` : notebook principal contenant le nettoyage des données, l’analyse exploratoire, les modèles et les résultats.
- `datasets/diagnosed_cbc_data_v4.csv` : fichier principal de données.
- `demo_photos/` : images ou captures de démonstration.
- `Presentation_Projet_Anemie.pptx` : support de présentation.
- `Rapport_Projet_Anemie.docx` : rapport détaillé du projet.

## Jeu de données

Le dataset contient plusieurs variables biologiques et hématologiques, notamment :

- WBC
- LYMp
- NEUTp
- LYMn
- NEUTn
- RBC
- HGB
- HCT
- MCV
- MCH
- MCHC
- PLT
- PDW
- PCT
- Diagnosis

La colonne `Diagnosis` correspond à la cible de classification.

## Outils et dépendances

Pour exécuter le notebook, il est conseillé d’utiliser Python avec les bibliothèques suivantes :

- Python 3.9+
- Jupyter Notebook / VS Code Python
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

Installation recommandée :

```bash
pip install jupyter pandas numpy matplotlib seaborn scikit-learn
```

## Comment lancer le projet

1. Ouvrir le dossier du projet.
2. Lancer Jupyter ou VS Code avec un environnement Python configuré.
3. Ouvrir le fichier `projet-anemie.ipynb`.
4. Exécuter les cellules du notebook dans l’ordre.

## Workflow du notebook

Le notebook traite généralement les étapes suivantes :

1. Chargement des données
2. Vérification du schéma des colonnes
3. Analyse exploratoire des données
4. Nettoyage et préparation des features
5. Division train/test
6. Entraînement de modèles de classification
7. Évaluation des performances
8. Interprétation des résultats

## Résultats attendus

Le projet permet de comparer plusieurs approches de classification et d’évaluer la performance selon des métriques telles que :

- précision
- rappel
- F1-score
- matrice de confusion
- accuracy

## Photos de démonstration

Voici les captures du projet, organisées selon les étapes du workflow de classification des types d’anémie :

### 1. Découverte du dataset et exploration initiale

![Vue initiale du dataset](demo_photos/Capture%20d%27%C3%A9cran%202026-08-15%20142215.png)

La première capture montre le chargement du fichier CSV et la structure du dataset avant nettoyage.

### 2. Distribution des classes

![Distribution des diagnostics](demo_photos/Capture%20d%27%C3%A9cran%202026-08-15%20152131.png)

Cette image met en évidence le déséquilibre entre les classes d’anémie et la présence de catégories majoritaires comme “Healthy”.

### 3. Analyse exploratoire et valeurs aberrantes

![Histogrammes et valeurs aberrantes](demo_photos/Capture%20d%27%C3%A9cran%202026-08-15%20152144.png)

L’analyse visuelle repère les valeurs impossibles qui seront corrigées lors du prétraitement (bornage médical).

### 4. Corrélation entre variables

![Matrice de corrélation](demo_photos/Capture%20d%27%C3%A9cran%202026-08-15%20152154.png)

Cette étape montre les relations entre les variables biométriques et confirme qu’elles peuvent contribuer à la classification.

### 5. Prétraitement et normalisation

![Prétraitement des données](demo_photos/Capture%20d%27%C3%A9cran%202026-08-15%20152206.png)

Les données sont corrigées puis normalisées afin d’éviter les biais liés à l’échelle des variables.

### 6. Entraînement des modèles

![Comparaison des modèles](demo_photos/Capture%20d%27%C3%A9cran%202026-08-15%20152234.png)

Cette capture illustre l’entraînement de plusieurs modèles comme la régression logistique, K-NN, l’arbre de décision et le Random Forest.

### 7. Évaluation et matrice de confusion

![Matrice de confusion](demo_photos/Capture%20d%27%C3%A9cran%202026-08-15%20152246.png)

La dernière image présente l’évaluation du modèle et la matrice de confusion, qui permet de vérifier les erreurs entre classes.

## Auteur et contexte

Ce projet a été réalisé dans le cadre du module Data Mining / Graph Mining et du cours de Machine Learning.

## Remarques

- Le dataset est un fichier CSV prêt à l’emploi.
- Les résultats peuvent varier selon les modèles choisis et la séparation train/test.
- Pour une meilleure reproduction, il est conseillé d’utiliser la même version des bibliothèques Python.
