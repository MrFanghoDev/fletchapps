# Contribuer à FletchApps

*[English version below](#contributing-to-fletchapps)*

Merci de t'intéresser à FletchApps ! C'est un projet né d'un usage de
club (Les Aigles 77 / Archers Libres de Fontaine le Port), publié en
open source sous licence [GPL-3.0-or-later](LICENSE). On garde le
processus de contribution volontairement simple.

## Signaler un bug ou proposer une idée

Passe par les [Issues GitHub](https://github.com/MrFanghoDev/fletchapps/issues) --
pas besoin de formulaire compliqué. Pour un bug, ce qui aide le plus :
- Ce que tu as fait, ce que tu attendais, ce qui s'est passé à la place
- Ton navigateur/appareil et une capture d'écran si le souci est visuel

Pas besoin d'avoir déjà une solution en tête -- un problème bien décrit
suffit amplement.

## Proposer un changement de code

Le flux classique de l'open source, rien de plus :

1. **Fork** le dépôt, puis clone ton fork
2. Crée une branche (`git checkout -b ma-fonctionnalite`)
3. Fais tes changements
4. Vérifie-les dans un vrai navigateur (voir ci-dessous)
5. Ouvre une **Pull Request** vers `master`, en expliquant le *pourquoi* du
   changement, pas seulement le *quoi*

Pas besoin de discuter d'un petit changement à l'avance -- mais pour
quelque chose de plus structurant (ex. rendre les cartes de projet
pilotées par une config plutôt qu'écrites en dur, voir les Issues
ouvertes à ce sujet), ouvrir une Issue d'abord pour en discuter évite
de coder dans une direction qui ne conviendrait pas.

### Installation pour développer

Aucune installation ni build nécessaire (HTML/CSS pur, aucune
dépendance, pas de `npm install`) -- ouvre `index.html` dans un
navigateur, ou sers le dossier avec un petit serveur local :

```bash
git clone https://github.com/MrFanghoDev/fletchapps.git
cd fletchapps
python3 -m http.server 8080
# puis ouvrir http://localhost:8080/ dans un navigateur
```

### Style de code

Pas d'outil de formatage automatique -- reste cohérent avec le style
déjà en place dans `index.html`/`theme.css` (une carte de projet =
un bloc HTML complet, voir les cartes existantes comme modèle).

### Vérifier un changement

Pas de suite de tests automatisés -- un changement visuel doit être
vérifié en ouvrant réellement `index.html` dans un navigateur, pas
seulement relu. Pense à vérifier aussi :
- Les deux thèmes (clair/sombre) et le focus clavier (`:focus-visible`)
- Les liens vers les projets (bien à jour, pas de faute de frappe)
- Si tu touches `theme.css` : que la palette reste cohérente avec
  l'identité visuelle des autres projets Fletch (voir le
  [CLAUDE.md](CLAUDE.md) du dépôt)

### Pour aller plus loin

Le [CLAUDE.md](CLAUDE.md) du dépôt documente les quelques décisions
techniques déjà prises -- utile avant de se lancer dans un changement
conséquent.

## Le ton qu'on essaie de garder

Projet porté par un club, pas une entreprise -- pas de pression, pas
d'attente de réactivité instantanée. Sois patient·e avec les retours,
bienveillant·e dans les échanges, et n'hésite pas si quelque chose dans
cette doc (ou dans le code) n'est pas clair : c'est aussi un signal utile
pour l'améliorer. Voir aussi le [code de conduite](CODE_OF_CONDUCT.md).

---

# Contributing to FletchApps

Thanks for your interest in FletchApps! This project started from a
club's real-world use (Les Aigles 77 / Archers Libres de Fontaine le
Port), published open source under [GPL-3.0-or-later](LICENSE). The
contribution process is kept deliberately simple.

## Reporting a bug or suggesting an idea

Use [GitHub Issues](https://github.com/MrFanghoDev/fletchapps/issues) --
no complicated form needed. For a bug, what helps most:
- What you did, what you expected, what happened instead
- Your browser/device, and a screenshot if the issue is visual

You don't need a solution in mind already -- a well-described problem is
plenty.

## Proposing a code change

The classic open-source flow, nothing more:

1. **Fork** the repository, then clone your fork
2. Create a branch (`git checkout -b my-feature`)
3. Make your changes
4. Check them in a real browser (see below)
5. Open a **Pull Request** against `master`, explaining the *why* of the
   change, not just the *what*

No need to discuss a small change beforehand -- but for anything more
structural (e.g. driving the project cards from a config instead of
hardcoded HTML, see the open Issues on that topic), opening an Issue
first to discuss it avoids coding in a direction that might not fit.

### Setting up for development

No installation or build needed (plain HTML/CSS, no dependency, no
`npm install`) -- open `index.html` in a browser, or serve the folder
with a small local server:

```bash
git clone https://github.com/MrFanghoDev/fletchapps.git
cd fletchapps
python3 -m http.server 8080
# then open http://localhost:8080/ in a browser
```

### Code style

No automatic formatting tool -- stay consistent with the style already
in `index.html`/`theme.css` (a project card = one complete HTML block,
see existing cards as a template).

### Verifying a change

No automated test suite -- a visual change must be verified by actually
opening `index.html` in a browser, not just reviewed. Also worth
checking:
- Both themes (light/dark) and keyboard focus (`:focus-visible`)
- The links to each project (up to date, no typos)
- If you touch `theme.css`: that the palette stays consistent with the
  visual identity of the other Fletch projects (see the repository's
  [CLAUDE.md](CLAUDE.md))

### Going further

The repository's [CLAUDE.md](CLAUDE.md) documents the few technical
decisions already made -- worth a read before starting anything
substantial.

## The tone we're aiming for

This is a club-run project, not a company -- no pressure, no expectation of
instant responsiveness. Please be patient with feedback, kind in
discussions, and don't hesitate to flag if anything in this doc (or the
code) isn't clear: that's useful signal for improving it too. See also the
[Code of Conduct](CODE_OF_CONDUCT.md).
