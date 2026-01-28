# 📚 INDEX - TP4: Classification Robuste et Modélisation de l'Incertitude

## 📂 Structure du Projet

```
machine_learning_fofack/
│
├── 📓 NOTEBOOKS JUPYTER (4 parties)
│   ├── TP4_Robust_Classification.ipynb              [22 KB]  ⭐ PARTIE 1
│   ├── TP4_Robust_Classification_Part2.ipynb        [32 KB]  ⭐ PARTIE 2
│   ├── TP4_Robust_Classification_Part3.ipynb        [38 KB]  ⭐ PARTIE 3
│   └── TP4_Robust_Classification_Part4.ipynb        [48 KB]  ⭐ PARTIE 4
│
├── 📖 DOCUMENTATION
│   ├── TP4_README.md                                [10 KB]  📘 Guide complet
│   ├── TP4_QUICK_START.md                           [9 KB]   🚀 Démarrage rapide
│   ├── TP4_FORMULAS.md                              [9 KB]   📐 Formulaire mathématique
│   └── TP4_INDEX.md                                 [Ce fichier]
│
├── 📄 FICHIERS DE CONFIGURATION
│   ├── requirements.txt                             [512 B]  📦 Dépendances Python
│   └── .gitignore                                   [71 B]   🔒 Git ignore
│
├── 📊 DONNÉES
│   ├── housing.csv                                  [1.4 MB] 🏠 Dataset (autre TP)
│   └── [Breast Cancer Wisconsin]                   [Chargé via sklearn]
│
└── 📑 DOCUMENTS ORIGINAUX
    └── TP4_Classification.pdf                       [257 KB] 📋 Énoncé du TP
```

---

## 📓 Description des Notebooks

### **Partie 1: Préparation et Baselines Probabilistes** ⭐
**Fichier:** `TP4_Robust_Classification.ipynb`  
**Taille:** 22 KB  
**Cellules:** ~20 cellules  

**Contenu:**
- ✅ Chargement et exploration du dataset Breast Cancer Wisconsin
- ✅ Prétraitement et standardisation des données
- ✅ Implémentation de Régression Logistique avec SGA (from scratch)
- ✅ Comparaison avec scikit-learn
- ✅ Naive Bayes Classifier
- ✅ K-Nearest Neighbors avec optimisation de K

**Temps estimé:** 1-2 heures

---

### **Partie 2: Classification Avancée et Non-Linéaire** ⭐
**Fichier:** `TP4_Robust_Classification_Part2.ipynb`  
**Taille:** 32 KB  
**Cellules:** ~25 cellules  

**Contenu:**
- ✅ Arbres de Décision (CART)
- ✅ Analyse de l'importance des features
- ✅ Visualisation de l'arbre
- ✅ Boosting: AdaBoost et Gradient Boosting
- ✅ SVM Linéaire et Soft Margin
- ✅ SVM avec Kernel RBF
- ✅ Visualisation des frontières de décision (2D avec PCA)

**Temps estimé:** 2-3 heures

---

### **Partie 3: Robustesse, Évaluation et MLOps** ⭐
**Fichier:** `TP4_Robust_Classification_Part3.ipynb`  
**Taille:** 38 KB  
**Cellules:** ~30 cellules  

**Contenu:**
- ✅ Évaluation avec 6 métriques (Accuracy, Precision, Recall, F1, ROC-AUC, AP)
- ✅ Courbes ROC et Precision-Recall
- ✅ Simulation de labels incertains (5% de bruit)
- ✅ Entraînement de modèles robustes avec régularisation
- ✅ Analyse de la dégradation des performances
- ✅ Configuration et utilisation de MLflow
- ✅ Logging de 3 modèles avec hyperparamètres et métriques

**Temps estimé:** 2-3 heures

---

### **Partie 4: Lien avec Evidential Deep Learning** ⭐
**Fichier:** `TP4_Robust_Classification_Part4.ipynb`  
**Taille:** 48 KB  
**Cellules:** ~15 cellules (beaucoup de markdown)  

**Contenu:**
- ✅ Théorie de Dempster-Shafer
- ✅ Principes d'Evidential Deep Learning (EDL)
- ✅ Comparaison Softmax vs EDL
- ✅ Simulation conceptuelle avec distributions Dirichlet
- ✅ Structure complète d'article de recherche (8 sections)
- ✅ Abstract, Introduction, Méthodologie, Résultats, Discussion, Conclusion

**Temps estimé:** 2-3 heures

---

## 📖 Description de la Documentation

### **TP4_README.md** 📘
**Taille:** 10 KB  
**Sections:** 15+  

**Contenu:**
- Vue d'ensemble du TP
- Objectifs pédagogiques
- Structure détaillée des notebooks
- Instructions d'installation
- Guide d'utilisation de MLflow
- Concepts clés abordés
- Questions de réflexion
- Ressources complémentaires
- Dépannage
- Critères d'évaluation

**Utilisation:** Lire en premier pour comprendre le TP

---

### **TP4_QUICK_START.md** 🚀
**Taille:** 9 KB  
**Sections:** 10+  

**Contenu:**
- Installation rapide
- Checklist de progression (4 phases)
- Résultats clés attendus
- Points clés par phase
- Astuces d'exécution
- Commandes utiles
- Graphiques attendus
- Erreurs courantes et solutions
- Auto-évaluation
- Validation finale

**Utilisation:** Guide pratique pendant l'exécution

---

### **TP4_FORMULAS.md** 📐
**Taille:** 9 KB  
**Sections:** 15 catégories  

**Contenu:**
- Régression Logistique (Sigmoïde, SGA, Régularisation)
- Naive Bayes (Théorème de Bayes, Gaussian)
- KNN (Distances)
- Arbres de Décision (Gini, Entropie)
- SVM (Marge, Kernel)
- Ensemble Methods (AdaBoost, Gradient Boosting)
- Métriques (Accuracy, Precision, Recall, F1, ROC-AUC)
- EDL (Dirichlet, Incertitude)
- Dempster-Shafer Theory
- Statistiques et Probabilités
- Normalisation
- Régularisation
- Validation Croisée
- PCA
- Optimisation

**Utilisation:** Référence mathématique pendant le TP

---

## 📦 Fichiers de Configuration

### **requirements.txt**
**Taille:** 512 B  

**Dépendances:**
```
numpy>=1.21.0
pandas>=1.3.0
scipy>=1.7.0
scikit-learn>=1.0.0
matplotlib>=3.4.0
seaborn>=0.11.0
mlflow>=1.20.0
imbalanced-learn>=0.8.0
jupyter>=1.0.0
```

**Installation:**
```bash
pip install -r requirements.txt
```

---

## 📊 Données

### **Breast Cancer Wisconsin Dataset**
- **Source:** `sklearn.datasets.load_breast_cancer()`
- **Échantillons:** 569
- **Features:** 30
- **Classes:** 2 (Maligne, Bénigne)
- **Type:** Classification binaire
- **Déséquilibre:** 37% / 63%

**Chargement:**
```python
from sklearn.datasets import load_breast_cancer
data = load_breast_cancer()
X = data.data
y = data.target
```

---

## 🎯 Parcours d'Apprentissage

### **Débutant** (Première fois avec ML)
1. Lire `TP4_README.md` complètement
2. Installer les dépendances avec `requirements.txt`
3. Exécuter Partie 1 cellule par cellule
4. Consulter `TP4_FORMULAS.md` pour les formules
5. Utiliser `TP4_QUICK_START.md` pour la checklist

### **Intermédiaire** (Connaissance de base en ML)
1. Lire `TP4_QUICK_START.md`
2. Exécuter les 4 parties séquentiellement
3. Se concentrer sur les comparaisons de modèles
4. Expérimenter avec les hyperparamètres
5. Explorer MLflow en détail

### **Avancé** (Expérience en ML)
1. Exécuter rapidement les Parties 1-2
2. Se concentrer sur la Partie 3 (Robustesse)
3. Approfondir la Partie 4 (EDL)
4. Implémenter des variantes
5. Rédiger l'article de recherche

---

## 📈 Résultats Attendus

### **Graphiques Générés** (Total: ~20)
- Distribution des classes
- Boxplots des features
- Courbe de convergence SGA
- Matrices de confusion (6 modèles)
- Impact de K (KNN)
- Importance des features
- Visualisation de l'arbre
- Comparaison Boosting
- Impact de C (SVM)
- Frontières de décision 2D (3 modèles)
- Comparaison métriques (bar charts)
- Courbes ROC (3 modèles)
- Courbes Precision-Recall (3 modèles)
- Dégradation performance
- Comparaison Softmax vs EDL
- Distributions Dirichlet

### **Modèles Entraînés** (Total: 10+)
1. Logistic Regression (SGA)
2. Logistic Regression (sklearn)
3. Naive Bayes
4. KNN (5 valeurs de K)
5. Decision Tree
6. AdaBoost
7. Gradient Boosting
8. SVM Linear
9. SVM RBF (multiple C et gamma)
10. Modèles robustes (3)

### **Expériences MLflow** (Total: 3)
1. Logistic Regression Robust (C=0.1)
2. Gradient Boosting Robust (depth=2)
3. SVM RBF Robust (C=0.5)

---

## ✅ Checklist Complète

### **Installation**
- [ ] Python 3.8+ installé
- [ ] Dépendances installées (`pip install -r requirements.txt`)
- [ ] Jupyter Notebook/Lab fonctionnel
- [ ] MLflow installé et testé

### **Exécution**
- [ ] Partie 1 exécutée sans erreur
- [ ] Partie 2 exécutée sans erreur
- [ ] Partie 3 exécutée sans erreur
- [ ] Partie 4 exécutée sans erreur
- [ ] Tous les graphiques générés
- [ ] MLflow UI explorée

### **Compréhension**
- [ ] Différence entre les algorithmes comprise
- [ ] Rôle de la régularisation compris
- [ ] Importance de PRC vs ROC comprise
- [ ] Principes d'EDL compris
- [ ] Théorie de Dempster-Shafer comprise

### **Livrables**
- [ ] 4 notebooks exécutés
- [ ] Rapport MLflow généré
- [ ] Draft d'article commencé
- [ ] Présentation préparée (optionnel)

---

## 🎓 Compétences Acquises

### **Techniques**
✅ Implémentation from scratch (Logistic Regression)  
✅ Utilisation de scikit-learn  
✅ Visualisation avec matplotlib/seaborn  
✅ Tracking avec MLflow  
✅ Gestion de notebooks Jupyter  

### **Théoriques**
✅ Algorithmes de classification (6+)  
✅ Métriques d'évaluation avancées  
✅ Robustesse et régularisation  
✅ Uncertainty quantification  
✅ Evidential Deep Learning  

### **Pratiques**
✅ Prétraitement de données  
✅ Optimisation d'hyperparamètres  
✅ Analyse comparative de modèles  
✅ Gestion de labels bruités  
✅ MLOps et reproductibilité  

---

## 📞 Support et Ressources

### **Documentation**
- 📘 `TP4_README.md` - Guide complet
- 🚀 `TP4_QUICK_START.md` - Démarrage rapide
- 📐 `TP4_FORMULAS.md` - Formulaire mathématique
- 📋 `TP4_Classification.pdf` - Énoncé original

### **Liens Utiles**
- [scikit-learn Documentation](https://scikit-learn.org/)
- [MLflow Documentation](https://mlflow.org/)
- [Matplotlib Gallery](https://matplotlib.org/stable/gallery/)
- [Seaborn Tutorial](https://seaborn.pydata.org/tutorial.html)

### **Contact**
- 📧 Email: louis.fippo@univ-yaounde1.cm
- 🏫 Institution: ENSPY - Génie Informatique

---

## 📊 Statistiques du Projet

| Métrique | Valeur |
|----------|--------|
| **Notebooks** | 4 |
| **Cellules totales** | ~90 |
| **Lignes de code** | ~2000+ |
| **Graphiques** | ~20 |
| **Modèles** | 10+ |
| **Algorithmes** | 6 |
| **Métriques** | 6 |
| **Documentation** | 4 fichiers |
| **Taille totale** | ~150 KB |
| **Temps estimé** | 8-12 heures |

---

## 🏆 Objectif Final

**Produire un article de recherche complet** comparant les approches classiques de ML et EDL pour la classification médicale robuste, avec:

1. ✅ Expériences reproductibles
2. ✅ Résultats quantitatifs
3. ✅ Analyse critique
4. ✅ Visualisations de qualité
5. ✅ Code documenté
6. ✅ Tracking MLflow
7. ✅ Conclusions pertinentes

---

## 🎉 Conclusion

Ce TP complet vous guide à travers:
- **Phase I:** Fondations (Baselines)
- **Phase II:** Méthodes Avancées (SVM, Boosting)
- **Phase III:** Robustesse et MLOps
- **Phase IV:** Théorie EDL et Article

**Bon courage et bon apprentissage! 🚀📊🎓**

---

*Dernière mise à jour: Janvier 2026*  
*Version: 1.0*  
*Auteurs: Louis Fippo Fitime, Claude Tinku, Kerolle Sonfack*
