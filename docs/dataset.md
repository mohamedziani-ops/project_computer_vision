# Jeu de données

## Présentation

Le jeu de données utilisé dans ce projet est un ensemble d'images de déchets issus de sources publiques, préalablement redimensionnées et organisées en vue de l'entraînement du modèle YOLOv8.

Le dossier `dataset-resized/` contient l'intégralité des images prétraitées. Ce dossier ne doit pas être modifié manuellement afin de garantir la reproductibilité des expériences.

---

## Catégories de déchets

Le dataset couvre plusieurs catégories de déchets couramment rencontrés dans les filières de tri sélectif :

| Catégorie | Description |
|-----------|-------------|
| Plastique | Bouteilles, emballages, sacs plastiques |
| Verre | Bouteilles, bocaux, vitres |
| Métal | Canettes, boîtes de conserve, ferraille |
| Papier / Carton | Journaux, boîtes, emballages cartonnés |
| Organique | Déchets alimentaires, végétaux |
| Autre | Déchets non classifiables dans les catégories précédentes |

---

## Structure du dossier

```
dataset-resized/
├── train/
│   ├── images/
│   └── labels/
├── val/
│   ├── images/
│   └── labels/
└── test/
    ├── images/
    └── labels/
```

---

## Prétraitement appliqué

Les images ont été soumises aux traitements suivants avant l'entraînement :

- **Redimensionnement** : toutes les images ont été normalisées à une résolution uniforme (par exemple 640×640 pixels), conformément aux exigences de YOLOv8.
- **Normalisation des pixels** : les valeurs de pixels ont été mises à l'échelle dans l'intervalle [0, 1].
- **Augmentation des données** (*Data Augmentation*) : application de transformations aléatoires (rotations, retournements horizontaux, modifications de luminosité et de contraste) afin d'améliorer la robustesse du modèle et de réduire le surapprentissage.

---

## Répartition des données

| Ensemble | Proportion | Utilisation |
|----------|------------|-------------|
| Entraînement (`train`) | ~70 % | Optimisation des paramètres du modèle |
| Validation (`val`) | ~15 % | Réglage des hyperparamètres |
| Test (`test`) | ~15 % | Évaluation finale des performances |

---

## Considérations éthiques et de qualité

Les images ont été collectées dans le respect des licences ouvertes. Le dataset peut présenter un déséquilibre entre les classes, ce qui a été pris en compte lors de la phase d'entraînement. Des techniques de rééchantillonnage ou de pondération des classes peuvent être appliquées pour corriger ce biais.

!!! note
    Le dossier `dataset-resized/` est fourni tel quel et ne doit pas être modifié. Toute altération de ce dossier pourrait compromettre la reproductibilité des résultats présentés dans ce projet.
