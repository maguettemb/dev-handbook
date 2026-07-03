# 2. Organisation d'un projet

Comment structurer un projet pour qu'il soit lisible, maintenable, et prêt pour la production — au-delà du notebook exploratoire.

## Ce que couvre cette section

- **[Anatomie d'un repo propre](anatomie-repo.md)** — arborescence type, README, conventions
- **[Notebook vs package Python](notebook-vs-package.md)** — quand et comment faire la transition
- **[Gestion des secrets](secrets.md)** — .env, Vault, ce qu'on ne commit jamais

## Le changement de mentalité

Un projet data science type est souvent linéaire : données → notebook → résultat. Un projet software est modulaire : le code est découpé en composants réutilisables, testés indépendamment, et pensé pour être maintenu par plusieurs personnes dans la durée.
