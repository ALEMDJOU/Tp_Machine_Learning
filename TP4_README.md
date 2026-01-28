# TP4: Classification Robuste et Modélisation de l'Incertitude

## 📋 Vue d'Ensemble

Ce TP complet explore la classification robuste dans le contexte médical, avec un focus sur la gestion de l'incertitude des labels. Il est divisé en **4 notebooks Jupyter** couvrant toutes les phases du projet.

**Auteurs:** Louis Fippo Fitime, Claude Tinku, Kerolle Sonfack  
**Institution:** ENSPY - Génie Informatique  
**Date:** Décembre 2025

---

## 🎯 Objectifs Pédagogiques

- ✅ Maîtriser les algorithmes de classification (Logistic Regression, Naive Bayes, KNN, Decision Trees, SVM)
- ✅ Implémenter des méthodes d'ensemble (Boosting)
- ✅ Évaluer avec des métriques avancées (Precision-Recall, AUC)
- ✅ Gérer l'incertitude et le bruit dans les labels
- ✅ Pratiquer le MLOps avec MLflow
- ✅ Comprendre l'Evidential Deep Learning (EDL)

---

## 📚 Structure des Notebooks

### **Partie 1: Préparation et Baselines Probabilistes**
📓 `TP4_Robust_Classification.ipynb`

**Contenu:**
- Task 1.1: Chargement et prétraitement des données
- Task 1.2: Régression Logistique avec Stochastic Gradient Ascent (SGA)
- Task 1.3: Naive Bayes et K-Nearest Neighbors (KNN)

**Durée estimée:** 1-2 heures

**Points clés:**
- Implémentation from scratch de la régression logistique
- Comparaison avec scikit-learn
- Analyse de l'impact du paramètre K pour KNN

---

### **Partie 2: Classification Avancée et Non-Linéaire**
📓 `TP4_Robust_Classification_Part2.ipynb`

**Contenu:**
- Task 2.1: Arbres de Décision et Boosting
- Task 2.2: Support Vector Machines (SVM)
- Task 2.3: Visualisation des frontières de décision

**Durée estimée:** 2-3 heures

**Points clés:**
- Importance des features avec Decision Trees
- Comparaison AdaBoost vs Gradient Boosting
- SVM Linéaire, Soft Margin, et Kernel RBF
- Visualisation 2D avec PCA

---

### **Partie 3: Robustesse, Évaluation et MLOps**
📓 `TP4_Robust_Classification_Part3.ipynb`

**Contenu:**
- Task 3.1: Évaluation avancée et gestion du déséquilibre
- Task 3.2: Robustesse face à l'incertitude des labels
- Task 3.3: MLOps avec MLflow

**Durée estimée:** 2-3 heures

**Points clés:**
- Courbes ROC et Precision-Recall
- Simulation de labels bruités (5% de bruit)
- Comparaison baseline vs modèles robustes
- Tracking d'expériences avec MLflow

---

### **Partie 4: Lien avec Evidential Deep Learning**
📓 `TP4_Robust_Classification_Part4.ipynb`

**Contenu:**
- Task 4.1: Modélisation conceptuelle de l'incertitude
- Task 4.2: Structure d'article de recherche

**Durée estimée:** 2-3 heures

**Points clés:**
- Théorie de Dempster-Shafer
- Comparaison Softmax vs EDL
- Simulation conceptuelle
- Draft complet d'article scientifique

---

## 🚀 Installation et Prérequis

### Environnement Python

```bash
# Python 3.8 ou supérieur recommandé
python --version
```

### Installation des Dépendances

```bash
# Installation de toutes les bibliothèques nécessaires
pip install numpy pandas scikit-learn matplotlib seaborn mlflow imbalanced-learn scipy
```

**Bibliothèques utilisées:**
- `numpy` - Calculs numériques
- `pandas` - Manipulation de données
- `scikit-learn` - Algorithmes ML
- `matplotlib` & `seaborn` - Visualisations
- `mlflow` - MLOps et tracking
- `scipy` - Fonctions statistiques

---

## 📊 Dataset

**Breast Cancer Wisconsin Dataset**
- **Source:** scikit-learn (load_breast_cancer)
- **Échantillons:** 569
- **Features:** 30 (caractéristiques extraites d'images)
- **Classes:** 2 (Maligne vs Bénigne)
- **Distribution:** ~37% Maligne, ~63% Bénigne

**Pourquoi ce dataset?**
- Représentatif des problèmes médicaux
- Bien documenté et validé
- Taille appropriée pour l'apprentissage
- Déséquilibré (réaliste)

---

## 🔄 Ordre d'Exécution

### Option 1: Exécution Séquentielle (Recommandée)

1. **Partie 1** → Comprendre les bases
2. **Partie 2** → Méthodes avancées
3. **Partie 3** → Robustesse et MLOps
4. **Partie 4** → Théorie EDL et article

### Option 2: Exécution Indépendante

Chaque notebook peut être exécuté indépendamment car:
- Les données sont rechargées au début
- Les imports sont inclus
- Pas de dépendances entre notebooks

---

## 📈 Résultats Attendus

### Performance sur Données Propres

| Modèle | Accuracy | F1-Score | ROC-AUC |
|--------|----------|----------|---------|
| Logistic Regression | ~97% | ~97% | ~99% |
| Gradient Boosting | ~97% | ~97% | ~99% |
| SVM RBF | ~98% | ~98% | ~99% |

### Performance avec Labels Bruités (5% bruit)

| Modèle | Dégradation F1 |
|--------|----------------|
| LogReg (C=0.1) | -1.2% |
| GradBoost (depth=2) | -1.8% |
| SVM (C=0.5) | -3.7% |

---

## 🛠️ Utilisation de MLflow

### Lancer l'Interface MLflow

Après avoir exécuté la Partie 3:

```bash
# Dans le terminal, depuis le dossier du projet
mlflow ui
```

Puis ouvrir dans le navigateur: `http://localhost:5000`

### Fonctionnalités MLflow

- 📊 Comparaison des runs
- 📈 Visualisation des métriques
- 🔍 Recherche et filtrage
- 💾 Téléchargement des modèles
- 🏷️ Tags et annotations

---

## 📝 Livrables du TP

### 1. Notebooks Exécutés
- Tous les notebooks avec cellules exécutées
- Graphiques générés
- Résultats affichés

### 2. Rapport MLflow
- Captures d'écran de l'interface MLflow
- Comparaison des expériences
- Meilleur modèle identifié

### 3. Article de Recherche (Draft)
- Basé sur la structure de la Partie 4
- Remplir avec vos résultats spécifiques
- Format: IEEE ou ACM

---

## 🎓 Concepts Clés Abordés

### Machine Learning
- Classification binaire et multiclasse
- Frontières de décision
- Régularisation (L1/L2)
- Validation croisée

### Évaluation
- Métriques: Accuracy, Precision, Recall, F1
- Courbes ROC et Precision-Recall
- AUC et Average Precision
- Matrices de confusion

### Robustesse
- Label noise
- Régularisation
- Ensemble methods
- Calibration

### MLOps
- Experiment tracking
- Model versioning
- Hyperparameter logging
- Reproducibility

### Théorie Avancée
- Dempster-Shafer Theory
- Evidential Deep Learning
- Uncertainty quantification
- Bayesian approaches

---

## 🔍 Questions de Réflexion

### Partie 1
1. Pourquoi le SGA est-il plus efficace que le batch gradient descent pour les grands datasets?
2. Quelle est la limitation principale de l'hypothèse d'indépendance de Naive Bayes?
3. Comment choisir la valeur optimale de K pour KNN?

### Partie 2
1. Pourquoi les arbres de décision ont-ils tendance au surapprentissage?
2. Expliquez le rôle du paramètre C dans les SVM.
3. Comment le kernel trick permet-il de gérer les données non-linéaires?

### Partie 3
1. Pourquoi PRC est-elle préférable à ROC pour les données déséquilibrées?
2. Comment la régularisation améliore-t-elle la robustesse au bruit?
3. Quels sont les avantages de MLflow pour la collaboration en équipe?

### Partie 4
1. Quelle est la différence fondamentale entre Softmax et EDL?
2. Comment EDL représente-t-il l'ignorance?
3. Pourquoi EDL est-il particulièrement adapté aux applications médicales?

---

## 📖 Ressources Complémentaires

### Articles de Référence
1. **Evidential Deep Learning** - Sensoy et al., NeurIPS 2018
2. **Uncertainty in Deep Learning** - Gal & Ghahramani, 2016
3. **Label Noise** - Patrini et al., CVPR 2017

### Tutoriels
- [scikit-learn Documentation](https://scikit-learn.org/)
- [MLflow Documentation](https://mlflow.org/docs/latest/index.html)
- [Dempster-Shafer Theory](https://en.wikipedia.org/wiki/Dempster%E2%80%93Shafer_theory)

### Datasets Médicaux
- [CheXpert](https://stanfordmlgroup.github.io/competitions/chexpert/)
- [ISIC Skin Lesions](https://www.isic-archive.com/)
- [NIH Chest X-rays](https://www.nih.gov/news-events/news-releases/nih-clinical-center-provides-one-largest-publicly-available-chest-x-ray-datasets-scientific-community)

---

## 🐛 Dépannage

### Problème: Erreur d'import
```python
# Solution: Installer la bibliothèque manquante
pip install <nom_bibliotheque>
```

### Problème: MLflow UI ne démarre pas
```bash
# Vérifier que MLflow est installé
pip show mlflow

# Réinstaller si nécessaire
pip install --upgrade mlflow
```

### Problème: Graphiques ne s'affichent pas
```python
# Ajouter en début de notebook
%matplotlib inline
import matplotlib.pyplot as plt
```

### Problème: Mémoire insuffisante
```python
# Réduire la taille du dataset
X_train_sample = X_train[:1000]
y_train_sample = y_train[:1000]
```

---

## 💡 Conseils pour Réussir

1. **Exécutez cellule par cellule** - Comprenez chaque étape
2. **Lisez les commentaires** - Ils expliquent le code
3. **Expérimentez** - Modifiez les hyperparamètres
4. **Visualisez** - Les graphiques sont essentiels
5. **Documentez** - Prenez des notes sur vos observations
6. **Comparez** - Analysez les différences entre modèles
7. **Questionnez** - Pourquoi tel modèle est meilleur?

---

## 🏆 Critères d'Évaluation

### Technique (60%)
- ✅ Exécution correcte de tous les notebooks (20%)
- ✅ Compréhension des algorithmes (20%)
- ✅ Analyse des résultats (20%)

### Rapport (30%)
- ✅ Structure claire (10%)
- ✅ Analyse critique (10%)
- ✅ Conclusions pertinentes (10%)

### Présentation (10%)
- ✅ Clarté des explications
- ✅ Qualité des visualisations
- ✅ Réponses aux questions

---

## 📞 Support

**Questions?** Contactez:
- **Email:** louis.fippo@univ-yaounde1.cm
- **Heures de bureau:** [À définir]
- **Forum:** [Lien vers forum de discussion]

---

## 📜 Licence

Ce matériel pédagogique est fourni à des fins éducatives.  
© 2025 ENSPY - Tous droits réservés

---

## 🎉 Bonne Chance!

Profitez de ce TP pour approfondir vos connaissances en Machine Learning et en classification robuste. N'hésitez pas à explorer au-delà des exercices proposés!

**Happy Learning! 🚀📊🤖**
