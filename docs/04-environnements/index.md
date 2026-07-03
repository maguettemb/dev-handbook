# 4. Environnements & dépendances

Isoler et reproduire les dépendances d'un projet, du poste local au conteneur de production.

## Ce que couvre cette section

- **[venv vs conda vs poetry vs uv](comparatif.md)** — comparatif détaillé pour choisir selon le contexte
- **[Docker](docker.md)** — pourquoi conteneuriser, Dockerfile de base, multi-stage builds

## Le lien avec le déploiement

Un environnement mal maîtrisé en local se paie cher au déploiement. Comprendre la différence entre un environnement de dev (venv/poetry) et une image de production (Docker) est central pour la suite du handbook.
