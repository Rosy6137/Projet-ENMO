# Notebooks de développement

Versions de travail utilisées pour construire le projet. La version finale est `main.ipynb`, à la racine du dépôt.

| Notebook | Contenu |
|---|---|
| `01_analyse_simple.ipynb` | Première version : chargement, contrôle qualité, correction de calibration, ENMO, indice d'asymétrie et graphiques. |

Par rapport à cette version, `main.ipynb` ajoute : les hypothèses, des vérifications automatiques (OK / ERREUR) après chaque étape, la précision des capteurs, l'analyse par fenêtres de 5 s, le conseil santé et les références.

Ces notebooks lisent les données dans `../data/` et n'enregistrent rien dans `results/`.
