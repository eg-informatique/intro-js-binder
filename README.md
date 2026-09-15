# Introduction à la programmation — JavaScript (Deno) sur Binder

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/eg-informatique/intro-js-binder/HEAD?urlpath=lab/tree/notebooks)

Exercices d'introduction à la programmation en **JavaScript / TypeScript**, exécutés avec **Deno** dans Jupyter, **dans le navigateur, sans rien installer**.

## Pour les élèves

1. Clique sur le bouton **launch binder** ci-dessus, ou ouvre ce lien :
   <https://mybinder.org/v2/gh/eg-informatique/intro-js-binder/HEAD?urlpath=lab/tree/notebooks>
2. Patiente (quelques secondes, ou quelques minutes si l'environnement doit être reconstruit).
3. Ouvre les exercices dans l'ordre depuis le panneau de gauche, et exécute les cellules avec **Shift + Entrée**.

| Notebook | Thème |
|---|---|
| `1_Types-et-Variables.ipynb` | Types et variables |
| `2_Branchements-Conditionnels.ipynb` | Branchements conditionnels |
| `3_Boucles.ipynb` | Boucles |
| `4_Fonctions.ipynb` | Fonctions |

> ⚠️ Une session Binder est **temporaire** : elle s'arrête après ~10 minutes d'inactivité et les fichiers modifiés sont perdus.
> Télécharge régulièrement ton notebook (clic droit sur le fichier → *Download*).

> 💾 Chaque notebook ouvert utilise environ 200 Mo de mémoire, et une session est limitée à 2 Go (indicateur *Mem* en bas de l'écran).
> **Ferme les notebooks dont tu n'as plus besoin** : leur noyau s'arrête et la mémoire est libérée.
> Si JupyterLab affiche « Server Connection Error », relance Binder avec le lien ci-dessus.

## Pour les enseignants

### Contenu

| Fichier | Rôle |
|---|---|
| `environment.yml` | Installe JupyterLab et Deno (depuis conda-forge). |
| `postBuild` | Enregistre le noyau Deno (seul noyau proposé), et libère la mémoire des notebooks fermés (arrêt du noyau à la fermeture, arrêt des noyaux inactifs). |
| `notebooks/` | Les 4 séries d'exercices (noyau **Deno**). |

Les notebooks sont des copies des exercices du dépôt [1m](https://github.com/eg-informatique/1m) (`intro-js/`, sans les corrections) :

| Ici | Source dans `1m/intro-js/` |
|---|---|
| `1_Types-et-Variables.ipynb` | `types_variables/Types-Variables_Exercices.ipynb` |
| `2_Branchements-Conditionnels.ipynb` | `branchements_conditionnels/Branchements-Conditionnels.ipynb` |
| `3_Boucles.ipynb` | `boucles/Boucles.ipynb` (noyau passé de Node.js à Deno) |
| `4_Fonctions.ipynb` | `fonctions/Fonctions.ipynb` |

Après une modification dans `1m`, recopier le notebook ici sous son nouveau nom, puis faire un `git push`.

### Avant le cours

Binder reconstruit l'environnement après chaque `git push` (quelques minutes). Ouvrir le lien soi-même une fois après chaque modification, pour que les élèves trouvent un environnement déjà prêt.

### Tester localement

```bash
pip install jupyter-repo2docker   # nécessite Docker
repo2docker .
```
