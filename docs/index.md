# Classification des Déchets par Vision par Ordinateur

## Présentation du projet

Ce projet académique s'inscrit dans le domaine de la **vision par ordinateur** appliquée à la **gestion des déchets**. Il propose un système automatisé de classification d'images de déchets à l'aide du modèle **YOLOv8**, développé par Ultralytics.

L'objectif principal est de concevoir un modèle capable d'identifier et de classer différentes catégories de déchets à partir d'images, dans le but de soutenir les efforts de tri sélectif et de recyclage.

---

## Auteurs

- **Mohamed Ziani** — Université Moulay Ismail
- **Hamdi Maria** — Université Moulay Ismail

---

## Contexte et motivation

La gestion des déchets constitue l'un des défis environnementaux majeurs de notre époque. L'automatisation du tri des déchets, via des systèmes intelligents de reconnaissance d'images, représente une solution prometteuse pour améliorer l'efficacité des filières de recyclage.

Grâce aux avancées récentes en apprentissage profond — et en particulier aux architectures de type YOLO (*You Only Look Once*) —, il est désormais possible de développer des systèmes de détection et de classification rapides, précis et adaptés à des contraintes industrielles réelles.

---

## Structure de la documentation

| Section | Description |
|---------|-------------|
| [Installation](installation.md) | Mise en place de l'environnement de développement |
| [Jeu de données](dataset.md) | Description et prétraitement du dataset |
| [Méthodologie](methodology.md) | Architecture du modèle et protocole d'entraînement |
| [Résultats](results.md) | Métriques d'évaluation et analyse des performances |
| [Conclusion](conclusion.md) | Bilan, limites et perspectives |

---

## Technologies principales

- **YOLOv8** (Ultralytics) — Détection et classification d'objets
- **PyTorch** — Framework d'apprentissage profond
- **OpenCV** — Traitement d'images
- **scikit-learn** — Métriques d'évaluation
