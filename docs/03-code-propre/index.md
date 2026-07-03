# 3. Écrire du code propre

Les pratiques qui rendent le code lisible, fiable, et sûr à modifier — surtout à plusieurs.

## Ce que couvre cette section

- **[Linters & formatters](linters.md)** — ruff, black, mypy
- **[Tests](tests.md)** — pytest, structure des tests, couverture
- **[Pre-commit hooks](pre-commit.md)** — automatiser les vérifications avant chaque commit
- **[Code review](code-review.md)** — comment lire et écrire une pull request utile

## Pourquoi c'est nouveau venant de la data science

Le code d'un notebook n'a en général pas besoin d'être relu par quelqu'un d'autre ni de survivre plusieurs mois sans modification. Le code de production, si — d'où l'importance des tests et de la revue de code, qui remplacent la "confiance sur parole".
