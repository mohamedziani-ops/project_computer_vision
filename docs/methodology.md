# Méthodologie

## Vue d'ensemble

L'approche adoptée dans ce projet repose sur l'utilisation du modèle **YOLOv8** (*You Only Look Once, version 8*) pour la classification d'images de déchets. YOLOv8 est une architecture de réseau de neurones convolutifs de pointe, développée par Ultralytics, qui offre un excellent compromis entre précision et rapidité d'inférence.

---

## Architecture du modèle

### YOLOv8 — Principes fondamentaux

YOLOv8 est un modèle de détection d'objets en temps réel qui prédit simultanément les classes et les boîtes englobantes (*bounding boxes*) des objets présents dans une image, en un seul passage (*single-stage detection*).

L'architecture se décompose en trois parties principales :

| Composant | Rôle |
|-----------|------|
| **Backbone** (CSPDarknet) | Extraction des caractéristiques visuelles multi-échelles |
| **Neck** (PANet) | Agrégation des features maps à différentes résolutions |
| **Head** | Prédiction des classes et des coordonnées des boîtes englobantes |

### Variante utilisée

Dans ce projet, nous utilisons la variante **YOLOv8n** (*nano*) ou **YOLOv8s** (*small*), adaptée à un contexte académique avec des ressources matérielles limitées, tout en maintenant des performances satisfaisantes.

---

## Protocole d'entraînement

### Paramètres principaux

| Paramètre | Valeur |
|-----------|--------|
| Taille d'entrée | 640 × 640 pixels |
| Nombre d'époques | 50–100 |
| Taille du lot (*batch size*) | 16 |
| Optimiseur | SGD / AdamW |
| Taux d'apprentissage initial | 0.01 |
| Fonction de perte | CIoU + BCE |

### Stratégie d'entraînement

1. **Transfert d'apprentissage** (*Transfer Learning*) : le modèle est initialisé avec des poids pré-entraînés sur le dataset COCO, ce qui permet d'accélérer la convergence et d'améliorer les performances sur un dataset de taille limitée.

2. **Fine-tuning** : les couches du réseau sont progressivement dégelées pour adapter les représentations apprises au domaine spécifique des déchets.

3. **Early stopping** : l'entraînement est interrompu automatiquement si les performances sur l'ensemble de validation ne s'améliorent plus pendant un nombre défini d'époques consécutives.

---

## Pipeline de traitement

```
Image brute
    ↓
Redimensionnement (640×640)
    ↓
Normalisation [0, 1]
    ↓
Augmentation des données (train uniquement)
    ↓
Inférence YOLOv8
    ↓
Post-traitement (NMS)
    ↓
Classe prédite + Score de confiance
```

---

## Augmentation des données

Les transformations suivantes ont été appliquées lors de la phase d'entraînement afin d'améliorer la généralisation du modèle :

- Retournement horizontal aléatoire
- Rotation aléatoire (±10°)
- Modification aléatoire de la luminosité et du contraste
- Recadrage aléatoire (*random crop*)
- Mosaïque (*Mosaic augmentation*, spécifique à YOLOv8)

---

## Environnement d'expérimentation

| Composant | Détail |
|-----------|--------|
| Langage | Python 3.11 |
| Framework | PyTorch 2.x |
| Librairie principale | Ultralytics YOLOv8 |
| Environnement d'exécution | Jupyter Notebook |
| Matériel | GPU NVIDIA (si disponible) / CPU |
