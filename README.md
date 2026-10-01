# 🩺 Robust classification & uncertainty modelling

My solution to **TP4 of the Machine Learning course** (Computer Engineering, ENSPY): robust classification in a medical context, with a focus on **label noise and uncertainty**.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)

---

## 📓 Notebooks

| Part | Notebook | Content |
|---|---|---|
| 1 | `TP4_Robust_Classification.ipynb` | Preprocessing, **logistic regression implemented from scratch** (stochastic gradient ascent), Naive Bayes, KNN |
| 2 | `TP4_Robust_Classification_Part2.ipynb` | Decision trees, AdaBoost vs Gradient Boosting, SVM (linear, soft margin, RBF kernel), decision boundaries |
| 3 | `TP4_Robust_Classification_Part3.ipynb` | Advanced evaluation (precision-recall, AUC), class imbalance, robustness to noisy labels, experiment tracking with **MLflow** |
| 4 | `TP4_Robust_Classification_Part4.ipynb` | Uncertainty modelling: Softmax vs **Evidential Deep Learning (EDL)** |

Detailed documentation (in French): [TP4_README.md](TP4_README.md) · [Quick start](TP4_QUICK_START.md) · [Formulas](TP4_FORMULAS.md) · [Summary](TP4_SUMMARY.md)

## 🚀 Getting started

```bash
git clone https://github.com/ALEMDJOU/Tp_Machine_Learning.git
cd Tp_Machine_Learning
pip install -r "requirements_ml_minimal..txt"
jupyter notebook
```

## 📚 Credits

Assignment designed by **Louis Fippo Fitime**, Claude Tinku and Kerolle Sonfack (ENSPY, Computer Engineering department). Subject: [TP4_Classification.pdf](TP4_Classification.pdf).

---

👤 **Henri Joël Fofack Alemdjou** · [Portfolio](https://portfoliofofackhenri.vercel.app/) · [LinkedIn](https://linkedin.com/in/henri-fofack-250b1b320)
