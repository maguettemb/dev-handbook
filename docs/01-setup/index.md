# 1. Setup de l'environnement

Première étape de toute transition vers le software engineering : avoir un environnement de travail solide, reproductible, et compris — pas juste "ça marche sur ma machine".

## Ce que couvre cette section

- **[Terminal & shell](terminal.md)** — sortir de l'IDE tout-en-un et être à l'aise en ligne de commande
- **[Git & GitHub](git-github.md)** — versionner son code, pas seulement le sauvegarder
- **[VS Code](vscode.md)** — configuration et extensions pour du développement Python sérieux
- **[Gestion des versions Python](python-versions.md)** — pyenv, uv, poetry : lequel pour quel usage
- **[Claude Code](claude-code.md)** — utiliser un agent de code en ligne de commande efficacement

## Pourquoi ça compte particulièrement venant de la data science

En data science, on travaille souvent dans un seul environnement (Jupyter, Colab, Anaconda) sans trop se soucier de reproductibilité stricte ou de la différence entre plusieurs versions de Python. En software engineering, l'environnement de dev doit être :

- **Reproductible** — un collègue (ou une CI) doit pouvoir le recréer à l'identique
- **Isolé** — pas de pollution entre projets
- **Documenté** — pour que l'onboarding d'un nouveau dev soit rapide
