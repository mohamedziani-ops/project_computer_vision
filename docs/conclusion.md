# Conclusion

## Bilan du projet

Ce projet a permis de mettre en œuvre un pipeline complet de **classification d'images de déchets** basé sur le modèle **YOLOv8**, depuis la préparation du jeu de données jusqu'à l'évaluation des performances du modèle entraîné.

Les principaux apports de ce travail sont les suivants :

- **Maîtrise du framework Ultralytics YOLOv8** pour des tâches de classification et de détection d'objets
- **Mise en pratique du transfert d'apprentissage** sur un dataset de taille limitée
- **Application des bonnes pratiques** de développement en apprentissage automatique : séparation train/val/test, augmentation des données, suivi des métriques
- **Développement d'une documentation technique professionnelle** déployée sur Read the Docs

---

## Limites identifiées

Malgré les résultats encourageants obtenus, plusieurs limitations méritent d'être soulignées :

### Limitations liées aux données

- Le dataset peut présenter un **déséquilibre entre les classes**, ce qui peut biaiser les performances en faveur des classes majoritaires.
- La **diversité visuelle** des images est limitée : variations d'éclairage, d'angle de vue et d'arrière-plan insuffisantes pour garantir une bonne généralisation en conditions réelles.

### Limitations liées au modèle

- L'utilisation d'une variante légère de YOLOv8 (*nano* ou *small*) représente un compromis acceptable dans un contexte académique, mais une variante plus grande (*medium*, *large*, *xlarge*) permettrait d'obtenir de meilleures performances.
- L'entraînement sur CPU ou sur un GPU d'entrée de gamme limite le nombre d'époques et la taille de lot utilisables.

---

## Perspectives et améliorations futures

Plusieurs pistes d'amélioration sont envisageables pour donner suite à ce projet :

| Axe | Amélioration proposée |
|-----|----------------------|
| **Données** | Enrichissement du dataset par collecte d'images supplémentaires et techniques d'augmentation avancées |
| **Modèle** | Expérimentation avec des variantes plus puissantes de YOLOv8 ou d'autres architectures (RT-DETR, EfficientDet) |
| **Déploiement** | Intégration du modèle dans une application web ou mobile via une API REST |
| **Temps réel** | Adaptation du pipeline pour le traitement de flux vidéo en temps réel |
| **Évaluation** | Mise en place d'une validation croisée (*k-fold cross-validation*) pour une évaluation plus robuste |

---

## Applications potentielles

Ce type de système de classification automatique des déchets peut trouver des applications concrètes dans :

- Les **centres de tri automatisés** pour assister ou remplacer le tri manuel
- Les **applications mobiles** permettant aux citoyens de connaître le bac approprié pour un déchet donné
- La **surveillance de sites** (parcs, rues) pour détecter les dépôts sauvages de déchets
- Les **systèmes robotisés** de collecte et de tri des déchets industriels

---

## Remerciements

Les auteurs remercient leurs encadrants pédagogiques pour leur accompagnement tout au long de ce projet, ainsi que la communauté *open source* Ultralytics pour la mise à disposition du modèle YOLOv8.

---

## Références

1. Jocher, G., Chaurasia, A., & Qiu, J. (2023). *Ultralytics YOLOv8*. [https://github.com/ultralytics/ultralytics](https://github.com/ultralytics/ultralytics)
2. Redmon, J., & Farhadi, A. (2018). *YOLOv3: An Incremental Improvement*. arXiv:1804.02767.
3. Wang, C.-Y., Bochkovskiy, A., & Liao, H.-Y. M. (2023). *YOLOv7: Trainable bag-of-freebies sets new state-of-the-art for real-time object detectors*. CVPR 2023.
4. He, K., Zhang, X., Ren, S., & Sun, J. (2016). *Deep Residual Learning for Image Recognition*. CVPR 2016.
5. Lin, T.-Y. et al. (2017). *Feature Pyramid Networks for Object Detection*. CVPR 2017.
