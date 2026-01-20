# 🫀 Tableau de Bord de Prédiction du Risque Cardiaque

🔗 **Application en ligne** :
https://machine-learning-mq5chodfmh6jdyoyrqj8qy.streamlit.app/ 

---

## 📌 Présentation du projet

Ce projet propose un **tableau de bord interactif basé sur le Machine Learning** permettant de prédire le **risque de maladie cardiaque (CHD)** à partir de données cliniques et comportementales.

L’application est développée en **Python** et déployée avec **Streamlit**, en s’appuyant sur une chaîne complète de traitement en apprentissage automatique.

---

## 🎯 Objectifs du projet

* Réaliser une analyse exploratoire des données (EDA)
* Mettre en place des pipelines de prétraitement robustes
* Appliquer une réduction de dimension par **ACP**
* Entraîner et comparer plusieurs modèles supervisés
* Gérer le déséquilibre des classes avec **SMOTE**
* Sélectionner et sauvegarder le meilleur modèle
* Déployer le modèle final dans une application Streamlit interactive

---

## 📊 Jeu de données

Le projet utilise le dataset **CHD (Coronary Heart Disease)**, qui contient des informations cliniques relatives à des patients.

### Variables d’entrée

* Pression artérielle systolique (SBP)
* Consommation de tabac
* LDL cholestérol
* Adiposité
* Comportement de type A
* Obésité
* Consommation d’alcool
* Âge
* Antécédents familiaux de maladies cardiaques (`famhist`)

### Variable cible

* `chd`

  * `0` → Absence de maladie cardiaque
  * `1` → Présence de maladie cardiaque

---

## ⚙️ Pipeline de Machine Learning

Le projet est implémenté à l’aide de **pipelines scikit-learn**, garantissant la reproductibilité et l’absence de fuite de données.

### Étapes principales :

1. **Prétraitement des données**

   * Imputation des valeurs manquantes
   * Standardisation des variables numériques
   * Encodage One-Hot des variables catégorielles
2. **Réduction de dimension**

   * Analyse en Composantes Principales (ACP) avec 90 % de variance expliquée
3. **Modélisation**

   * Régression logistique (avec et sans ACP)
   * K-Nearest Neighbors (KNN)
4. **Gestion du déséquilibre**

   * SMOTE (Synthetic Minority Over-sampling Technique)
5. **Optimisation**

   * Recherche des hyperparamètres avec GridSearchCV
6. **Sauvegarde**

   * Modèle final sauvegardé sous `Model.pkl`

---

## 🖥️ Application Streamlit

L’application Streamlit permet à l’utilisateur de :

* Saisir les informations cliniques d’un patient
* Lancer une prédiction en temps réel
* Visualiser :

  * Le niveau de risque cardiaque (faible / élevé)
  * La probabilité associée à la prédiction

L’interface adopte un **design de type tableau de bord**, simple, professionnel et orienté lisibilité.

---

## 🚀 Déploiement

L’application est déployée sur **Streamlit Cloud**.

🔗 **Accès à l’application** :
https://machine-learning-mq5chodfmh6jdyoyrqj8qy.streamlit.app/ 

---

## 🛠️ Technologies utilisées

* Python 3
* pandas, numpy
* scikit-learn
* imbalanced-learn
* joblib
* Streamlit

---

## 📁 Structure du projet

```
├── train_model.py        # Entraînement et sélection du modèle
├── app.py                # Application Streamlit
├── CHD.csv               # Jeu de données
├── Model.pkl             # Modèle entraîné
├── requirements.txt      # Dépendances
└── README.md             # Documentation
```

---

## ▶️ Exécution en local

```bash
# Installation des dépendances
pip install -r requirements.txt

# Entraînement du modèle
python train_model.py

# Lancement de l'application
streamlit run app.py

```

## 👥 Auteurs

```
Projet réalisé par :

KHALID NAIT ALI

SAAD SAINANE

ZAKARIRA FTISSA

EL MEHDI AMAR

Ce projet a été réalisé dans un cadre académique.

