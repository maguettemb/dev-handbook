# Dev Handbook

Carnet de route pour la transition Data Scientist → Software Engineer, documenté au fur et à mesure d'un projet fil rouge.

## Lancer le site en local

```bash
python -m venv .venv
source .venv/bin/activate  # ou .venv\Scripts\activate sous Windows
pip install -r requirements.txt
mkdocs serve
```

Le site est alors disponible sur `http://127.0.0.1:8000`.

## Déploiement

Le site se déploie automatiquement sur GitHub Pages à chaque push sur `main`, via `.github/workflows/deploy.yml`.

Pour un déploiement manuel :

```bash
mkdocs gh-deploy --force
```

## Structure

```
docs/
├── index.md              # Page d'accueil
├── journal.md             # Journal de bord du projet fil rouge
├── 01-setup/               # Setup environnement
├── 02-organisation/        # Organisation d'un projet
├── 03-code-propre/         # Bonnes pratiques de code
├── 04-environnements/      # Environnements & dépendances
├── 05-cicd/                 # CI/CD
├── 06-deploiement/          # Déploiement
└── 07-outils-ia/            # Outils IA pour développer
```

Chaque page de contenu (hors index de section) suit un template commun : Objectif, Ce que j'ai fait, Pour/Contre, Ce que j'ai appris, Ressources.
