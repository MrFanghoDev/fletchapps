# Instructions pour Claude sur FletchApps

Pour notre façon de travailler ensemble (commune aux trois projets
frères -- fletchapps/fletchscore/fletchtime), voir le `CLAUDE.md` global
(`~/.claude/CLAUDE.md`), toujours chargé automatiquement. Ce fichier-ci
reste volontairement court : FletchApps est un projet simple.

## Contexte en une phrase

FletchApps est le portail statique (une seule page, `index.html` +
`theme.css`, aucune dépendance/build) qui présente et relie FletchScore
et FletchTime.

## Conventions techniques

- HTML/CSS pur, pas de framework ni d'étape de build -- garder ça ainsi
  sauf besoin réel et discuté.
- `theme.css` définit les tokens visuels (couleurs dont `--gold`,
  typographie) réutilisés par la page -- toute modification de palette
  ici a des chances de devoir être répercutée dans l'identité visuelle
  des deux autres projets (`branding/` côté FletchScore,
  `docs/_static/logo.svg` et assets côté FletchTime) : vérifier plutôt
  que de supposer que c'est isolé à ce dépôt.
- Pas de suite de tests ni de CI pour l'instant -- vérifier un
  changement en ouvrant réellement `index.html` (rendu, liens vers les
  deux autres projets, focus clavier vu le `:focus-visible` déjà en
  place) plutôt que par relecture du HTML/CSS seule.

## Erreurs déjà commises, à ne pas répéter

*Rien de spécifique consigné pour l'instant -- section à tenir à jour au
fil des sessions.*
