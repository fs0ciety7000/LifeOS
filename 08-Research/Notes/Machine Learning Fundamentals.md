---
title: "Machine Learning Fundamentals"
type: research
status: 📝 en cours
date_created: 2025-12-01
last_updated: 2026-01-20
domain: AI/ML
source_type: cours
tags:
  - research
  - ml
  - ai
  - learning
---

# Machine Learning Fundamentals

## Metadata
| | |
|---|---|
| **Domaine** | AI / Machine Learning |
| **Status** | 📝 En cours |
| **Derniere MAJ** | 2026-01-20 |
| **Source** | Andrew Ng - ML Specialization |

## Resume

Notes de cours sur les fondamentaux du Machine Learning.

## Types de ML

### Supervised Learning
- **Regression**: Predire une valeur continue
  - Linear regression
  - Polynomial regression
- **Classification**: Predire une categorie
  - Logistic regression
  - Decision trees
  - SVM

### Unsupervised Learning
- **Clustering**: Grouper des donnees similaires
  - K-means
  - Hierarchical clustering
- **Dimensionality reduction**
  - PCA
  - t-SNE

### Reinforcement Learning
- Agent apprend par essai/erreur
- Reward-based learning

## Concepts importants

### Bias vs Variance Tradeoff
- **High bias** = underfitting
- **High variance** = overfitting
- But: trouver l'equilibre

### Train/Test Split
```python
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)
```

### Cross-Validation
- K-fold CV pour evaluation robuste
- Eviter l'overfitting sur le test set

### Metriques
| Type | Metriques |
|------|-----------|
| Regression | MSE, RMSE, MAE, R² |
| Classification | Accuracy, Precision, Recall, F1 |

## Algorithmes etudies

### Linear Regression
- Hypothese: h(x) = θ₀ + θ₁x
- Cost function: MSE
- Optimization: Gradient Descent

### Logistic Regression
- Pour classification binaire
- Sigmoid function
- Cross-entropy loss

### Decision Trees
- Splitting criteria: Gini, Entropy
- Prone to overfitting
- Solution: pruning, Random Forest

## Code snippets

### Basic sklearn pipeline
```python
from sklearn.linear_model import LogisticRegression
from sklearn.preprocessing import StandardScaler
from sklearn.pipeline import Pipeline

pipe = Pipeline([
    ('scaler', StandardScaler()),
    ('clf', LogisticRegression())
])
pipe.fit(X_train, y_train)
```

## Questions a explorer
- [ ] Comment choisir le bon algorithme?
- [ ] Quand utiliser deep learning vs ML classique?
- [ ] Feature engineering best practices

## Resources
- [[03-Projects/Learn Python for AI|Projet Python AI]]
- Andrew Ng's course notes
- Scikit-learn documentation

## Tags
#research #ml #ai #sklearn
