# 📊 Prédiction de l’éligibilité aux prêts bancaires avec Machine Learning

Ce projet vise à prédire l’éligibilité à l’octroi d’un prêt personnel en se basant sur les caractéristiques sociodémographiques et financières des clients. L’objectif est d’outiller les décideurs bancaires avec un modèle robuste capable de détecter les profils à risque ou éligibles à un prêt.

---

## 🧠 Objectifs

- Comprendre les déterminants de l’octroi d’un prêt personnel.
- Évaluer l’importance des variables via des modèles explicatifs (Probit, Arbre).
- Construire un modèle de classification supervisée performant avec le machine learning.
- Comparer différentes méthodes d'agrégation (Bagging, Boosting, etc.).
- Identifier le modèle le plus robuste et l’évaluer sur de nouvelles données.

---

## 📁 Structure du projet
prediction_prets/
├── rapport_projet_pret.pdf # Rapport complet
├── analysis/
│ └── bivariate_analysis.ipynb # Analyse exploratoire
├── modelisation/
│ └── loan_prediction_model.ipynb # Modélisation machine learning
├── visuals/
│ ├── matrice_confusion.png
│ └── importance_variables.png
└── README.md

---

## 🔧 Outils & Technologies

- Python 3.x
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Jupyter Notebook

---

## 📂 Données

Les données utilisées dans ce projet sont fictives et simulées dans le cadre d’un projet académique.  
Un petit échantillon anonymisé est fourni dans le fichier `sample_dataset.csv` afin de permettre la reproduction des étapes du projet.

---

## 🔍 Méthodologie

### 1. Exploration du profil client
- Variables analysées : âge, revenu, expérience, taille de la famille, niveau d'éducation, dépenses mensuelles, etc.
- Visualisations et corrélations avec la variable cible (accord ou refus du prêt).

### 2. Importance des variables
- **Modèle Probit** pour une approche économétrique.
- **Arbre de décision** pour une segmentation explicite.

### 3. Mise en compétition des modèles
Modèles testés :
- Régression Logistique
- Probit
- Arbre de Décision
- Agrégation : Bagging, Random Forest, AdaBoost, Gradient Boosting

### 4. Validation sur nouvelles données
- Le modèle final est testé sur des individus inédits pour valider sa robustesse.

---

## 📈 Résultats clés

| Modèle             | Exactitude | Précision | Rappel | AUC     |
|--------------------|------------|-----------|--------|---------|
| Decision Tree      | 0.942      | 0.631     | 0.98   | 0.9786  |
| Bagging            | 0.807      | 0.337     | **1.00** | 0.9795|
| Random Forest      | 0.940      | 0.630     | 0.98   | 0.9786  |
| AdaBoost           | 0.990      | 0.970     | 0.93   | 0.9944  |
| Gradient Boosting  | 0.980      | 0.940     | 0.93   |**0.9983**|

✅ **Modèle retenu : Arbre de décision avec Bagging**  
💡 Ce modèle présente un **rappel de 1.0**, garantissant l’identification de tous les clients éligibles, ce qui est essentiel dans une logique de gestion de risque.

---

## 🔎 Variables les plus influentes

- **Revenu**  
- **Niveau d’éducation**  
- **Dépenses mensuelles**  
- **Taille de la famille**

---

## 📄 Rapport complet

Le rapport d’analyse complet du projet est disponible ici :  
👉 [rapport_projet_pret.pdf](./rapport_projet_pret.pdf)

Il contient l’ensemble des étapes, des résultats et des interprétations.

---

## 🧠 Ce que j’ai appris

- Construction d’un pipeline ML complet (de l’exploration à la validation).
- Comparaison rigoureuse de modèles supervisés.
- Choix stratégique d’un modèle basé sur les bonnes métriques (ici : **rappel**).
- Importance de la communication des résultats dans un cadre décisionnel.

---

## 📌 Pistes d'amélioration

- Déploiement d’une interface (ex : Streamlit)
- Génération d’un fichier `.pkl` pour sauvegarde du modèle
- Implémentation d’un modèle XGBoost
- Prise en compte des déséquilibres de classes avec SMOTE

---

## 👤 Auteurs

   **Youcef Belabbas**  
📍 [LinkedIn](https://www.linkedin.com/in/youcef-belabbas-83a86a259/)  
✉️ youcefbelabbas97@gmail.com

   **Saad Alloumi**  
📍 [LinkedIn](https://www.linkedin.com/in/saad-alloumi-b1902b1b6/)  
✉️ saadalloumi@gmail.com
