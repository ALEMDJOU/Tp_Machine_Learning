# Formulaire Mathématique - TP4

## 📐 Formules Essentielles pour la Classification Robuste

---

## 1. Régression Logistique

### Fonction Sigmoïde
$$\sigma(z) = \frac{1}{1 + e^{-z}}$$

### Hypothèse
$$h_\theta(x) = \sigma(\theta^T x + b) = \frac{1}{1 + e^{-(\theta^T x + b)}}$$

### Fonction de Coût (Log-Loss)
$$J(\theta) = -\frac{1}{m} \sum_{i=1}^{m} [y_i \log(h_\theta(x_i)) + (1-y_i) \log(1-h_\theta(x_i))]$$

### Gradient Descent
$$\theta_j := \theta_j - \alpha \frac{\partial J}{\partial \theta_j}$$

### Stochastic Gradient Ascent (SGA)
$$\theta := \theta + \alpha \cdot (y_i - h_\theta(x_i)) \cdot x_i$$
$$b := b + \alpha \cdot (y_i - h_\theta(x_i))$$

### Régularisation L2
$$J(\theta) = -\frac{1}{m} \sum_{i=1}^{m} [y_i \log(h_\theta(x_i)) + (1-y_i) \log(1-h_\theta(x_i))] + \frac{\lambda}{2m} \sum_{j=1}^{n} \theta_j^2$$

---

## 2. Naive Bayes

### Théorème de Bayes
$$P(y|x) = \frac{P(x|y) \cdot P(y)}{P(x)}$$

### Hypothèse d'Indépendance
$$P(x_1, x_2, ..., x_n | y) = \prod_{i=1}^{n} P(x_i | y)$$

### Classification
$$\hat{y} = \arg\max_y P(y) \prod_{i=1}^{n} P(x_i | y)$$

### Gaussian Naive Bayes
$$P(x_i | y) = \frac{1}{\sqrt{2\pi\sigma_y^2}} \exp\left(-\frac{(x_i - \mu_y)^2}{2\sigma_y^2}\right)$$

---

## 3. K-Nearest Neighbors (KNN)

### Distance Euclidienne
$$d(x, x') = \sqrt{\sum_{i=1}^{n} (x_i - x'_i)^2}$$

### Prédiction (Classification)
$$\hat{y} = \text{mode}(\{y_1, y_2, ..., y_k\})$$

où $\{y_1, ..., y_k\}$ sont les labels des K voisins les plus proches

### Distance de Manhattan
$$d(x, x') = \sum_{i=1}^{n} |x_i - x'_i|$$

---

## 4. Arbres de Décision

### Impureté de Gini
$$G = 1 - \sum_{i=1}^{C} p_i^2$$

où $p_i$ est la proportion de la classe $i$

### Entropie
$$H = -\sum_{i=1}^{C} p_i \log_2(p_i)$$

### Gain d'Information
$$IG(D, A) = H(D) - \sum_{v \in \text{values}(A)} \frac{|D_v|}{|D|} H(D_v)$$

### Complexité
$$O(n \cdot m \cdot \log(n) \cdot \text{depth})$$

---

## 5. Support Vector Machines (SVM)

### Hyperplan de Séparation
$$w^T x + b = 0$$

### Marge
$$\text{margin} = \frac{2}{||w||}$$

### Problème d'Optimisation (Hard Margin)
$$\min_{w,b} \frac{1}{2}||w||^2$$
$$\text{s.t. } y_i(w^T x_i + b) \geq 1, \forall i$$

### Soft Margin SVM
$$\min_{w,b,\xi} \frac{1}{2}||w||^2 + C \sum_{i=1}^{m} \xi_i$$
$$\text{s.t. } y_i(w^T x_i + b) \geq 1 - \xi_i, \xi_i \geq 0$$

### Kernel Trick
$$K(x, x') = \phi(x)^T \phi(x')$$

### Kernel RBF (Gaussian)
$$K(x, x') = \exp\left(-\gamma ||x - x'||^2\right)$$

où $\gamma = \frac{1}{2\sigma^2}$

### Kernel Polynomial
$$K(x, x') = (\gamma x^T x' + r)^d$$

---

## 6. Ensemble Methods

### AdaBoost - Poids des Échantillons
$$w_i^{(t+1)} = w_i^{(t)} \cdot \exp(\alpha_t \cdot \mathbb{1}(y_i \neq h_t(x_i)))$$

### AdaBoost - Poids du Classificateur
$$\alpha_t = \frac{1}{2} \ln\left(\frac{1 - \epsilon_t}{\epsilon_t}\right)$$

où $\epsilon_t$ est le taux d'erreur

### Gradient Boosting
$$F_m(x) = F_{m-1}(x) + \nu \cdot h_m(x)$$

où $\nu$ est le learning rate et $h_m$ est le nouvel arbre

---

## 7. Métriques d'Évaluation

### Accuracy
$$\text{Accuracy} = \frac{TP + TN}{TP + TN + FP + FN}$$

### Precision
$$\text{Precision} = \frac{TP}{TP + FP}$$

### Recall (Sensibilité)
$$\text{Recall} = \frac{TP}{TP + FN}$$

### F1-Score
$$F1 = 2 \cdot \frac{\text{Precision} \cdot \text{Recall}}{\text{Precision} + \text{Recall}} = \frac{2TP}{2TP + FP + FN}$$

### Spécificité
$$\text{Specificity} = \frac{TN}{TN + FP}$$

### ROC-AUC
$$\text{AUC} = \int_0^1 \text{TPR}(t) \, d(\text{FPR}(t))$$

### Average Precision (AP)
$$AP = \sum_n (R_n - R_{n-1}) P_n$$

---

## 8. Evidential Deep Learning (EDL)

### Fonction Softmax (Classique)
$$P(y=k|x) = \frac{e^{z_k}}{\sum_{j=1}^{K} e^{z_j}}$$

### Distribution de Dirichlet
$$\text{Dir}(\mathbf{p} | \boldsymbol{\alpha}) = \frac{1}{B(\boldsymbol{\alpha})} \prod_{k=1}^{K} p_k^{\alpha_k - 1}$$

où $B(\boldsymbol{\alpha}) = \frac{\prod_{k=1}^{K} \Gamma(\alpha_k)}{\Gamma(\sum_{k=1}^{K} \alpha_k)}$

### Paramètres Dirichlet (EDL)
$$\alpha_k = e_k + 1$$

où $e_k$ est l'évidence pour la classe $k$

### Strength (Force)
$$S = \sum_{k=1}^{K} \alpha_k$$

### Probabilités Subjectives
$$\hat{p}_k = \frac{\alpha_k}{S}$$

### Incertitude
$$u = \frac{K}{S}$$

### Fonction de Perte EDL
$$\mathcal{L} = \mathcal{L}_{CE}(\hat{\mathbf{p}}, \mathbf{y}) + \lambda_t \text{KL}(\text{Dir}(\boldsymbol{\alpha}) || \text{Dir}(\boldsymbol{\alpha}_0))$$

### KL Divergence (Dirichlet)
$$\text{KL}(\text{Dir}(\boldsymbol{\alpha}) || \text{Dir}(\boldsymbol{\alpha}_0)) = \log\frac{\Gamma(S)}{\Gamma(S_0)} + \sum_{k=1}^{K} \left[\log\frac{\Gamma(\alpha_{0k})}{\Gamma(\alpha_k)} + (\alpha_k - \alpha_{0k})(\psi(\alpha_k) - \psi(S))\right]$$

où $\psi$ est la fonction digamma

---

## 9. Dempster-Shafer Theory

### Belief (Croyance)
$$\text{Bel}(A) = \sum_{B \subseteq A} m(B)$$

### Plausibility
$$\text{Pl}(A) = 1 - \text{Bel}(\neg A) = \sum_{B \cap A \neq \emptyset} m(B)$$

### Uncertainty (Incertitude)
$$u = m(\Omega)$$

où $\Omega$ est l'ensemble de toutes les hypothèses

### Belief Mass
$$\sum_{A \subseteq \Omega} m(A) = 1$$

---

## 10. Statistiques et Probabilités

### Espérance
$$\mathbb{E}[X] = \sum_{i} x_i P(x_i)$$

### Variance
$$\text{Var}(X) = \mathbb{E}[(X - \mathbb{E}[X])^2] = \mathbb{E}[X^2] - (\mathbb{E}[X])^2$$

### Écart-Type
$$\sigma = \sqrt{\text{Var}(X)}$$

### Covariance
$$\text{Cov}(X, Y) = \mathbb{E}[(X - \mathbb{E}[X])(Y - \mathbb{E}[Y])]$$

### Corrélation de Pearson
$$\rho_{X,Y} = \frac{\text{Cov}(X, Y)}{\sigma_X \sigma_Y}$$

### Entropie de Shannon
$$H(X) = -\sum_{i} P(x_i) \log_2 P(x_i)$$

### Information Mutuelle
$$I(X; Y) = H(X) - H(X|Y) = H(Y) - H(Y|X)$$

---

## 11. Normalisation et Standardisation

### Min-Max Normalization
$$x' = \frac{x - x_{\min}}{x_{\max} - x_{\min}}$$

### Z-Score Standardization
$$x' = \frac{x - \mu}{\sigma}$$

### L2 Normalization
$$x' = \frac{x}{||x||_2} = \frac{x}{\sqrt{\sum_i x_i^2}}$$

---

## 12. Régularisation

### L1 Regularization (Lasso)
$$J(\theta) = \text{Loss} + \lambda \sum_{j=1}^{n} |\theta_j|$$

### L2 Regularization (Ridge)
$$J(\theta) = \text{Loss} + \lambda \sum_{j=1}^{n} \theta_j^2$$

### Elastic Net
$$J(\theta) = \text{Loss} + \lambda_1 \sum_{j=1}^{n} |\theta_j| + \lambda_2 \sum_{j=1}^{n} \theta_j^2$$

---

## 13. Validation Croisée

### K-Fold Cross-Validation Score
$$\text{CV Score} = \frac{1}{K} \sum_{k=1}^{K} \text{Score}_k$$

### Leave-One-Out (LOO)
$$\text{LOO Error} = \frac{1}{n} \sum_{i=1}^{n} \mathbb{1}(y_i \neq \hat{y}_{-i})$$

---

## 14. Réduction de Dimensionnalité

### PCA - Variance Expliquée
$$\text{Variance Expliquée} = \frac{\lambda_i}{\sum_{j=1}^{n} \lambda_j}$$

où $\lambda_i$ est la i-ème valeur propre

### t-SNE - Divergence KL
$$\text{KL}(P||Q) = \sum_i \sum_j p_{ij} \log \frac{p_{ij}}{q_{ij}}$$

---

## 15. Optimisation

### Learning Rate Decay
$$\alpha_t = \frac{\alpha_0}{1 + \text{decay} \cdot t}$$

### Momentum
$$v_t = \beta v_{t-1} + (1-\beta) \nabla J(\theta_t)$$
$$\theta_{t+1} = \theta_t - \alpha v_t$$

### Adam Optimizer
$$m_t = \beta_1 m_{t-1} + (1-\beta_1) \nabla J(\theta_t)$$
$$v_t = \beta_2 v_{t-1} + (1-\beta_2) (\nabla J(\theta_t))^2$$
$$\hat{m}_t = \frac{m_t}{1-\beta_1^t}, \quad \hat{v}_t = \frac{v_t}{1-\beta_2^t}$$
$$\theta_{t+1} = \theta_t - \alpha \frac{\hat{m}_t}{\sqrt{\hat{v}_t} + \epsilon}$$

---

## 📝 Notation

- $x$ : vecteur de features
- $y$ : label (classe)
- $\theta$ : paramètres du modèle
- $m$ : nombre d'échantillons
- $n$ : nombre de features
- $K$ ou $C$ : nombre de classes
- $\alpha$ : learning rate
- $\lambda$ : paramètre de régularisation
- $\sigma$ : écart-type
- $\mu$ : moyenne
- $\gamma$ : paramètre de kernel
- $\epsilon$ : taux d'erreur
- $\xi$ : variable de relâchement (slack variable)

---

## 🔗 Références

1. **Bishop, C. M.** (2006). Pattern Recognition and Machine Learning. Springer.
2. **Hastie, T., Tibshirani, R., & Friedman, J.** (2009). The Elements of Statistical Learning. Springer.
3. **Murphy, K. P.** (2012). Machine Learning: A Probabilistic Perspective. MIT Press.
4. **Goodfellow, I., Bengio, Y., & Courville, A.** (2016). Deep Learning. MIT Press.
5. **Sensoy, M., Kaplan, L., & Kandemir, M.** (2018). Evidential Deep Learning to Quantify Classification Uncertainty. NeurIPS.

---

**Note:** Ce formulaire est un aide-mémoire. Pour une compréhension approfondie, consultez les références et les notebooks du TP.
