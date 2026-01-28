# Guide d'Exécution Rapide - TP4

## 🚀 Démarrage Rapide (Quick Start)

### 1. Installation des Dépendances

```bash
pip install numpy pandas scikit-learn matplotlib seaborn mlflow scipy
```

### 2. Ordre d'Exécution des Notebooks

```
1️⃣ TP4_Robust_Classification.ipynb          (Phase I - Baselines)
2️⃣ TP4_Robust_Classification_Part2.ipynb    (Phase II - Avancé)
3️⃣ TP4_Robust_Classification_Part3.ipynb    (Phase III - Robustesse & MLOps)
4️⃣ TP4_Robust_Classification_Part4.ipynb    (Phase IV - EDL & Article)
```

### 3. Lancer MLflow (après Partie 3)

```bash
mlflow ui
# Ouvrir: http://localhost:5000
```

---

## 📋 Checklist de Progression

### Phase I: Baselines ✅
- [ ] Données chargées et prétraitées
- [ ] Régression Logistique SGA implémentée
- [ ] Comparaison avec sklearn validée
- [ ] Naive Bayes entraîné
- [ ] KNN testé avec différents K
- [ ] Meilleur K identifié

### Phase II: Méthodes Avancées ✅
- [ ] Arbre de Décision entraîné
- [ ] Importance des features analysée
- [ ] AdaBoost et Gradient Boosting comparés
- [ ] SVM Linéaire implémenté
- [ ] Impact du paramètre C analysé
- [ ] SVM RBF avec kernel testé
- [ ] Frontières de décision visualisées (2D)

### Phase III: Robustesse & MLOps ✅
- [ ] Tous les modèles évalués (6 métriques)
- [ ] Courbes ROC tracées
- [ ] Courbes Precision-Recall tracées
- [ ] Labels bruités simulés (5%)
- [ ] Modèles robustes entraînés
- [ ] Dégradation de performance calculée
- [ ] MLflow configuré
- [ ] 3 modèles loggés dans MLflow
- [ ] Interface MLflow explorée

### Phase IV: EDL & Article ✅
- [ ] Théorie EDL comprise
- [ ] Comparaison Softmax vs EDL effectuée
- [ ] Simulation conceptuelle exécutée
- [ ] Distributions Dirichlet visualisées
- [ ] Structure d'article lue
- [ ] Draft d'article commencé

---

## 📊 Résultats Clés à Obtenir

### Métriques de Performance (Données Propres)

| Modèle | Accuracy | F1-Score |
|--------|----------|----------|
| LogReg | ~0.97 | ~0.97 |
| NB | ~0.95 | ~0.95 |
| KNN | ~0.96 | ~0.96 |
| DT | ~0.95 | ~0.95 |
| GB | ~0.97 | ~0.97 |
| SVM | ~0.98 | ~0.98 |

### Robustesse (5% Bruit)

| Modèle Robuste | Dégradation F1 |
|----------------|----------------|
| LogReg (C=0.1) | < 2% |
| GB (depth=2) | < 2.5% |
| SVM (C=0.5) | < 4% |

---

## 🎯 Points Clés par Phase

### Phase I
- **SGA** converge en ~100 époques
- **KNN** optimal: K=5 ou K=7
- **Naive Bayes** rapide mais moins précis

### Phase II
- **Boosting** améliore significativement les arbres
- **SVM RBF** meilleure performance globale
- **Frontières** très différentes selon le modèle

### Phase III
- **PRC** plus informative que ROC
- **Régularisation** = clé de la robustesse
- **MLflow** facilite la comparaison

### Phase IV
- **EDL** quantifie l'incertitude explicitement
- **Softmax** toujours confiant (problème!)
- **Dempster-Shafer** représente l'ignorance

---

## 💡 Astuces d'Exécution

### Pour Jupyter Notebook

```python
# Redémarrer le kernel si nécessaire
# Kernel → Restart & Clear Output

# Exécuter toutes les cellules
# Cell → Run All

# Afficher les graphiques inline
%matplotlib inline
```

### Pour Gagner du Temps

```python
# Réduire les époques pour tests rapides
epochs = 50  # au lieu de 100

# Réduire le nombre d'estimateurs
n_estimators = 50  # au lieu de 100

# Tester sur un sous-ensemble
X_train_small = X_train[:200]
y_train_small = y_train[:200]
```

### Pour Déboguer

```python
# Afficher les shapes
print(f"X_train shape: {X_train.shape}")
print(f"y_train shape: {y_train.shape}")

# Vérifier les valeurs manquantes
print(f"Missing values: {np.isnan(X_train).sum()}")

# Afficher les premières prédictions
print(f"First 5 predictions: {y_pred[:5]}")
```

---

## 🔧 Commandes Utiles

### Installation
```bash
# Vérifier Python
python --version

# Installer pip si nécessaire
python -m ensurepip --upgrade

# Installer toutes les dépendances
pip install -r requirements.txt  # si fichier fourni
```

### MLflow
```bash
# Lancer l'UI
mlflow ui

# Lancer sur un port spécifique
mlflow ui --port 5001

# Voir les runs
mlflow runs list --experiment-name TP4_Robust_Medical_Classification
```

### Jupyter
```bash
# Lancer Jupyter Notebook
jupyter notebook

# Lancer JupyterLab (interface moderne)
jupyter lab

# Convertir notebook en HTML
jupyter nbconvert --to html TP4_Robust_Classification.ipynb
```

---

## 📈 Graphiques Attendus

### Partie 1
- ✅ Distribution des classes (bar chart)
- ✅ Boxplots des features
- ✅ Courbe de convergence SGA
- ✅ Matrice de confusion LogReg
- ✅ Impact de K sur KNN

### Partie 2
- ✅ Importance des features (bar chart)
- ✅ Arbre de décision (tree plot)
- ✅ Comparaison Boosting (grouped bar)
- ✅ Impact de C sur SVM (line plot)
- ✅ Frontières de décision 2D (contour plots)

### Partie 3
- ✅ Comparaison métriques (grouped bar)
- ✅ Courbes ROC (3 modèles)
- ✅ Courbes Precision-Recall (3 modèles)
- ✅ Dégradation performance (bar chart)
- ✅ Baseline vs Robust (comparison)

### Partie 4
- ✅ Comparaison Softmax vs EDL (bar charts)
- ✅ Distributions Dirichlet (2 scénarios)
- ✅ Mesures d'incertitude (comparison)

---

## ⚠️ Erreurs Courantes et Solutions

### Erreur 1: Module not found
```python
# Problème
ModuleNotFoundError: No module named 'mlflow'

# Solution
!pip install mlflow
```

### Erreur 2: Kernel died
```python
# Problème: Mémoire insuffisante

# Solution: Réduire la taille des données
X_train = X_train[:1000]
y_train = y_train[:1000]
```

### Erreur 3: Graphiques ne s'affichent pas
```python
# Solution
%matplotlib inline
import matplotlib.pyplot as plt
plt.show()
```

### Erreur 4: MLflow UI ne démarre pas
```bash
# Vérifier l'installation
pip show mlflow

# Réinstaller
pip uninstall mlflow
pip install mlflow
```

---

## 📝 Livrables Finaux

### 1. Notebooks Exécutés (4 fichiers)
- `TP4_Robust_Classification.ipynb` ✅
- `TP4_Robust_Classification_Part2.ipynb` ✅
- `TP4_Robust_Classification_Part3.ipynb` ✅
- `TP4_Robust_Classification_Part4.ipynb` ✅

### 2. Rapport MLflow
- Captures d'écran de l'interface
- Tableau comparatif des runs
- Identification du meilleur modèle

### 3. Article de Recherche (Draft)
- Titre
- Abstract (150 mots)
- Introduction
- Méthodologie
- Résultats
- Discussion EDL
- Conclusion

### 4. Présentation (Optionnel)
- 10-15 slides
- Résultats principaux
- Visualisations clés
- Conclusions

---

## 🎓 Auto-Évaluation

### Compréhension Théorique
- [ ] Je comprends la différence entre classification binaire et multiclasse
- [ ] Je peux expliquer le fonctionnement de chaque algorithme
- [ ] Je comprends le rôle de la régularisation
- [ ] Je sais interpréter les courbes ROC et PRC
- [ ] Je comprends les principes d'EDL

### Compétences Pratiques
- [ ] Je sais implémenter un algorithme from scratch
- [ ] Je peux utiliser scikit-learn efficacement
- [ ] Je sais évaluer un modèle avec plusieurs métriques
- [ ] Je peux utiliser MLflow pour tracker des expériences
- [ ] Je sais visualiser des résultats de ML

### Analyse Critique
- [ ] Je peux comparer plusieurs modèles objectivement
- [ ] Je comprends les limites de chaque approche
- [ ] Je peux proposer des améliorations
- [ ] Je sais identifier les cas d'usage appropriés

---

## 🏁 Prochaines Étapes

### Court Terme
1. Compléter tous les notebooks
2. Générer le rapport MLflow
3. Rédiger le draft d'article
4. Préparer la présentation

### Moyen Terme
1. Implémenter EDL avec PyTorch
2. Tester sur CheXpert dataset
3. Comparer avec approches Bayésiennes
4. Publier les résultats

### Long Terme
1. Déployer en production avec MLflow
2. Intégrer dans un système de diagnostic
3. Collecter du feedback médical
4. Itérer et améliorer

---

## 📞 Aide et Support

**Besoin d'aide?**
- 📧 Email: louis.fippo@univ-yaounde1.cm
- 💬 Forum: [Lien]
- 📚 Documentation: README.md complet

**Ressources:**
- [scikit-learn docs](https://scikit-learn.org/)
- [MLflow docs](https://mlflow.org/)
- [Matplotlib gallery](https://matplotlib.org/stable/gallery/)

---

## ✅ Validation Finale

Avant de soumettre, vérifiez:
- [ ] Tous les notebooks s'exécutent sans erreur
- [ ] Tous les graphiques sont générés
- [ ] Les résultats sont cohérents
- [ ] MLflow contient les 3 runs
- [ ] Le rapport est complet
- [ ] L'article est structuré

---

**Bon courage et bon apprentissage! 🚀📊🎓**
