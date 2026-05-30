# Installation

Cette section décrit les étapes nécessaires pour configurer l'environnement de développement et exécuter le projet sur votre machine locale.

---

## Prérequis système

| Composant | Version minimale recommandée |
|-----------|------------------------------|
| Python | 3.11+ |
| pip | 23.0+ |
| RAM | 8 Go (16 Go recommandé) |
| GPU (optionnel) | Compatible CUDA 11.8+ |

!!! note "GPU"
    L'utilisation d'un GPU compatible CUDA est fortement recommandée pour accélérer l'entraînement du modèle. En l'absence de GPU, l'entraînement s'effectuera sur CPU, ce qui allongera considérablement les temps de calcul.

---

## Étapes d'installation

### 1. Cloner le dépôt

```bash
git clone https://github.com/votre-utilisateur/project_computer_vision.git
cd project_computer_vision
```

### 2. Créer un environnement virtuel

Il est fortement conseillé d'isoler les dépendances du projet dans un environnement virtuel Python.

=== "Linux / macOS"
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

=== "Windows"
    ```bash
    python -m venv venv
    venv\Scripts\activate
    ```

### 3. Installer les dépendances

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Vérifier l'installation

```bash
python -c "import ultralytics; ultralytics.checks()"
```

Une sortie sans erreur confirme que YOLOv8 est correctement installé.

---

## Lancer le notebook

```bash
jupyter notebook garbage_classification_yolov8.ipynb
```

Ou avec JupyterLab :

```bash
jupyter lab garbage_classification_yolov8.ipynb
```

---

## Génération de la documentation locale

```bash
mkdocs serve
```

La documentation est ensuite accessible à l'adresse : [http://127.0.0.1:8000](http://127.0.0.1:8000)

---

## Résolution des problèmes courants

!!! warning "Erreur CUDA non disponible"
    Si PyTorch ne détecte pas de GPU, vérifiez que la version de CUDA installée sur votre système est compatible avec la version de PyTorch. Consultez [pytorch.org](https://pytorch.org/get-started/locally/) pour installer la version adaptée.

!!! tip "Conflit de dépendances"
    En cas de conflit, recréez l'environnement virtuel depuis zéro et réinstallez les dépendances avec `pip install -r requirements.txt`.
