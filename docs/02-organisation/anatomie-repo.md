# Anatomie d'un repo propre

## Objectif

Un repo bien structuré dès le départ évite les gros refactorings plus tard, et permet à n'importe qui (collègue ou CI) de comprendre le projet en quelques secondes.

## Ce que j'ai fait

Sur le mini-projet `mini-projet-api`, structure posée avant la moindre ligne de code métier :

```bash
mini-projet-api/
├── .git/
├── .gitignore
├── .venv/          # jamais commité
├── README.md
├── requirements.txt
└── src/
    └── main.py
```

!!! tip "Craftsmanship — Git init avant le code"
    `git init` se fait **avant** d'écrire la moindre ligne de code, pas après. Chaque étape devient un commit traçable dès le début, pas un gros commit fourre-tout à la fin.

!!! tip "Craftsmanship — README avant le code"
    Écrire le README en premier force à clarifier l'intention du projet avant de foncer dans le code.

!!! warning "Craftsmanship — .gitignore avant tout fichier sensible"
    Le `.gitignore` se crée **avant** le premier `.env` ou la première dépendance installée. Une fois qu'un secret est commité — même supprimé ensuite — il reste dans l'historique Git.

!!! info "Craftsmanship — /health dès le départ"
    Un endpoint `/health` dès le premier fichier de code : convention standard pour vérifier qu'une app est vivante. Indispensable plus tard pour la CI, le monitoring, et Kubernetes.

## Pour / Contre

| Pour | Contre |
|---|---|
| Structure claire dès le départ = moins de dette technique | Peut sembler "lent" au début vs juste ouvrir un fichier et coder |
| Reproductible par n'importe qui via `requirements.txt` | Discipline à maintenir (facile de sauter une étape sous pression) |

## Ce que j'ai appris

*À compléter au fil du projet.*

## Ressources

- [Documentation FastAPI](https://fastapi.tiangolo.com/)