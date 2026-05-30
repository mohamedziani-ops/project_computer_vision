# Résultats

## Métriques d'évaluation

Les performances du modèle YOLOv8 entraîné sur le dataset de classification de déchets sont évaluées à l'aide des métriques standard en vision par ordinateur :

| Métrique | Description |
|----------|-------------|
| **Précision (P)** | Proportion des détections correctes parmi toutes les détections effectuées |
| **Rappel (R)** | Proportion des objets réels correctement détectés |
| **mAP@0.5** | Précision moyenne calculée à un seuil IoU de 0.5 |
| **mAP@0.5:0.95** | Précision moyenne calculée sur plusieurs seuils IoU (de 0.5 à 0.95) |
| **F1-Score** | Moyenne harmonique entre précision et rappel |

---

## Performances globales

Les résultats ci-dessous sont obtenus sur l'ensemble de **test**, après entraînement complet du modèle.

| Métrique | Valeur obtenue |
|----------|----------------|
| Précision (P) | à compléter après expérience |
| Rappel (R) | à compléter après expérience |
| mAP@0.5 | à compléter après expérience |
| mAP@0.5:0.95 | à compléter après expérience |
| F1-Score | à compléter après expérience |

!!! info "Mise à jour des résultats"
    Les valeurs ci-dessus seront complétées à l'issue de l'exécution complète du notebook `garbage_classification_yolov8.ipynb`. Les résultats dépendent des paramètres d'entraînement et du matériel utilisé.

---

## Performances par classe

| Classe | Précision | Rappel | mAP@0.5 |
|--------|-----------|--------|---------|
| Plastique | — | — | — |
| Verre | — | — | — |
| Métal | — | — | — |
| Papier / Carton | — | — | — |
| Organique | — | — | — |
| Autre | — | — | — |

---

## Courbes d'apprentissage

L'évolution des métriques au cours de l'entraînement (perte d'entraînement, perte de validation, mAP) est tracée et sauvegardée automatiquement par Ultralytics dans le dossier `runs/` lors de l'exécution du notebook.

Les courbes typiquement observées incluent :

- **Loss courbe** : décroissance progressive de la perte totale (classification + localisation) au fil des époques
- **mAP courbe** : augmentation progressive de la précision moyenne sur l'ensemble de validation
- **Courbe Précision-Rappel** : analyse du compromis précision/rappel par classe

---

## Matrice de confusion

La matrice de confusion permet de visualiser les erreurs de classification entre les différentes catégories de déchets. Elle est générée automatiquement à la fin de l'entraînement et permet d'identifier les classes les plus susceptibles d'être confondues par le modèle.

---

## Analyse des erreurs

Les principales sources d'erreur identifiées sont :

- **Confusions inter-classes** : certains déchets partagent des caractéristiques visuelles similaires (ex. : emballages plastiques et cartons)
- **Déséquilibre des classes** : les classes sous-représentées dans le dataset tendent à obtenir des scores de rappel plus faibles
- **Qualité des images** : les images de faible résolution ou prises dans des conditions d'éclairage défavorables induisent davantage d'erreurs

---

## Comparaison avec l'état de l'art

YOLOv8 représente l'une des architectures les plus performantes pour la détection d'objets en temps réel. Par rapport aux versions précédentes (YOLOv5, YOLOv7), il offre une meilleure précision à vitesse d'inférence comparable, grâce à des améliorations architecturales significatives (tête de détection *anchor-free*, meilleure agrégation des features).
