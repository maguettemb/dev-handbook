# Gestion des versions Python (pyenv / uv / poetry)


## Objectif


En data science, on utilise souvent le Python système ou Anaconda sans trop se poser de questions.
En développement logiciel, isoler chaque projet dans son propre environnement, avec des dépendances figées et reproductibles, est une pratique de base et indispensable pour que le projet tourne pareil sur une autre machine ou en CI.

## Ce que j'ai fait

### Installation de uv

Il ne faut pas utiiliser le Python du sytème macOS parce qu'il est ancien, partagé et risqué à être modifié. 
On installe d'abord uv (similaire à pip) mais va gérer à la fois les versions de Python et les environnements virtuels. 
Il est aussi plus rapide que pip et venv

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

<!--
!!! note "Statut"
    :material-progress-clock: curl -LsSf https://astral.sh/uv/install.sh | sh -->

On vérifie la bonne installation avec:

```bash
curl uv --version
```
### Création de l'environnement virtuel du projet 

```bash
uv venv 
```
Avec python:
 ```bash
python -m venv venv
```
(la différence entre les 2: )

On l'active avec: 
```bash
source .venv/bin/activate 
```
Si on utilise uv, on installe les dépendances avec la syntaxe:
```bash uv pip install fastapi "uvicorn[standard]" ```

Si c'est pip : 
```bash pip install fastapi "uvicorn[standard]" ````

Les dépendances peuvent être figées pour le reproducibilité avec requirements.txt

```bash uv pip freeze > requirements.txt

!!! tip "Craftsmanship — jamais le Python système"
    Ne jamais coder directement avec le Python système de macOS (ancien, partagé entre tous les outils, risqué à modifier). Isoler ses environnements dès le premier jour évite la majorité des "ça marche pas chez moi".

!!! warning "Craftsmanship — .venv ne se commit jamais"
    Un environnement virtuel se recrée à partir de `requirements.txt`, il ne se partage pas via Git. D'où l'importance du `.gitignore` posé en amont.


## Pour / Contre

| Outil | Pour | Contre |
|---|---|---|
| **uv** | Très rapide (écrit en Rust), gère versions Python + venv + packages en un seul outil, remplace pip/venv/pyenv | Récent, écosystème encore jeune |
| **venv + pip** | Standard, inclus nativement dans Python, aucune installation | Lent, pas de gestion de version Python, `requirements.txt` moins fiable qu'un vrai lockfile |
| **conda** | Gère aussi des dépendances non-Python (utile en data science : CUDA, libs C) | Lourd, lent, moins adapté à un vrai projet logiciel/prod |
| **poetry** | Gestion de dépendances très propre avec lockfile, bon pour publier des packages | Plus lent qu'uv, courbe d'apprentissage un peu plus longue |

## Ce que j'ai appris

- La différence entre installer une dépendance (`pip install` classique) et **figer** une dépendance (`pip freeze` / lockfile) : la première fixe une version au moment T, mais sans fichier figé, une réinstallation plus tard peut tirer des versions différentes et casser le projet silencieusement.
- `uv` remplace en un seul outil ce que je faisais avec plusieurs (conda pour les envs, pip pour les packages) — plus simple à retenir.

## Ressources

- [Documentation uv](https://docs.astral.sh/uv/)
Colle ça, commit, push, et on repart sur la suite du projet (le fichier main.py et le test de /health si ce n'est pas encore fait).eClaude is AI and can make mistakes. Please double-check responses.