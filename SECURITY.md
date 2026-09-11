# Politique de sécurité

*[English version below](#security-policy)*

## Portée

FletchApps n'a **aucun serveur** : c'est une page web purement statique
(HTML/CSS, hébergée sur GitHub Pages), sans compte ni donnée utilisateur.
La seule logique dynamique est un script qui interroge l'API GitHub
(`api.github.com`) pour afficher la version/le statut de chaque projet
frère -- le résultat est inséré via `textContent` (jamais `innerHTML`),
donc pas de surface d'injection de script réaliste même si cette
réponse était un jour forgée.

Sont notamment dans le périmètre :
- Toute faille qui permettrait d'injecter du contenu exécutable dans la
  page malgré ce qui précède
- Une dérive de `theme.css`/`index.html` qui romprait le
  `:focus-visible`/l'accessibilité de façon à tromper l'utilisateur
  (ex. lien masqué redirigeant ailleurs que son texte ne l'indique)

Hors périmètre (comportement attendu, pas une faille) :
- Les requêtes vers `api.github.com` (chargement des statuts/versions)
  révèlent à GitHub l'IP de qui consulte la page -- comportement
  inhérent à tout appel à une API tierce, pas une fuite propre à
  FletchApps
- FletchApps lui-même ne collecte, ne reçoit, ni ne transmet aucune
  donnée personnelle -- pas de serveur, pas de compte, pas de
  télémétrie

## Signaler une faille

**Ne pas** ouvrir une Issue publique pour une faille de sécurité tant
qu'elle n'est pas corrigée. Contacte plutôt le mainteneur directement :

- Via l'onglet **Security** du dépôt GitHub
  ([signaler une vulnérabilité](https://github.com/MrFanghoDev/fletchapps/security/advisories/new))
- Ou par le contact indiqué sur le profil GitHub du mainteneur

Merci d'inclure : les étapes pour reproduire et l'impact potentiel tel
que tu le vois.

## À quoi s'attendre

Projet porté par un club, pas une entreprise avec une équipe sécurité
dédiée -- pas de délai de réponse garanti, mais chaque signalement sera
pris au sérieux.

---

# Security Policy

## Scope

FletchApps has **no server at all**: it's a purely static web page
(HTML/CSS, hosted on GitHub Pages), with no account and no user data.
The only dynamic logic is a script that queries the GitHub API
(`api.github.com`) to display each sibling project's version/status --
the result is inserted via `textContent` (never `innerHTML`), so there's
no realistic script-injection surface even if that response were ever
forged.

In scope:
- Any flaw that would allow injecting executable content into the page
  despite the above
- A drift in `theme.css`/`index.html` that would break
  `:focus-visible`/accessibility in a way that misleads the user (e.g. a
  hidden link pointing somewhere other than its visible text suggests)

Out of scope (expected behavior, not a vulnerability):
- Requests to `api.github.com` (loading statuses/versions) reveal the
  viewer's IP to GitHub -- inherent behavior of any third-party API
  call, not a leak specific to FletchApps
- FletchApps itself doesn't collect, receive, or transmit any personal
  data -- no server, no account, no telemetry

## Reporting a vulnerability

**Do not** open a public Issue for a security vulnerability until it's
fixed. Instead, contact the maintainer directly:

- Via the repository's **Security** tab
  ([report a vulnerability](https://github.com/MrFanghoDev/fletchapps/security/advisories/new))
- Or through the contact listed on the maintainer's GitHub profile

Please include: steps to reproduce, and the potential impact as you see
it.

## What to expect

This project is run by a club, not a company with a dedicated security
team -- no guaranteed response time, but every report will be taken
seriously.
