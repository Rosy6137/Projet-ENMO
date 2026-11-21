# Projet ENMO : asymétrie bras droit / bras gauche selon la dominance manuelle

Projet de M2 Santé Physique.

**Question scientifique :** la dominance manuelle (droitier ou gaucher) entraîne-t-elle une asymétrie mesurable de l'accélération entre le bras droit et le bras gauche selon le type d'activité réalisée ?

## Protocole
- 2 participants : Daniel (gaucher) et Said (droitier)
- Un accéléromètre à chaque poignet : Axivity AX6 à gauche, AX3 à droite, environ 100 Hz
- 4 tâches de 2 minutes : repos assis, écriture manuscrite, clavier, marche à vitesse normale

## Lancer la démonstration
```bash
pip install -r requirements.txt
jupyter notebook main.ipynb
```
Puis exécuter toutes les cellules (menu *Run → Run All Cells*).

## Organisation du dépôt
| Élément | Contenu |
|---|---|
| `main.ipynb` | Tout le code et la démonstration : données → qualité → calibration → ENMO → indice → graphiques → interprétation |
| `data/` | Données brutes exportées des capteurs (`<côté>_<participant>.csv` : temps, x, y, z en g) |
| `figures/` | Graphiques générés par le notebook |

## Méthode
1. **Contrôle qualité** : fréquence d'échantillonnage, trous, valeurs manquantes.
2. **Correction de calibration** : la norme de chaque capteur est divisée par sa norme moyenne au repos, qui doit valoir 1 g.
3. **ENMO** = max(‖a‖ − 1 g, 0), moyenné sur chaque tâche.
4. **Indice d'asymétrie** = (ENMO droit − ENMO gauche) / (ENMO droit + ENMO gauche), calculé pour chaque participant. Il vaut 0 si le mouvement est symétrique, +1 si tout vient du bras droit, −1 si tout vient du bras gauche.

## Résultat principal
Pendant l'écriture, l'indice est négatif chez le gaucher (−0,55) et positif chez le droitier (+0,81) : la dominance manuelle est visible dans les données d'accélération. La marche reste quasi symétrique.
