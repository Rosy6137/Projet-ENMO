# Projet ENMO : asymétrie bras droit / bras gauche selon la main dominante

Projet du cours **HAH913E : Physical activity for health** (M2 Santé Physique).

**Question scientifique :** la main dominante (droitier ou gaucher) entraîne-t-elle une asymétrie mesurable de l'accélération entre le bras droit et le bras gauche, selon le type d'activité ?

**Résultat principal :** pendant l'écriture, l'indice d'asymétrie est négatif chez le gaucher (−0,55) et positif chez le droitier (+0,81). L'inversion se retrouve dans 22/24 et 24/24 fenêtres de 5 secondes. La marche reste presque symétrique.

## Lancer la démonstration
1. Installer Python avec les bibliothèques nécessaires (par exemple avec [Anaconda](https://www.anaconda.com/)), ou :
   ```bash
   pip install -r requirements.txt
   ```
2. Ouvrir `main.ipynb` (Jupyter ou VS Code) **depuis le dossier du dépôt**.
3. Exécuter toutes les cellules (*Run All*). Le notebook vérifie chaque étape (OK / ERREUR) et enregistre les figures et le tableau dans `results/`.

## Organisation du dépôt
| Élément | Contenu |
|---|---|
| `main.ipynb` | **Point d'entrée** : démonstration complète du projet |
| `notebooks/` | Notebooks de développement (versions précédentes de l'analyse) |
| `data/` | Données brutes des 4 capteurs (CSV) |
| `results/` | Résultats générés par `main.ipynb` : figures (PNG et PDF) et tableau (CSV) |
| `requirements.txt` | Bibliothèques Python nécessaires |

Chaque dossier contient son propre `readme.md`.

## Dispositif de mesure
- **Participants :** 2 (Daniel, gaucher ; Said, droitier).
- **Capteurs :** Axivity **AX6 au poignet gauche**, **AX3 au poignet droit**, environ 100 mesures par seconde. L'AX3 enregistre jusqu'à ±8 g, avec une précision de 15,6 mg ; l'AX6 a une précision de 0,24 mg.
- **Tâches :** 4 tâches de 2 minutes, dans le même ordre pour les deux participants :
  1. **Repos assis**, bras posés sur la table (condition de référence) ;
  2. **Écriture manuscrite**, copie d'un texte avec la main habituelle ;
  3. **Clavier**, saisie d'un texte sur ordinateur ;
  4. **Marche** à vitesse normale sur un parcours plat.
- **Données :** les heures de début et de fin de chaque tâche ont été notées pendant la séance (7 novembre 2026). Les enregistrements ont ensuite été exportés en CSV (temps, x, y, z en g).

## Méthode
1. **Contrôle qualité :** fréquence, trous, valeurs manquantes, précision, saturation, durée de chaque tâche.
2. **Correction de calibration :** au repos, la norme doit valoir 1 g. Les capteurs mesuraient de 0,949 à 1,040 g, donc la norme de chaque capteur est divisée par sa valeur moyenne au repos.
3. **ENMO** = max(‖a‖ − 1 g, 0), en mg (van Hees et al., 2013).
4. **Indice d'asymétrie** = (ENMO droit − ENMO gauche) / (ENMO droit + ENMO gauche), calculé pour chaque participant : 0 = symétrique, +1 = tout à droite, −1 = tout à gauche.
5. **Solidité :** indice recalculé sur des fenêtres de 5 s.
6. **Interprétation et conseil santé.**

## Équipe
*À compléter : noms des membres du groupe.*
