# itou-theme — Skill Claude Code

Skill du design system **« Les Emplois de l'inclusion »** pour Claude Code. Permet a Claude de generer des interfaces et prototypes conformes au design system itou-theme (Bootstrap 5.3, police Marianne, composants BEM).

## Contenu du dossier

```
SKILL.md              — Documentation complete du design system (2700+ lignes)
stylesheets/app.css   — CSS compile du theme (inclut @font-face)
javascripts/app.js    — JavaScript du theme (tooltips, popovers, clipboard, etc.)
fonts/                — Marianne, Covered By Your Grace, Remix Icon
images/               — Logos des services, favicon, illustrations
modeles/              — 22 templates HTML de reference (pages auth et non-auth)
```

## Installation

1. **Copier le dossier** dans votre projet ou dans un emplacement accessible :

```bash
cp -r "Skill itou-theme" ~/mon-projet/.claude/skills/itou-theme
```

2. **Declarer le skill** dans la configuration Claude Code du projet (`.claude/settings.json`) :

```json
{
  "skills": [
    ".claude/skills/itou-theme/SKILL.md"
  ]
}
```

Alternativement, pour une installation globale (disponible dans tous les projets) :

```bash
cp -r "Skill itou-theme" ~/.claude/skills/itou-theme
```

Puis dans `~/.claude/settings.json` :

```json
{
  "skills": [
    "~/.claude/skills/itou-theme/SKILL.md"
  ]
}
```

## Utilisation

Une fois installe, Claude Code connait automatiquement le design system. Exemples de prompts :

- *« Genere une page de tableau de bord authentifie avec une liste de candidatures »*
- *« Cree un formulaire d'inscription en 3 etapes avec le stepper »*
- *« Ajoute un header authentifie avec la navigation pour le service emploi »*

Claude utilisera les bonnes classes CSS (`.s-header-authenticated`, `.c-stepper`, etc.), la structure BEM, et les conventions du design system.

## Prototypage rapide

Les assets fournis permettent de creer des prototypes fonctionnels. Claude peut generer des fichiers HTML autonomes qui referent aux CSS/JS/fonts inclus :

```html
<link rel="stylesheet" href="./stylesheets/app.css">
<script type="module" src="./javascripts/app.js"></script>
```

Les 22 templates dans `modeles/` servent de base pour les pages types (dashboard, formulaire, recherche, etc.).

> **Note** : les templates dans `modeles/` utilisent des chemins relatifs `./images/`, `./stylesheets/`, etc. Depuis le sous-dossier `modeles/`, ajustez les chemins en `../images/`, `../stylesheets/`, etc.

## Prerequis

- Claude Code (CLI, desktop ou web)
- Aucune dependance externe requise — tous les assets sont inclus
