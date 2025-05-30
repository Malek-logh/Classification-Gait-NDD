# Classification des Troubles Neuro-dégénératifs à Partir de Données de Marche

🎓 Projet de fin d’études – Faculté des Sciences de Sfax (2025)  
👥 Réalisé par : Akram HAGGUI & Malek LOGHMARI  
📅 Soutenu le : 29 mai 2025

## 🧠 Objectif

Ce projet vise à classifier des troubles neurodégénératifs (ALS, Parkinson, Huntington) à partir de données de marche en utilisant des réseaux GAN pour l’augmentation de données et un modèle CNN-LSTM pour la classification.

## 📂 Dataset

- **Source** : [PhysioNet – Gait in Neurodegenerative Disease Database](https://physionet.org/content/gaitndd/1.0.0/)
- **Données** : 64 sujets répartis en 4 classes (Control, ALS, PD, HD)
- **Fréquence d'échantillonnage** : 300 Hz
- **Caractéristiques extraites** : 13 paramètres spatio-temporels

## ⚙️ Méthodologie

1. **Prétraitement des signaux** :
   - Filtrage Butterworth
   - Normalisation Min-Max
   - Fenêtrage glissant de 4s

2. **Augmentation des données** :
   - Utilisation de TCGAN (Time-series Conditional GAN)
   - Génération ciblée de signaux pour les classes minoritaires

3. **Classification** :
   - Architecture hybride CNN + LSTM
   - Évaluation sur plusieurs binaires (Control vs ALS, PD, HD, NDD)

## 📊 Résultats

| Test                | Accuracy | F1-score |
|---------------------|----------|----------|
| Control vs ALS      | 97%      | 0.96     |
| Control vs Parkinson| 94%      | 0.94     |
| Control vs Hunt     | 96%      | 0.96     |
| Control vs NDD      | 97%      | 0.98     |

Les résultats montrent des performances élevées, comparables aux meilleures méthodes de la littérature, avec une capacité renforcée grâce à l'augmentation des données synthétiques.

## 🛠️ Outils utilisés

- Python 3.x
- TensorFlow / Keras
- Google Colab (GPU T4)
- Matplotlib / Seaborn

## 📈 Perspectives

- Entraînement avec des autoencodeurs variationnels
- Extension aux troubles moteurs post-AVC
- Intégration dans une plateforme d’aide au diagnostic

## 📄 Rapport

Le rapport détaillé du projet est disponible ici : [Rapport.pdf](./Rapport.pdf)

## 📝 Références

Voir section "Références" du [Rapport](./Rapport.pdf) pour les articles scientifiques et travaux comparés.

---

> **Note** : Ce projet a été réalisé dans un cadre académique et n’est pas destiné à un usage médical sans validation clinique.
