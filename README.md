# 🗑️ Classification des Déchets par Vision par Ordinateur (YOLOv8)

[![Documentation Status](https://readthedocs.org/projects/project-computer-vision/badge/?version=latest)](https://project-computer-vision.readthedocs.io/fr/latest/)
[![Python](https://img.shields.io/badge/Python-3.11-blue.svg)](https://www.python.org/)
[![YOLOv8](https://img.shields.io/badge/YOLOv8-Ultralytics-green.svg)](https://github.com/ultralytics/ultralytics)

## 📌 Description

Ce projet propose un système de **classification automatique des déchets** à partir d'images, en utilisant le modèle de détection d'objets **YOLOv8** (You Only Look Once, version 8). Il s'inscrit dans une démarche d'intelligence artificielle appliquée à la gestion environnementale.

Le modèle est entraîné sur un dataset d'images de déchets redimensionnées, et permet de distinguer différentes catégories de déchets afin de faciliter leur tri et leur recyclage.

---

## 👥 Auteurs

| Nom | Rôle |
|-----|------|
| **Mohamed Ziani** | Développement, entraînement du modèle, documentation |
| **Hamdi Maria** | Prétraitement des données, évaluation, documentation |

---

## 🗂️ Structure du projet

```
project_computer_vision/
│
├── dataset-resized/                  # Dataset d'images (ne pas modifier)
├── garbage_classification_yolov8.ipynb  # Notebook principal (ne pas modifier)
├── requirements.txt                  # Dépendances Python
├── README.md                         # Ce fichier
├── mkdocs.yml                        # Configuration documentation MkDocs
├── .readthedocs.yaml                 # Configuration Read the Docs
└── docs/                             # Documentation académique
    ├── index.md
    ├── installation.md
    ├── dataset.md
    ├── methodology.md
    ├── results.md
    └── conclusion.md
```

---

## ⚙️ Installation

### Prérequis

- Python 3.11+
- pip
- (Recommandé) Un environnement virtuel

### Étapes

```bash
# 1. Cloner le dépôt
git clone https://github.com/votre-utilisateur/project_computer_vision.git
cd project_computer_vision

# 2. Créer un environnement virtuel
python -m venv venv
source venv/bin/activate        # Linux / macOS
venv\Scripts\activate           # Windows

# 3. Installer les dépendances
pip install -r requirements.txt
```

---

## 🚀 Exécution

Ouvrir et exécuter le notebook principal :

```bash
jupyter notebook garbage_classification_yolov8.ipynb
```

Ou via JupyterLab :

```bash
jupyter lab garbage_classification_yolov8.ipynb
```

---

## 📚 Documentation

La documentation complète est disponible en ligne :

👉 [https://project-computer-vision.readthedocs.io](https://project-computer-vision.readthedocs.io)

Pour générer la documentation localement :

```bash
pip install mkdocs
mkdocs serve
```

Puis ouvrir [http://127.0.0.1:8000](http://127.0.0.1:8000) dans votre navigateur.

---

## 🛠️ Technologies utilisées

- [YOLOv8 — Ultralytics](https://github.com/ultralytics/ultralytics)
- [PyTorch](https://pytorch.org/)
- [OpenCV](https://opencv.org/)
- [scikit-learn](https://scikit-learn.org/)
- [MkDocs](https://www.mkdocs.org/)

---

## 📄 Licence

Ce projet est réalisé dans un cadre académique. Toute réutilisation doit mentionner les auteurs.
