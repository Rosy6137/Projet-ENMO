# Données

Données brutes d'accélération des 4 capteurs, une ligne par mesure (environ 100 mesures par seconde).

| Fichier | Participant | Poignet | Capteur | Début → fin | Mesures |
|---|---|---|---|---|---|
| `gauche_Daniel.csv` | Daniel (gaucher) | gauche | AX6 | 14:32:36 → 14:50:40 | 107 040 |
| `droite_Daniel.csv` | Daniel (gaucher) | droit | AX3 | 14:33:11 → 14:51:10 | 108 720 |
| `gauche_Said.csv` | Said (droitier) | gauche | AX6 | 15:03:34 → 15:18:29 | 88 400 |
| `droite_Said.csv` | Said (droitier) | droit | AX3 | 15:03:42 → 15:18:34 | 89 760 |

## Format
Pas de ligne d'en-tête. 4 colonnes :

| Colonne | Contenu | Unité |
|---|---|---|
| 1 | Date et heure de la mesure (`2026-11-07 15:03:42.479`) | — |
| 2 | Accélération sur l'axe x | g |
| 3 | Accélération sur l'axe y | g |
| 4 | Accélération sur l'axe z | g |

## Heures des tâches (2 minutes chacune)
| Tâche | Daniel | Said |
|---|---|---|
| Repos assis | 14:36 → 14:38 | 15:07 → 15:09 |
| Écriture | 14:39 → 14:41 | 15:10 → 15:12 |
| Clavier | 14:43 → 14:45 | 15:13 → 15:15 |
| Marche | 14:47 → 14:49 | 15:16 → 15:18 |
