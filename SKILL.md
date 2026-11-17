---
name: itou-theme
description: Skill du design system "Les Emplois de l'inclusion" — itou-theme base sur Bootstrap 5.3 avec la police Marianne, composants personnalises et conventions BEM.
---

# itou-theme — Design System des Emplois de l'inclusion

Design system de la plateforme **Les Emplois de l'inclusion** (les-emplois.inclusion.beta.gouv.fr), porte par le GIP Plateforme de l'inclusion.

**Base** : Bootstrap 5.3 — prefix CSS : `bs-` (`--bs-*` pour les CSS vars, `.bs-*` implicite dans les utilities).
**Convention** : classes Bootstrap standard + composants personnalises en BEM (`c-box`, `c-info`, etc.).
**Mode sombre** : desactive (`$enable-dark-mode: false`).
**Ombres** : activees (`$enable-shadows: true`).
**CSS Grid** : active (`$enable-cssgrid: true`).
**Marges negatives** : activees (`$enable-negative-margins: true`).
**Validation icons HTML natives** : desactivees.

**Source** : https://github.com/gip-inclusion/itou-theme
**Storybook** : https://gip-inclusion.github.io/itou-theme

---

## Typographie

Police principale : **Marianne** (police officielle de l'Etat francais).
Police decorative : **Covered By Your Grace** (annotations manuscrites, usage ponctuel uniquement).

| Famille SCSS | Stack |
|---|---|
| `$font-family-sans-serif` | `Marianne, Arial, sans-serif` |
| `$font-family-extra-01` | `Covered, Marianne, Arial, sans-serif` |
| `$font-family-monospace` | `SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace` |

### Poids disponibles

| Poids | Variable SCSS | Fichier |
|---|---|---|
| Light 300 | `$font-weight-lighter` / `$font-weight-light` | Marianne-Light.woff2 |
| Regular 400 | `$font-weight-normal` | Marianne-Regular.woff2 |
| Medium 500 | `$font-weight-medium` | Marianne-Medium.woff2 |
| Semi-bold 600 | `$font-weight-semibold` | Marianne-Bold.woff2 |
| Bold 700 | `$font-weight-bold` | Marianne-Bold.woff2 |
| ExtraBold 900 | `$font-weight-bolder` | Marianne-ExtraBold.woff2 |

Italiques disponibles pour 300, 400, 500.

### Echelle typographique

| Style | Taille | Poids | Line-height | Usage |
|---|---|---|---|---|
| h1-hero | 60px (48px mobile) | 700 | 1.2 | Titres hero, landing pages |
| h1 | 32px | 700 | 1.2 | Titres de page |
| h2 | 24px | 700 | 1.2 | Titres de section |
| h3 | 20px | 700 | 1.2 | Sous-titres, chapo |
| h4 | 18px | 700 | 1.2 | Titres de cartes |
| h5 | 16px | 700 | 1.2 | Titres mineurs |
| h6 | 16px | 700 | 1.2 | Plus petit niveau |
| body-lg | 18px | 400 | 1.6 | Paragraphes d'introduction |
| body | 16px | 400 | 1.6 | Corps de texte par defaut |
| body-sm / `.fs-sm` | 14px | 400 | 1.4 | Texte secondaire, legendes |
| body-xs / `.fs-xs` | 12px | 400 | 1.4 | Mentions legales, horodatages |
| body-bold | 16px | 700 | 1.6 | Emphase inline |
| accent (Covered) | 24px | 400 | 1.4 | Titres decoratifs manuscrits |

Line-heights : `$line-height-sm: 1.4`, `$line-height-base: 1.6`, `$line-height-lg: 1.8`.
Couleur titres : `$headings-color: $primary` (#000638) — les titres sont toujours en couleur primaire.

---

## Couleurs

### Couleurs principales

| Token | Hex | Usage |
|---|---|---|
| `primary` / `gray-900` | `#000638` | Encre texte, titres, elements structurels. NE JAMAIS utiliser #000 pur. |
| `secondary` / `gray-800` | `#333860` | Texte secondaire, sous-titres |
| `tertiary` | `#000091` | Bleu France — accent gouvernemental, etats actifs, liens hover, emphase |
| `white` | `#ffffff` | Fond de page, texte sur fonds fonces |
| `black` | `#383838` | Texte max contraste, icones |
| `light` / `gray-400` | `#f8f8f8` | Fond subtil |
| `dark` | `#383838` | Elements sombres, pied de page |

### Boutons

| Token | Hex |
|---|---|
| `button` | `#000091` (= tertiary) |
| `button-light` | `#2323ff` |
| `button-lighter` | `#daedff` |
| `button-lightest` | `#edf6ff` |

### Statuts — chaque statut a 4 niveaux : plein, light, lighter, lightest

| Statut | Plein | Light | Lighter | Lightest |
|---|---|---|---|---|
| `success` | `#18753c` | `#ceefdb` | `#e0f7e9` | `#f3fff8` |
| `warning` | `#b34000` | `#ffe7c0` | `#fff3df` | `#fffbf3` |
| `danger` | `#ce0500` | `#ffcfcd` | `#ffe1e0` | `#fff3f2` |
| `info` | `#0063cb` | `#dde4ff` | `#e8edff` | `#f6f8ff` |
| `important` | `#6c38d9` | `#cfbff5` | `#e9dffc` | `#f4f2ff` |

### Accents (decoration, illustrations)

| Token | Hex | Light | Lighter | Lightest |
|---|---|---|---|---|
| `accent-01` | `#f42ad4` (magenta) | `#fdcdf6` | `#fedff9` | `#fff1fd` |
| `accent-02` | `#8adcff` (bleu ciel) | `#d1f1ff` | `#e2f6ff` | `#ebf9ff` |
| `accent-03` | `#ffbe18` (or) | `#ffe8ad` | `#fff2cf` | `#fffdf9` |

### Sous-produits (couleurs identitaires)

| Token | Hex | Light | Lighter | Lightest |
|---|---|---|---|---|
| `emploi` | `#006adc` | `#cce1f8` | `#e5f0fb` | `#f2f8fd` |
| `marche` | `#fe5455` | `#ffdddd` | `#ffeeee` | `#fff6f6` |
| `communaute` | `#18a47d` | `#d1ede5` | `#e8f6f2` | `#f3faf8` |
| `pilotage` | `#ffad1d` | `#ffefd2` | `#fff7e8` | `#fff8ed` |

### Nuances (echelle gris-bleu) — privilegier cette echelle aux gris Bootstrap

| Token | Hex | Usage |
|---|---|---|
| `nuance-01` | `#1a1f4c` | Fonds sombres, pieds de page |
| `nuance-02` | `#333860` | Texte secondaire |
| `nuance-03` | `#4d5174` | Texte tertiaire |
| `nuance-04` | `#727492` | Placeholders, icones secondaires |
| `nuance-05` | `#999baf` | Bordures actives, separateurs |
| `nuance-06` | `#b3b4c3` | Desactive, bordures secondaires |
| `nuance-07` | `#cccdd7` | Bordures subtiles |
| `nuance-08` | `#e6e6eb` | Bordure par defaut, dividers, contours inputs |
| `nuance-09` | `#f2f3f5` | Lignes alternees, fonds tableaux |
| `nuance-10` | `#f8f8f8` | Fond subtil, blockquote |

### Utilitaires couleur

| Token | Hex | Usage |
|---|---|---|
| `blue` | `#0a76f6` | Focus ring, liens, elements interactifs |
| `disabled` / `nuance-06` | `#b3b4c3` | Elements desactives |
| `disabled-light` / `nuance-09` | `#f2f3f5` | Fond elements desactives |
| `muted` / `nuance-04` | `#727492` | Texte attenue |
| `border` / `nuance-08` | `#e6e6eb` | Bordure par defaut |
| `border-hover` / `nuance-07` | `#cccdd7` | Bordure survol |

### Echelle de gris Bootstrap (surcharges)

| Token | Hex |
|---|---|
| `gray-100` | `#eff1ff` |
| `gray-200` | `#cccccc` |
| `gray-300` | `#6a6a6a` |
| `gray-400` | `#f8f8f8` |
| `gray-500` | `#b2b4c4` |
| `gray-600` | `#999baf` |
| `gray-700` | `#80829c` |
| `gray-800` | `#333860` |
| `gray-900` | `#000638` |

---

## Espacement

Base : `$spacer: 1rem` (16px).

| Token | Valeur | Usage |
|---|---|---|
| `space-0` | 0 | — |
| `space-1` | 0.25rem (4px) | Ecart icone/texte, padding badge |
| `space-2` | 0.5rem (8px) | Gap inline, padding vertical input |
| `space-3` | 1rem (16px) | Gap par defaut, margin paragraphe, padding horizontal input |
| `space-4` | 1.5rem (24px) | Padding carte, gouttiere colonnes |
| `space-5` | 2rem (32px) | Padding conteneur, separation sections |
| `space-6` | 3rem (48px) | Marges entre blocs |
| `space-7` | 4rem (64px) | Espacement entre sections |
| `space-8` | 5rem (80px) | Padding hero |
| `space-9` | 6rem (96px) | Grand espacement |
| `space-10` | 8rem (128px) | Espacement maximum |

---

## Bordures et arrondis

| Token | Valeur | Usage |
|---|---|---|
| `border-width` | 1px | — |
| `border-color` | `nuance-08` (#e6e6eb) | Bordure par defaut |
| `border-color-hover` | `nuance-07` (#cccdd7) | Bordure survol |
| `radius-sm` | 2px (0.125rem) | Blockquote, pre/code |
| `radius` | 4px (0.25rem) | **Defaut** — inputs, boutons, cartes, alertes, badges |
| `radius-lg` | 8px (0.5rem) | Conteneurs proeminents, modales, boites (c-box) |
| `radius-xl` | 16px (1rem) | Elements decoratifs |
| `radius-pill` | 50rem | Tags arrondis, badges pill |

---

## Ombres

| Token | Valeur | Usage |
|---|---|---|
| `shadow-sm` | `0 3px 8px 0 rgba(0,6,56, 0.1)` | Cartes au repos |
| `shadow` | `0 3px 8px 0 rgba(0,6,56, 0.2)` | Cartes, dropdowns, popovers |
| `shadow-lg` | `0 3px 8px 0 rgba(0,6,56, 0.3)` | Modales, elements flottants |
| `shadow-xl` | `0 3px 16px 0 rgba(0,6,56, 0.2)` | Elements proeminents, tooltips |

---

## Grille et mise en page

Grille Bootstrap 12 colonnes, gouttiere 24px (1.5rem). Container padding-x : 32px (2rem).

| Breakpoint | Valeur | Container max-width |
|---|---|---|
| xs | 0 | — |
| sm | 560px | 560px |
| md | 768px | 768px |
| lg | 1024px | 1024px |
| xl | 1280px | 1280px |
| xxl | 1640px | 1640px |
| xxxl | 2220px | 2220px |

Contenu principal contraint a `max-width: 1280px` (xl) dans le corps de page.

---

## Icones

Le systeme utilise **Remix Icon** (police d'icones) chargee en vendor.
Syntaxe : `<i class="ri-{nom}-{style}" aria-hidden="true"></i>`

Styles : `line` (contour), `fill` (plein).
Tailles : `.ri-xs`, `.ri-sm`, `.ri-1x` (defaut dans btn), `.ri-lg`, `.ri-xl`, `.ri-xxl`.

Privilegier les icones Remix Icon pour la coherence avec le theme.

---

## Composants

### Button `.btn`

Base Bootstrap 5.3 avec personnalisations.

**Variantes** :
- `.btn-primary` — fond primary (#000638), texte blanc
- `.btn-outline-primary` — bordure primary, texte primary
- `.btn-secondary` — fond secondary
- `.btn-success`, `.btn-danger` — statuts
- `.btn-link` — couleur `button` (#000091), bold, pas de decoration, hover = `button-light`
- `.btn-white` — fond blanc, texte `button`, hover = fond `disabled-light`
- `.btn-outline-white` — bordure blanche
- `.btn-link-white` — texte blanc, pour fonds colores (c-box--action)

**Tailles** : `.btn-sm` (32px), defaut (40px), `.btn-lg` (48px), `.btn-xl` (56px)
**Largeur** : `.btn-block` = width 100%

**Avec icone** :
```html
<button class="btn btn-primary btn-ico" type="button">
  <i class="ri-zoom-in-line fw-medium" aria-hidden="true"></i>
  <span>Rechercher</span>
</button>
```

**Icone seule** (obligatoire : `aria-label`) :
```html
<button class="btn btn-primary btn-ico-only" type="button" aria-label="Fermer">
  <i class="ri-close-line fw-medium" aria-hidden="true"></i>
</button>
```

**Desactive** : attribut `disabled` sur `<button>`, `.disabled` sur `<a>`. Opacity = 1 (pas de transparence, couleurs changees).

**Bouton partenaire** :
```html
<a href="" target="_blank" class="btn btn-partner btn-partner--diagoriente">
  Creer un CV avec Diagoriente
</a>
```

**Groupe de boutons actions** :
```html
<div class="btn-group-action">
  <button class="btn btn-primary btn-sm">Action 1</button>
  <button class="btn btn-outline-primary btn-sm">Action 2</button>
</div>
```

**Filtre dropdown** :
```html
<div class="btn-dropdown-filter-group">
  <button class="btn btn-dropdown-filter dropdown-toggle" data-bs-toggle="dropdown">
    Filtre 1
  </button>
  <button class="btn btn-dropdown-filter has-selected-item dropdown-toggle" data-bs-toggle="dropdown">
    Filtre 2 (actif)
  </button>
</div>
```

---

### Alert `.alert`

Basee sur Bootstrap alerts avec variantes supplementaires.

**Variantes** : `.alert-info`, `.alert-success`, `.alert-warning`, `.alert-danger`, `.alert-important`

```html
<div class="alert alert-info" role="status">
  <div class="alert-heading">
    <strong>Information</strong>
  </div>
  <p>Message detaille ici.</p>
</div>
```

**Avec icone, bouton et fermeture** :
```html
<div class="alert alert-warning alert-dismissible" role="status">
  <i class="ri-alert-line" aria-hidden="true"></i>
  <div>
    <strong>Attention</strong>
    <p>Description du message.</p>
    <a href="#" class="btn btn-sm btn-warning btn-ico">
      <i class="ri-arrow-right-line" aria-hidden="true"></i>
      <span>Action</span>
    </a>
  </div>
  <button type="button" class="btn-close" data-bs-dismiss="alert" aria-label="Fermer"></button>
</div>
```

**Fermeture memorisee** : `.alert-dismissible-once` + `id` unique — le JS du theme memorise dans localStorage.

**Roles ARIA** : `role="status"` pour info, `role="alert"` pour erreurs critiques.

---

### Global Alert `.alert` (en-tete de page)

Alertes positionnees en haut de page, generalement au-dessus de l'en-tete.

```html
<div class="alert alert-info mb-0 rounded-0 text-center" role="status">
  <strong>Message global</strong> — Visible sur toute la plateforme.
  <button type="button" class="btn-close" data-bs-dismiss="alert" aria-label="Fermer"></button>
</div>
```

---

### Badge `.badge`

Badges Bootstrap avec tailles personnalisees. `display: inline-flex`, `align-items: center`, `gap: space-1`.

**Tailles** :

| Classe | Description |
|---|---|
| `.badge` | Taille heritee du parent |
| `.badge-xl` | Extra-large (font-size-lg, padding double) |
| `.badge-base` | Standard (font-size-base) |
| `.badge-sm` | Petite (font-size-sm) |
| `.badge-xs` | Extra-petite (font-size-xs, font-weight normal) |

**Couleurs** : `.bg-primary`, `.bg-success`, `.bg-warning`, `.bg-danger`, `.bg-info`, `.bg-important`, `.bg-accent-01/02/03`, plus variantes `-lighter`/`-lightest`. Texte : `.text-white` pour fonds pleins, `.text-{status}` pour fonds clairs, `.text-primary` pour accent-02/03.

```html
<span class="badge badge-base rounded-pill bg-primary text-white">Nouveau</span>
<span class="badge badge-xs rounded-pill bg-success text-white">EI</span>
<span class="badge badge-sm rounded-pill bg-success-lighter text-success">
  <i class="ri-check-line" aria-hidden="true"></i> Eligible
</span>
```

**Badge circulaire** (compteur) :
```html
<span class="badge badge-xl rounded-circle bg-tertiary text-white">5</span>
```

**Badge comme declencheur dropdown** (taille `.badge-base` uniquement) :
```html
<button type="button" class="badge badge-base rounded-pill bg-info dropdown-toggle" data-bs-toggle="dropdown" aria-expanded="false">
  Prise de contact
</button>
<ul class="dropdown-menu">
  <li><button type="button" class="dropdown-item">Action</button></li>
</ul>
```

**Badge avec texte secondaire** :
```html
<span class="badge badge-base rounded-pill bg-important text-white">
  Nouveau <small>Expire le 12/08/26</small>
</span>
```

**Groupe de badges** `.badge-group` :
```html
<div class="badge-group">
  <span class="badge badge-xs rounded-pill bg-accent-02-light text-primary">CDI</span>
  <span class="badge badge-xs rounded-pill bg-accent-02-light text-primary">26h/semaine</span>
</div>
```

---

### Tag `.tag`

Composant personnalise pour indiquer un statut. Texte majuscule, petite taille.

```html
<span class="tag bg-info-lighter text-info">Prescripteur</span>
<a href="#" class="tag bg-important-lighter text-important">Cliquable</a>
<span class="tag tag-lg bg-accent-01-lighter text-accent-01">Grand</span>
```

**Avec icone** :
```html
<span class="tag bg-info-lighter text-info">
  <i class="ri-check-line ri-xs" aria-hidden="true"></i>Valide
</span>
```

**Groupe de tags** :
```html
<div class="tag-group">
  <span class="tag bg-nuance-09 text-primary">Tag 1</span>
  <span class="tag bg-nuance-09 text-primary">Tag 2</span>
</div>
```

Style : `display: inline-block`, `height: 20px` (24px pour `tag-lg`), `font-size: 12px` (14px pour `tag-lg`), `border-radius: badge-border-radius`, `font-weight: normal`.

---

### Box `.c-box`

Conteneur generique avec bordure et border-radius. Composant BEM personnalise.

```html
<div class="c-box">
  <h3>Titre</h3>
  <p>Contenu...</p>
</div>
```

Style : `background: white`, `border: 1px solid nuance-08`, `border-radius: 8px (radius-lg)`, `padding: 16px` (24px a partir de md).

**Variante lien unique** (hover change la bordure) :
```html
<div class="c-box has-one-link-inside">...</div>
```

**Variante multi-liens** :
```html
<div class="c-box has-links-inside">...</div>
```

#### Box Action `.c-box--action`

Barre d'actions sur fond `button` (#000091). Utilisee en haut de page pour les actions principales.

```html
<div class="c-box c-box--action">
  <h2 class="visually-hidden">Actions rapides</h2>
  <div class="form-row align-items-center gx-3">
    <div class="form-group col-12 col-lg-auto">
      <a href="#" class="btn btn-lg btn-white btn-block btn-ico">
        <i class="ri-check-line fw-medium" aria-hidden="true"></i>
        <span>Accepter</span>
      </a>
    </div>
    <div class="form-group col-12 col-lg-auto">
      <a href="#" class="btn btn-lg btn-outline-white btn-block btn-ico">
        <i class="ri-close-line fw-medium" aria-hidden="true"></i>
        <span>Decliner</span>
      </a>
    </div>
  </div>
</div>
```

#### Box Results `.c-box--results`

Carte de resultats de recherche avec en-tete/corps/pied.

```html
<div class="c-box c-box--results">
  <div class="c-box--results__header">
    <div class="c-box--results__summary">
      <i class="ri-building-line" aria-hidden="true"></i>
      <div><span class="badge badge-xs rounded-pill bg-primary">EI</span></div>
      <h3><a href="#">Nom de la structure</a></h3>
    </div>
  </div>
  <div class="c-box--results__body">
    <p>Description...</p>
  </div>
  <div class="c-box--results__footer">
    <a href="#" class="btn btn-sm btn-primary btn-ico">
      <i class="ri-arrow-right-line" aria-hidden="true"></i>
      <span>Voir le detail</span>
    </a>
  </div>
</div>
```

#### Box Organization `.c-box--organization`

Carte d'organisation avec icone et grid layout.

```html
<div class="c-box">
  <div class="c-box--organization__summary">
    <i class="ri-building-line" aria-hidden="true"></i>
    <div><span class="badge badge-xs rounded-pill bg-primary">ACI</span></div>
    <h3>Nom de l'organisation</h3>
  </div>
  <ul class="c-box--organization__list-contact">
    <li><i class="ri-phone-line ri-sm me-1" aria-hidden="true"></i> 01 23 45 67 89</li>
    <li><i class="ri-mail-line ri-sm me-1" aria-hidden="true"></i> contact@org.fr</li>
  </ul>
</div>
```

#### Box Summary `.c-box--summary`

Bloc recapitulatif avec en-tete (titre + statut), corps (liste de donnees ou texte), pied d'actions optionnel.

```html
<div class="c-box c-box--summary has-links-inside">
  <div class="c-box--summary__header">
    <div class="d-flex flex-column flex-lg-row gap-2 gap-lg-3">
      <div class="flex-grow-1">
        <h3 class="m-0">Documents</h3>
      </div>
      <div>
        <span class="badge badge-sm rounded-pill bg-accent-03 text-primary">A controler</span>
      </div>
    </div>
  </div>
  <hr class="m-0">
  <div class="c-box--summary__body">
    <div class="c-box--summary__list-data">
      <ul class="list-unstyled">
        <li class="d-flex gap-2">
          <span class="flex-grow-1">Label</span>
          <strong>Valeur</strong>
        </li>
      </ul>
    </div>
  </div>
  <div class="c-box--summary__footer">
    <div class="d-flex justify-content-end">
      <a class="btn btn-primary btn-block w-100 w-md-auto" href="#">Controler</a>
    </div>
  </div>
</div>
```

Cas d'usage : documents telecheargeables, recapitulatif chiffre, commentaire avec action modifier.

#### Box Dashboard `.c-box--dashboard`

Bloc d'actions et suivi en contexte dashboard. Entete avec titre/badge, corps avec liste de liens, pied optionnel.

```html
<div class="c-box c-box--dashboard">
  <div class="d-flex align-items-center justify-content-between mb-3">
    <h3 class="mb-0">Candidatures</h3>
    <a href="" class="btn btn-sm btn-outline-primary btn-ico">
      <i class="ri-eye-line fw-normal" aria-hidden="true"></i>
      <span>Voir toutes les candidatures</span>
    </a>
  </div>
  <ul class="list-group list-group-flush list-group-link mb-3">
    <li class="list-group-item list-group-item-action d-flex justify-content-between align-items-center">
      <a href="" class="stretched-link text-decoration-none text-primary fw-bold">A traiter</a>
      <span class="badge rounded-pill badge-xs bg-info-light text-info">3</span>
    </li>
    <li class="list-group-item list-group-item-action d-flex justify-content-between align-items-center">
      <a href="" class="stretched-link text-decoration-none">En attente</a>
      <span class="badge rounded-pill badge-xs bg-nuance-09 text-primary">12</span>
    </li>
  </ul>
</div>
```

#### Box PASS `.c-box--pass`

Carte PASS IAE avec statut, donnees cles et actions.

```html
<div class="c-box c-box--pass">
  <div class="mb-3 mb-md-4">
    <span class="badge badge-base rounded-pill bg-success-lighter text-success">
      <i class="ri-pass-valid-line" aria-hidden="true"></i>
      PASS IAE valide
    </span>
  </div>
  <ul class="list-data mb-3 mb-md-4">
    <li>
      <small>Numero de PASS IAE</small>
      <strong>99999 99 99999</strong>
    </li>
    <li>
      <small>Date de debut</small>
      <strong>05/07/2024</strong>
    </li>
    <li>
      <small>Date de fin previsionnelle</small>
      <strong>04/07/2026</strong>
    </li>
  </ul>
  <a href="" class="btn btn-outline-primary btn-block btn-ico">
    <i class="ri-pass-valid-line fw-normal" aria-hidden="true"></i>
    <span>Afficher le PASS IAE</span>
  </a>
</div>
```

#### Box Sidebar

Boxes dans la sidebar de contenu (colonne droite). Titre `<h3>` obligatoire. Variantes colorees possibles.

```html
<!-- Box sidebar standard -->
<div class="c-box mb-3 mb-md-4">
  <h3>Coordonnees</h3>
  <div class="d-flex text-secondary fs-sm">
    <i class="ri-map-pin-2-line me-2" aria-hidden="true"></i>
    <address class="m-0">123 rue Example, 75001 Paris</address>
  </div>
</div>

<!-- Box sidebar coloree -->
<div class="c-box bg-info-lightest border-info-light mb-3 mb-md-4">
  <h3>Information</h3>
  <p>Contenu informatif.</p>
</div>

<!-- Box sidebar warning -->
<div class="c-box bg-warning-lightest border-warning-light mb-3 mb-md-4">
  <h3>A faire</h3>
  <p>Action requise.</p>
</div>
```

#### Box Partenaire `.c-box--promo-partenaire`

Carte promotionnelle pour un service partenaire. Layout en 2 colonnes : texte + illustration.

```html
<div class="c-box c-box--promo-partenaire">
  <div class="row g-0">
    <div class="col-12 col-md pe-3 pe-md-4 py-3 py-md-4">
      <h3 class="text-tertiary">Titre partenaire</h3>
      <p><strong>Accroche</strong></p>
      <p class="fs-sm mb-4">Description du service.</p>
      <a href="#" target="_blank" class="btn btn-block w-100 w-md-auto btn-outline-primary has-external-link">
        Action
      </a>
    </div>
    <div class="d-none d-md-inline-flex col-md-auto align-self-end">
      <img src="illustration.png" class="img-fluid" alt="" aria-hidden="true">
    </div>
  </div>
</div>
```

#### Box Note `.c-box--note`

Zone de notes avec textarea et boutons d'action.

---

### Info `.c-info`

Bloc informatif collapsible avec fond bleu clair.

```html
<div class="c-info">
  <button class="c-info__summary" data-bs-toggle="collapse" data-bs-target="#info-detail" aria-expanded="false">
    <span>Titre de l'information</span>
  </button>
  <div class="collapse" id="info-detail">
    <div class="c-info__detail">
      <p>Contenu detaille...</p>
    </div>
  </div>
</div>
```

**Non collapsible** :
```html
<div class="c-info">
  <div class="c-info__summary">
    <span>Information importante</span>
  </div>
  <div class="c-info__detail">
    <p>Details...</p>
  </div>
</div>
```

**Sans bordure** : `.c-info--borderless`

Style : `background: info-lightest`, `border: 1px solid info-light`, `border-radius: 4px`. Icone info automatique via `::before`.

---

### Card `.card` / `.c-card`

Cartes Bootstrap standard avec surcharges du theme. Transition sur `border-color`. En-tetes et pieds : fond transparent, sans bordure.

```html
<div class="card">
  <img src="image.png" class="card-img-top" alt="Description">
  <div class="card-body">
    <h5 class="card-title">Titre</h5>
    <p class="card-text">Contenu.</p>
  </div>
  <div class="card-footer">
    <a href="#" class="btn btn-sm btn-primary">Voir le detail</a>
  </div>
</div>
```

**Grille de cartes** :
```html
<div class="row row-cols-1 row-cols-md-2 row-cols-xxl-3 mt-3 mt-md-4">
  <div class="col mb-3 mb-md-4">
    <div class="card h-100">...</div>
  </div>
</div>
```

**Carte avec lien unique** `.c-card.has-one-link-inside` — hover = bordure `button-light` (#2323ff) :
```html
<div class="card c-card has-one-link-inside h-100">
  <div class="card-header">
    <img src="logo.svg" height="53" alt="Nom du service">
  </div>
  <div class="card-body">
    <p>Description du service.</p>
  </div>
  <div class="card-footer text-end">
    <a href="#" class="btn btn-sm btn-ico btn-link stretched-link">
      <span>Voir le service</span>
      <i class="ri-arrow-right-up-line ri-lg" aria-hidden="true"></i>
    </a>
  </div>
</div>
```

**Carte multi-liens** `.c-card.has-links-inside` — hover = bordure `border-color-hover`.

**Carte avec header grid** `.card-header__summary` — grille 2 colonnes (icone + texte). Support collapse via `data-bs-toggle="collapse"`.

**Carte radio enrichie** `.has-rich-radio` — header passe en fond `button-lightest` quand le radio est coche.

---

### Table `.table`

Tables Bootstrap avec surcharges : `vertical-align: middle`, `th: font-weight medium (500)`, lignes alternees sur `gray-400`.

```html
<table class="table">
  <caption>Liste des candidats</caption>
  <thead>
    <tr>
      <th scope="col">Nom</th>
      <th scope="col">Statut</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Dupont Jean</th>
      <td><span class="badge rounded-pill bg-success">Actif</span></td>
    </tr>
  </tbody>
</table>
```

**Variantes** : `.table-sm` (compact), `.table-striped` (zebre), `.table-hover` (survol), `.table-bordered` (bordures).
**Responsive** : enrober dans `<div class="table-responsive">` ou `.table-responsive-{breakpoint}`.
**Triable** : `.table-sortable` + `aria-sort` sur les `<th>` avec boutons de tri :
```html
<table class="table table-hover table-sortable">
  <thead>
    <tr>
      <th aria-sort="descending"><button type="button">Colonne triee</button></th>
      <th aria-sort="none"><button type="button">Autre colonne</button></th>
    </tr>
  </thead>
</table>
```

**Table avec selection** (checkboxes + actions inline) — patron courant pour les listes de candidatures :
```html
<table class="table table-hover table-sortable">
  <thead>
    <tr>
      <th class="text-start w-50px">
        <input class="form-check-input" type="checkbox" id="select-all">
        <label class="visually-hidden" for="select-all">Tout selectionner</label>
      </th>
      <th scope="col" aria-sort="none"><button type="button">Nom</button></th>
      <th scope="col">Statut</th>
      <th scope="col" class="text-end w-50px"><span class="visually-hidden">Actions</span></th>
    </tr>
  </thead>
  <tbody>
    <tr class="align-top">
      <th scope="row" class="text-start w-50px">
        <input class="form-check-input" type="checkbox" name="selected" value="id">
      </th>
      <td><a class="btn-link" href="#">Nom</a></td>
      <td><span class="badge badge-sm rounded-pill bg-success">Acceptee</span></td>
      <td class="text-end w-50px">
        <a class="btn btn-sm btn-secondary btn-ico-only" href="" data-bs-toggle="tooltip" data-bs-title="Voir">
          <i class="ri-arrow-drop-right-line fs-lg" aria-hidden="true"></i>
        </a>
      </td>
    </tr>
  </tbody>
</table>
```

---

### Tabs `.nav-tabs`

Onglets Bootstrap personnalises : pas de bordure, indicateur via `border-bottom` sur l'onglet actif, couleur active = `button`.

```html
<ul class="nav nav-tabs" role="tablist">
  <li class="nav-item" role="presentation">
    <button class="nav-link active" data-bs-toggle="tab" data-bs-target="#tab1" role="tab" aria-selected="true">
      Onglet 1
    </button>
  </li>
  <li class="nav-item" role="presentation">
    <button class="nav-link" data-bs-toggle="tab" data-bs-target="#tab2" role="tab" aria-selected="false">
      Onglet 2
    </button>
  </li>
</ul>
<div class="tab-content">
  <div class="tab-pane fade show active" id="tab1" role="tabpanel">Contenu 1</div>
  <div class="tab-pane fade" id="tab2" role="tabpanel">Contenu 2</div>
</div>
```

---

### Accordion `.accordion`

Bootstrap accordion standard. Chaque item = bouton declencheur + panneau collapsible.

```html
<div class="accordion" id="myAccordion">
  <div class="accordion-item">
    <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapse1" aria-expanded="false" aria-controls="collapse1">
      Titre de l'element
    </button>
    <div id="collapse1" class="accordion-collapse collapse" data-bs-parent="#myAccordion">
      <div class="accordion-body">Contenu...</div>
    </div>
  </div>
</div>
```

**Variantes** :
- `.accordion-flush` — sans bordures ni coins arrondis (bord a bord)
- Omettre `data-bs-parent` pour permettre plusieurs elements ouverts simultanement

---

### Modal `.modal`

Bootstrap modal. Z-index modal : 3050, backdrop : 3040 (eleves par rapport au defaut Bootstrap).

```html
<button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#myModal">
  Ouvrir
</button>
<div class="modal fade" id="myModal" tabindex="-1" aria-labelledby="myModalLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h1 class="modal-title fs-5" id="myModalLabel">Titre</h1>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Fermer"></button>
      </div>
      <div class="modal-body">Contenu...</div>
      <div class="modal-footer">
        <button type="button" class="btn btn-outline-primary" data-bs-dismiss="modal">Annuler</button>
        <button type="button" class="btn btn-primary">Confirmer</button>
      </div>
    </div>
  </div>
</div>
```

---

### Toast `.toast`

Bootstrap toast avec variantes itou. Z-index : 1070.

**Variantes** : `.toast--info`, `.toast--warning`, `.toast--danger`, `.toast--success`

```html
<div class="toast-container position-fixed top-0 end-0 p-3">
  <div class="toast toast--success" role="status" aria-live="polite" aria-atomic="true">
    <div class="toast-header">
      <strong class="me-auto">Succes</strong>
      <button type="button" class="btn-close" data-bs-dismiss="toast" aria-label="Fermer"></button>
    </div>
    <div class="toast-body">Operation reussie.</div>
  </div>
</div>
```

ARIA : `role="status" aria-live="polite"` pour messages non critiques, `role="alert" aria-live="assertive"` pour messages importants.

---

### Tooltip `.tooltip` et Popover `.popover`

Bootstrap standard. Z-index tooltip : 1050, popover : 1055. Initialisation JS requise.

```html
<!-- Tooltip -->
<button type="button" class="btn btn-outline-primary" data-bs-toggle="tooltip" data-bs-title="Texte d'aide">
  Hover moi
</button>

<!-- Tooltip sur icone (accessible) -->
<i class="ri-information-line ri-xl text-info" aria-label="Information complementaire" data-bs-toggle="tooltip" data-bs-title="Explication" role="button" tabindex="0"></i>

<!-- Tooltip sur element disabled (wrapper focusable) -->
<span tabindex="0" data-bs-toggle="tooltip" data-bs-title="Indisponible">
  <button class="btn btn-primary" disabled>Desactive</button>
</span>

<!-- Popover -->
<button type="button" class="btn btn-outline-primary" data-bs-toggle="popover" data-bs-title="Titre" data-bs-content="Contenu detaille.">
  Popover
</button>
```

---

### Spinner `.spinner-border`

Bootstrap spinner avec utilitaire itou `.has-spinner-loading`.

**Spinner simple** :
```html
<div class="spinner-border text-tertiary" role="status">
  <span class="visually-hidden">Chargement...</span>
</div>
```

**Overlay de chargement sur un conteneur** : `.has-spinner-loading` masque le contenu et affiche un spinner centre.
```html
<div class="card has-spinner-loading" role="status">
  <div class="card-body">Contenu en cours de mise a jour.</div>
</div>
```

**Spinner dans un bouton** :
```html
<button class="btn btn-primary" type="button" disabled>
  <span class="loading-text">
    <span class="spinner-border spinner-border-sm" aria-hidden="true"></span>
    Chargement...
  </span>
  <span class="stable-text">Envoyer</span>
</button>
```

---

### Dropdown `.dropdown`

Dropdown Bootstrap avec surcharges : pas de bordure, shadow-sm, padding 0, liens hover = tertiary sur fond clair.

```html
<div class="dropdown">
  <button class="btn btn-primary dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
    Menu
  </button>
  <div class="dropdown-menu">
    <a class="dropdown-item active" href="#">Option active</a>
    <a class="dropdown-item" href="#">Option 2</a>
    <div class="dropdown-divider"></div>
    <h6 class="dropdown-header">Section</h6>
    <a class="dropdown-item" href="#">Option 3</a>
  </div>
</div>
```

**Variante organisation** `.dropdown-organization` : liste de structures avec badges dans un dropdown.

---

### Breadcrumb `.breadcrumb`

Bootstrap breadcrumb standard.

```html
<nav aria-label="Fil d'Ariane">
  <ol class="breadcrumb">
    <li class="breadcrumb-item"><a href="#">Accueil</a></li>
    <li class="breadcrumb-item"><a href="#">Section</a></li>
    <li class="breadcrumb-item active" aria-current="page">Page courante</li>
  </ol>
</nav>
```

---

### Collapse `.collapse`

Bootstrap collapse. Le theme ajoute `.has-collapse-caret` pour afficher un chevron qui change d'etat selon `aria-expanded`.

```html
<button type="button" class="btn btn-outline-primary fw-bold has-collapse-caret" data-bs-toggle="collapse" data-bs-target="#collapseContent" aria-expanded="false" aria-controls="collapseContent">
  Afficher / Masquer
</button>
<div class="collapse mt-3" id="collapseContent">
  <p>Contenu repliable...</p>
</div>
```

Le chevron peut etre place a droite avec `d-flex justify-content-between` sur le bouton.

---

### Title `.c-title`

Grille de titre de page avec zone principale, CTA et zone secondaire.

```html
<div class="c-title">
  <div class="c-title__main">
    <h1>Titre de la page</h1>
    <p class="text-muted">Sous-titre ou description</p>
  </div>
  <div class="c-title__cta">
    <a href="#" class="btn btn-primary btn-ico">
      <i class="ri-add-line fw-medium" aria-hidden="true"></i>
      <span>Action principale</span>
    </a>
  </div>
  <div class="c-title__secondary">
    <div class="tag-group">
      <span class="tag bg-info-lighter text-info">Tag info</span>
    </div>
  </div>
</div>
```

Layout : 1 colonne mobile, 2 colonnes (1fr auto) a partir de lg. Grid areas : `main`, `cta`, `secondary`.

---

### Stepper `.c-stepper`

Conteneur de progression par etapes.

```html
<div class="c-stepper">
  <p><strong>Etape 2 sur 4</strong></p>
  <div class="progress" style="height: 8px;">
    <div class="progress-bar bg-tertiary" role="progressbar" style="width: 50%;" aria-valuenow="50" aria-valuemin="0" aria-valuemax="100"></div>
  </div>
  <p class="mt-2"><strong>Informations personnelles</strong></p>
</div>
```

Style : meme que c-box (fond blanc, bordure, radius-lg).

---

### List Data `.list-data`

Liste de paires label/valeur responsive (container query a 560px).

```html
<ul class="list-data">
  <li>
    <small>Date de naissance</small>
    <strong>05/11/1997</strong>
  </li>
  <li>
    <small>Ville</small>
    <strong>Paris</strong>
  </li>
  <li class="has-forced-line-break">
    <small>Adresse complete</small>
    <strong>123 rue de la Paix, 75001 Paris</strong>
  </li>
</ul>
```

**Groupe** : `.list-data-group` = flex column, row a partir de xl.

---

### List Step `.list-step`

Timeline verticale avec bordure gauche.

```html
<ul class="list-step">
  <li>
    <time>12/11/2024</time>
    <span>Candidature envoyee</span>
  </li>
  <li>
    <time>10/11/2024</time>
    <span>Dossier cree</span>
  </li>
</ul>
```

Le premier element a une bordure `info` (#0063cb) et texte bold.

---

### List Note `.list-note`

Liste de notes/commentaires avec avatar icone.

```html
<ul class="list-note">
  <li class="is-current-user">
    <i class="ri-user-line" aria-hidden="true"></i>
    <div>
      <time>12/11/2024 a 14h30</time>
      <strong>Jean Dupont</strong>
    </div>
    <blockquote>Contenu de la note...</blockquote>
  </li>
</ul>
```

---

### List Ordered `.list-ordered`

Liste numerotee avec pastilles tertiary (#000091).

```html
<ol class="list-ordered">
  <li><span>Creer votre compte</span></li>
  <li><span>Renseigner vos informations</span></li>
  <li><span>Valider votre inscription</span></li>
</ol>
```

Pastilles : cercle 24px, fond tertiary, texte blanc, font-size sm, bold.

---

### List Group `.list-group`

Bootstrap list-group avec variantes itou.

```html
<ul class="list-group">
  <li class="list-group-item">Element 1</li>
  <li class="list-group-item active" aria-current="true">Element actif</li>
  <li class="list-group-item disabled" aria-disabled="true">Element desactive</li>
</ul>
```

**Variantes itou** :
- `.list-group-sm` : padding reduit (compact)
- `.list-group-flush` : sans bordures externes
- `.list-group-link` : items actionnables avec chevron droit automatique et lien stretche
- `.list-group-collapse` : items avec sous-contenu repliable (collapse integre)
- `.list-group-form` : rendu proche des champs de formulaire

---

## Formulaires

### Conteneur formulaire `.c-form`

Le composant `.c-form` structure un formulaire complet avec styles descendants pour les controles.

```html
<div class="c-form">
  <form>
    <fieldset>
      <legend>Informations generales</legend>
      <div class="form-group form-group-required form-group-input-w-lg-50">
        <label class="form-label" for="id_brand">Nom</label>
        <input type="text" class="form-control" required id="id_brand" aria-describedby="id_brand_help">
        <div id="id_brand_help" class="form-text">Texte d'aide.</div>
      </div>
      <div class="form-group form-group-input-w-lg-33">
        <label class="form-label" for="id_code">Code postal</label>
        <input type="text" class="form-control" maxlength="5" id="id_code">
      </div>
    </fieldset>
    <hr class="my-3">
    <div class="d-flex justify-content-end gap-3">
      <button type="reset" class="btn btn-outline-primary">Reinitialiser</button>
      <button type="submit" class="btn btn-primary">Enregistrer</button>
    </div>
  </form>
</div>
```

**Classes de largeur responsive** : `.form-group-input-w-lg-25`, `.form-group-input-w-lg-33`, `.form-group-input-w-lg-50`, `.form-group-input-w-lg-66` — adaptent la largeur du champ a son contenu attendu (a partir de lg).

**Champ requis** : `.form-group-required` ajoute un indicateur visuel.

### Input / Select / Textarea

Formulaires Bootstrap standard. Hauteurs fixes : sm=32px, defaut=40px, lg=48px, xl=56px.
Labels en bold (`$form-label-font-weight: 700`).
Bordure input = `secondary` (#333860). Focus = `gray-900`.
Placeholder = `muted-color`.

```html
<div class="form-group mb-3">
  <label for="inputNom" class="form-label">Nom <span class="text-danger">*</span></label>
  <input type="text" class="form-control" id="inputNom" required>
</div>

<div class="form-group mb-3">
  <label for="selectType" class="form-label">Type</label>
  <select class="form-select" id="selectType">
    <option selected>Choisir...</option>
    <option value="1">Option 1</option>
  </select>
</div>

<div class="form-group mb-3">
  <label for="textareaDesc" class="form-label">Description</label>
  <textarea class="form-control" id="textareaDesc" rows="3"></textarea>
</div>
```

**Tailles** : `.form-control-sm`, `.form-control-lg`, `.form-control-xl` / `.form-select-sm`, etc.

**Textarea auto-extensible** : `data-it-expandable="true"` sur le `<textarea>`.

### Checkbox `.form-check`

```html
<div class="form-check">
  <input class="form-check-input" type="checkbox" id="check1">
  <label class="form-check-label" for="check1">Option A</label>
</div>
```

Checkbox coche : fond `button-light` (#2323ff).

### Radio `.form-check`

```html
<div class="form-check">
  <input class="form-check-input" type="radio" name="radioGroup" id="radio1">
  <label class="form-check-label" for="radio1">Option A</label>
</div>
```

### Switch `.form-switch`

```html
<div class="form-check form-switch">
  <input class="form-check-input" type="checkbox" role="switch" id="switch1">
  <label class="form-check-label" for="switch1">Activer</label>
</div>
```

**Grande taille** : `.form-switch-lg`
**Reverse** : `.form-check-reverse` place le switch a droite du label.
**Label d'etat dynamique** : `.has-state-label` + attributs `data-it-state-label-off` / `data-it-state-label-on` sur le `<label>`.

```html
<div class="form-check form-switch form-switch-lg has-state-label">
  <input class="form-check-input" type="checkbox" role="switch" id="switch2">
  <label class="form-check-label" for="switch2" data-it-state-label-off="Desactive" data-it-state-label-on="Active">
    <span class="visually-hidden">Notifications</span>
  </label>
</div>
```

### Button Group `.btn-group`

Regroupement de boutons. Variante itou `.btn-group-action` pour actions rapides (icones seules).

```html
<div class="btn-group" role="group" aria-label="Actions">
  <a href="#" class="btn btn-primary active" aria-current="page">Lien actif</a>
  <a href="#" class="btn btn-primary">Lien</a>
</div>
```

**Actions rapides** :
```html
<div class="btn-group-action" role="group" aria-label="Actions rapides">
  <a class="btn btn-link btn-ico-only" href="" data-bs-toggle="tooltip" data-bs-title="Postuler">
    <i class="ri-draft-line" aria-label="Postuler"></i>
  </a>
  <button class="btn btn-link btn-ico-only" type="button" data-bs-toggle="dropdown" aria-label="Plus d'actions">
    <i class="ri-more-2-fill" aria-hidden="true"></i>
  </button>
</div>
```

### Input Group `.input-group`

Bootstrap input-group. Addon bg = transparent.

```html
<div class="input-group">
  <span class="input-group-text"><i class="ri-search-line" aria-hidden="true"></i></span>
  <input type="text" class="form-control" placeholder="Rechercher...">
</div>
```

**Clipboard copy** :
```html
<div class="input-group">
  <input type="text" class="form-control" value="contact@example.fr" readonly>
  <button class="btn btn-outline-primary btn-ico-only" type="button" data-it-clipboard="copy" data-bs-toggle="tooltip" data-bs-trigger="manual" data-bs-title="Copie !">
    <i class="ri-file-copy-line fw-normal" aria-hidden="true"></i>
    <span class="visually-hidden">Copier</span>
  </button>
</div>
```

**Mot de passe avec bascule afficher/masquer** :
```html
<div class="input-group">
  <input type="password" class="form-control" id="password">
  <button class="btn btn-outline-primary btn-ico" type="button" data-it-story-password="toggle">
    <i class="ri-eye-line" aria-hidden="true"></i>
    <span>Afficher</span>
  </button>
</div>
```

### Search `.c-search`

Barre de recherche avec grille adaptative, integration Select2 optionnelle et slider de resultats.

**Barre simple** :
```html
<div class="c-search__bar">
  <div class="c-search__bar__grid">
    <div class="input-group">
      <span class="input-group-text"><i class="ri-search-line" aria-hidden="true"></i></span>
      <input type="search" class="form-control" placeholder="Rechercher...">
    </div>
    <button class="btn btn-primary btn-ico" type="submit">
      <i class="ri-search-line" aria-hidden="true"></i>
      <span>Rechercher</span>
    </button>
  </div>
</div>
```

Style barre : `background: white`, `border: 1px solid border-color`, `border-radius: radius-lg`. La grille passe a N colonnes + auto au breakpoint md.

### Dropzone `.c-dropzone`

Zone de depot de fichiers avec bordure pointillee.

```html
<div class="c-dropzone">
  <input type="file" id="fileUpload" class="form-control">
  <label for="fileUpload">Deposer un fichier ou cliquer pour parcourir</label>
</div>
```

Style : `padding: 16px`, `border: 2px dashed gray-700`, `border-radius: 4px`, `text-align: center`.

---

## NavInfo `.c-navinfo`

Navigation contextuelle en haut de page (retour, navigation entre fiches, info complementaire). Se place dans `.s-title-02`.

```html
<div class="c-navinfo">
  <div class="c-navinfo__prevstep">
    <button type="button" class="btn btn-ico btn-link ps-0" aria-label="Retour vers la liste de candidatures">
      <i class="ri-arrow-drop-left-line ri-xl fw-medium" aria-hidden="true"></i>
      <span>Retour</span>
    </button>
  </div>
  <div class="c-navinfo__prevnext">
    <a href="" class="btn btn-ico-only btn-link disabled" data-bs-toggle="tooltip" data-bs-placement="bottom" data-bs-title="Candidature precedente">
      <span class="visually-hidden">Candidature precedente</span>
      <i class="ri-arrow-left-circle-line ri-xl fw-medium" aria-hidden="true"></i>
    </a>
    <a href="" class="btn btn-ico-only btn-link" data-bs-toggle="tooltip" data-bs-placement="bottom" data-bs-title="Candidature suivante">
      <span class="visually-hidden">Candidature suivante</span>
      <i class="ri-arrow-right-circle-line ri-xl fw-medium" aria-hidden="true"></i>
    </a>
  </div>
  <div class="c-navinfo__info">
    Mise a jour le 14/03/25
  </div>
</div>
```

---

## Mise en page et layout

### Layout authentifie `.l-authenticated`

Classe sur `<body>` pour les pages avec navigation laterale (sidebar offcanvas). Structure :

```html
<body class="l-authenticated">
  <nav class="c-skiplinks">...</nav>
  <header class="s-header">...</header>
  <div class="l-authenticated__wrapper">
    <aside class="offcanvas offcanvas-end offcanvas-xl" id="offcanvasSidebar">
      <div class="offcanvas-header">
        <button type="button" class="btn-close" data-bs-dismiss="offcanvas" data-bs-target="#offcanvasSidebar" aria-label="Fermer le menu"></button>
      </div>
      <div class="offcanvas-body">
        <nav aria-label="Menu principal" id="nav-primary">
          <ul class="nav nav-tabs flex-column">
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="#">
                <i class="ri-dashboard-line" aria-hidden="true"></i>
                <span>Tableau de bord</span>
              </a>
            </li>
          </ul>
        </nav>
      </div>
    </aside>
    <main class="s-main" role="main" id="main">
      <!-- sections de contenu -->
    </main>
  </div>
  <footer>...</footer>
</body>
```

Comportement : offcanvas a droite sur mobile (< xl), sidebar fixe a gauche sur xl+. Container main contraint a `max-width: xl` (1280px).

### En-tete `.s-header`

```html
<header class="s-header" role="banner">
  <section class="s-header__container container">
    <a href="/" class="s-header__logo">
      <img src="logo-emplois-light.svg" alt="Les emplois de l'inclusion - Retour a l'accueil" height="56">
    </a>
    <nav>
      <ul class="s-header__nav">
        <li><a href="#">Lien 1</a></li>
      </ul>
    </nav>
  </section>
</header>
```

Style : `position: sticky`, `top: 0`, fond blanc, `box-shadow`. En mode authentifie : fond `nuance-10`.

### Pied de page `.s-footer`

Structure en 3 parties :

```html
<footer>
  <section class="s-footer-quick">
    <!-- Liens rapides -->
  </section>
  <section class="s-footer-gip">
    <!-- Logo et liens du GIP -->
  </section>
  <section class="s-footer-legal">
    <!-- Mentions legales, accessibilite -->
  </section>
</footer>
```

### Skiplinks `.c-skiplinks`

```html
<nav role="navigation" aria-label="Acces rapide" class="c-skiplinks">
  <ul>
    <li><a href="#nav-primary">Aller au menu principal</a></li>
    <li><a href="#main">Aller au contenu principal</a></li>
  </ul>
</nav>
```

---

## Sections de page

### Section generique `.s-section`

Espacement vertical entre blocs de contenu.

```html
<section class="s-section">
  <div class="s-section__container container">
    <div class="s-section__row row">
      <div class="s-section__col col-12">
        <h2>Titre de section</h2>
        <p>Contenu...</p>
      </div>
    </div>
  </div>
</section>
```

Style : `margin-top/bottom: 24px`, `32px` a partir de lg. Variante max-width : `.container-max-lg`.

### Title01 `.s-title-01`

Titre de page simple avec sous-titre et paragraphe.

```html
<section class="s-title-01">
  <div class="s-title-01__container container">
    <div class="s-title-01__row row">
      <div class="s-title-01__col col-12">
        <h1>Titre de la page</h1>
        <h2>Sous-titre</h2>
        <p>Paragraphe introductif.</p>
      </div>
    </div>
  </div>
</section>
```

### Title02 `.s-title-02`

Titre de page complexe avec navinfo, composant c-title, et blocs contextuels (alerts, tabs, c-box--action).

```html
<section class="s-title-02">
  <div class="s-title-02__container container">
    <div class="s-title-02__row row">
      <div class="s-title-02__col col-12">
        <div class="c-navinfo">
          <div class="c-navinfo__prevstep">
            <button type="button" class="btn btn-ico btn-link ps-0" aria-label="Retour">
              <i class="ri-arrow-drop-left-line ri-xl fw-medium" aria-hidden="true"></i>
              <span>Retour</span>
            </button>
          </div>
        </div>
        <div class="c-title">
          <div class="c-title__main">
            <h1>Titre de la page</h1>
          </div>
          <div class="c-title__cta">
            <a href="#" class="btn btn-primary btn-ico">
              <i class="ri-add-line fw-medium" aria-hidden="true"></i>
              <span>Action</span>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
```

Devient sticky dans le layout authentifie a partir de xxl, avec un gradient fade en bas.

### HomeSearch `.s-home-search`

Hero de la page d'accueil non-authentifiee. Visuel de fond, titre hero, onglets de recherche, composant c-search.

```html
<section class="s-home-search">
  <div class="s-home-search__container container">
    <div class="s-home-search__row row">
      <div class="s-home-search__col col-12">
        <img class="s-home-search__visuel" src="hero.webp" alt="" width="1305" height="870">
        <h1>Titre hero</h1>
        <ul class="nav justify-content-center gap-2 mb-3" role="tablist">
          <li class="nav-item" role="presentation">
            <button class="s-home-search__badge active" data-bs-toggle="tab" data-bs-target="#tab1" role="tab" aria-selected="true">
              <i class="ri-briefcase-line me-1 d-none d-md-inline" aria-hidden="true"></i>
              <span>Onglet 1</span>
            </button>
          </li>
        </ul>
        <div class="tab-content">
          <div class="tab-pane active" id="tab1" role="tabpanel">
            <div class="c-search">
              <div class="c-search__bar">
                <!-- formulaire de recherche -->
              </div>
            </div>
          </div>
        </div>
        <p class="s-home-search__note">Note sous la recherche.</p>
      </div>
    </div>
  </div>
</section>
```

### HomeTitle01 `.s-home-title-01`

Hero alternatif avec recherche et cartes d'action.

```html
<section class="s-home-title-01 s-home-title-01--communaute">
  <div class="s-home-title-01__container container container-max-lg">
    <div class="s-home-title-01__row row">
      <div class="s-home-title-01__col col-12 col-md-8 col-lg-7 mb-4">
        <h1 class="h1-hero">Titre hero</h1>
        <p class="lead mb-md-5">Introduction.</p>
        <form class="s-home-title-01__form" role="search">
          <!-- input group de recherche -->
        </form>
      </div>
    </div>
    <div class="s-home-title-01__row row">
      <div class="s-home-title-01__col col-12">
        <div class="s-home-title-01__btn-group flex-column flex-md-row gap-3 gap-md-4">
          <div class="s-home-title-01__btn p-3 py-md-4">
            <div class="w-25 w-md-40">
              <img src="illu.png" class="img-fluid" alt="">
            </div>
            <div class="ps-3">
              <a href="#" class="btn-link stretched-link">Action 1</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
```

### ArticleFigure01 `.s-article-figure-01`

Bloc editorial : illustration + article cote a cote. Modifieur `--ltr` pour inverser.

```html
<section class="s-article-figure-01 s-article-figure-01--ltr">
  <div class="s-article-figure-01__container container container-max-lg">
    <div class="s-article-figure-01__row row">
      <div class="s-article-figure-01__col s-article-figure-01__col--figure col-12 col-md-3 col-lg-4 d-flex align-items-center justify-content-center">
        <figure class="w-50 w-md-100">
          <img src="illu.png" class="img-fluid img-fitcover" alt="">
        </figure>
      </div>
      <div class="s-article-figure-01__col s-article-figure-01__col--article col-12 col-md-9 col-lg-8 d-flex align-items-center">
        <article>
          <h2 class="h1 text-tertiary">Titre</h2>
          <p>Contenu...</p>
          <a href="#" class="btn btn-outline-primary">En savoir plus</a>
        </article>
      </div>
    </div>
  </div>
</section>
```

### ArticlePicture01 `.s-article-picture-01`

Similaire a ArticleFigure01 mais avec `<picture>` et lien cliquable.

```html
<section class="s-article-picture-01">
  <div class="s-article-picture-01__container container">
    <div class="s-article-picture-01__row row align-items-center">
      <div class="s-article-picture-01__col col-12 col-lg-6">
        <a href="#">
          <picture>
            <source srcset="image.webp" type="image/webp">
            <img src="image.jpg" alt="Description" class="img-fluid">
          </picture>
        </a>
      </div>
      <div class="s-article-picture-01__col col-12 col-lg-6">
        <article>
          <h2>Titre</h2>
          <p>Contenu de l'article.</p>
        </article>
      </div>
    </div>
  </div>
</section>
```

### ArticlePictureGroup01 `.s-article-picture-group-01`

Groupe d'articles avec images alternees (image a gauche puis a droite). Variantes de couleur par service : `--emploi`, `--marche`, `--communaute`, `--pilotage`. Chaque ligne alterne automatiquement l'ordre image/texte via `:nth-child(odd/even)`.

```html
<section class="s-article-picture-group-01 s-article-picture-group-01--emploi">
  <div class="s-article-picture-group-01__container container">
    <div class="s-article-picture-group-01__row row">
      <div class="s-article-picture-group-01__col s-article-picture-group-01__col--picture col-12 col-lg-6">
        <img src="..." alt="..." class="img-fluid">
      </div>
      <div class="s-article-picture-group-01__col s-article-picture-group-01__col--article col-12 col-lg-6">
        <article>
          <span class="h1">Titre</span>
          <p>Contenu de l'article.</p>
        </article>
      </div>
    </div>
  </div>
</section>
```

### CardsGrid01 `.s-cards-grid-01`

Grille de cartes avec espacement vertical. Peut recevoir la classe `.has-illustration-bg-01` pour afficher une illustration de fond decorative (visible a partir de `xl`).

```html
<section class="s-cards-grid-01 has-illustration-bg-01">
  <div class="s-cards-grid-01__container container">
    <!-- Cartes Bootstrap standard a l'interieur -->
  </div>
</section>
```

### ArticleCols01 `.s-articles-cols-01`

Articles en multi-colonnes (2, 3 ou 4 colonnes selon le contenu).

```html
<section class="s-articles-cols-01">
  <div class="s-articles-cols-01__container container">
    <div class="s-articles-cols-01__row row">
      <div class="s-articles-cols-01__col col-12 col-lg-4">
        <article>
          <h3>Titre article 1</h3>
          <p>Contenu.</p>
        </article>
      </div>
      <div class="s-articles-cols-01__col col-12 col-lg-4">
        <article>
          <h3>Titre article 2</h3>
          <p>Contenu.</p>
        </article>
      </div>
    </div>
  </div>
</section>
```

### PageMenu01 `.s-page-menu-01`

Navigation de page avec titre hero et grille de liens d'ancrage.

```html
<section class="s-page-menu-01">
  <div class="s-page-menu-01__container container">
    <div class="s-page-menu-01__row row align-items-center">
      <div class="s-page-menu-01__col s-page-menu-01__col--title col-12 col-lg-5">
        <h1 class="h1-hero"><strong>Titre</strong></h1>
      </div>
      <div class="s-page-menu-01__col s-page-menu-01__col--grid col-12 col-lg-7">
        <ul>
          <li><a href="#section1">Lien d'ancrage 1</a></li>
          <li><a href="#section2">Lien d'ancrage 2</a></li>
        </ul>
      </div>
    </div>
  </div>
</section>
```

### Tabs01 `.s-tabs-01`

Section avec onglets glissants (sliding tabs via Tiny Slider).

```html
<section class="s-tabs-01">
  <div class="s-tabs-01__container container">
    <div class="s-tabs-01__row row">
      <div class="s-tabs-01__col col-12">
        <ul class="s-tabs-01__nav nav nav-tabs" role="tablist" data-it-sliding-tabs="true">
          <li class="nav-item" role="presentation">
            <a class="nav-link active" data-bs-toggle="tab" href="#tab1" role="tab" aria-selected="true">Onglet 1</a>
          </li>
          <!-- ... -->
        </ul>
        <div class="tab-content">
          <div class="tab-pane fade show active" id="tab1" role="tabpanel">Contenu</div>
        </div>
      </div>
    </div>
  </div>
</section>
```

---

## Utilitaires personnalises

Classes utilitaires specifiques au theme, en complement de Bootstrap.

| Classe | Usage |
|---|---|
| `.fs-base` | font-size base (16px) |
| `.fs-lg` | font-size large (18px) |
| `.fs-sm` | font-size small (14px) |
| `.fs-xs` | font-size extra-small (12px) |
| `.ff-base` | font-family Marianne |
| `.ff-extra-01` | font-family Covered (decorative) |
| `.lh-base` / `.lh-lg` / `.lh-sm` | surcharges line-height |
| `.has-external-link` | Ajoute une icone lien externe (Remix `\ecaf`) apres l'element |
| `.has-downloadable-file` | Ajoute une icone telechargement apres l'element |
| `.has-ellipsis` | Tronque le texte avec ellipsis (overflow hidden, nowrap) |
| `.has-ratio-16-9` | Conteneur en ratio 16:9 via aspect-ratio |
| `.has-textarea-ratio-16-9` | Textarea en ratio 32:9, 16:9 a partir de xxl |
| `.has-no-transition` | Desactive les transitions (y compris collapse) |
| `.has-collapse-caret` | Chevron Remix qui change selon `aria-expanded` |
| `.img-fitcover` | `object-fit: cover; width: 100%` |
| `.img-muted` | `grayscale(100%); opacity: 0.3` |
| `.text-decoration-dashed` | Souligne en pointille |
| `.text-disabled` / `.disabled` | Couleur disabled + pointer-events none |
| `.text-muted` | Couleur attenuee (muted-color) |
| `.shadow-xl` | Ombre extra-large |
| `.rounded-xl` | Border-radius xl (16px) |
| `.white-space-normal` / `.white-space-nowrap` | Controle du retour a la ligne |

**Collapse caret avec texte dynamique** :
```html
<button class="has-collapse-caret" data-bs-toggle="collapse" data-bs-target="#content"
  data-it-collapse-text-show="Afficher" data-it-collapse-text-hide="Masquer"
  aria-expanded="false">
</button>
```

### Separateur avec texte `<hr data-it-text>`

```html
<hr class="my-5" data-it-text="ou">
```

Affiche un texte centre sur la ligne de separation.

### Dimensionnement personnalise

Classes responsive `.w-{bp}-{value}`, `.mw-{bp}-{value}`, `.mh-{bp}-{value}`.

**Width** : `25`, `33`, `40`, `50`, `66`, `75`, `50px`, `100px`, `200px`, `300px`, `400px`
**Max-width** : `25`, `33`, `50`, `66`, `75`
**Max-height** : `25`, `33`, `50`, `66`, `75`, `25vh`, `33vh`, `50vh`, `66vh`, `75vh`, `100vh`

Exemples : `.w-50`, `.w-md-33`, `.mw-75`, `.mh-50vh`, `.w-200px`.

---

## Offcanvas Filters `.c-offcanvas-filters`

Panneau lateral de filtres pour les pages de recherche/liste. Utilise l'offcanvas Bootstrap avec styles de formulaire adaptes.

```html
<div class="c-offcanvas-filters">
  <div class="offcanvas offcanvas-end" id="offcanvasFilters" tabindex="-1">
    <div class="offcanvas-header">
      <h5>Filtres</h5>
      <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Fermer"></button>
    </div>
    <div class="offcanvas-body">
      <fieldset>
        <legend>Categorie</legend>
        <button type="button" class="has-collapse-caret" data-bs-toggle="collapse" data-bs-target="#filter1" aria-expanded="false">
          Sous-categorie
        </button>
        <div class="collapse" id="filter1">
          <ul>
            <li>
              <div class="form-check">
                <input type="checkbox" class="form-check-input" id="f1">
                <label class="form-check-label" for="f1">Option</label>
              </div>
            </li>
          </ul>
        </div>
      </fieldset>
    </div>
  </div>
</div>
```

---

## Modeles de pages

### Fiche Detail (Box Detail)

Page de consultation d'une fiche avec sections de donnees.

**Regles d'integration** :
- Pour chaque sous-page en onglet, ajouter un `<h2>` repetant le libelle d'onglet
- Pour chaque page sans onglet, `<h2 class="visually-hidden">` pour maintenir la hierarchie
- Dans chaque `.c-box`, ajouter un `<h3>`
- Privilegier la separation en plusieurs `.c-box` plutot que `<hr>`
- Action principale dans une `.c-box` : `.btn-outline-primary` a droite du titre `<h3>`
- Action complementaire : `.btn-link` ou `.btn-secondary`
- Info permanente : `.c-info`
- Info conditionnelle : `.alert`

**Structure type** :
```html
<main class="s-main" role="main">
  <section class="s-title-02">...</section>
  <section class="s-section">
    <div class="s-section__container container">
      <div class="s-section__row row">
        <div class="s-section__col col-12 col-xxl-8 col-xxxl-9 order-3 order-xxl-2">
          <h2 class="visually-hidden">Titre de section</h2>
          <div class="c-box mb-3 mb-md-4">
            <div class="row mb-3">
              <div class="col-12 col-sm"><h3 class="mb-0">Titre</h3></div>
              <div class="col-12 col-sm-auto mt-2 mt-sm-0">
                <a href="#" class="btn btn-ico btn-outline-primary">...</a>
              </div>
            </div>
            <!-- contenu -->
          </div>
        </div>
        <div class="s-section__col col-12 col-xxl-4 col-xxxl-3 order-2 order-xxl-3">
          <!-- sidebar boxes -->
        </div>
      </div>
    </div>
  </section>
</main>
```

### Page Formulaire (Form Detail)

Page de saisie avec stepper et formulaire structure.

**Regles d'integration** :
- `<h2 class="visually-hidden">` pour la hierarchie de titres
- Dans `.c-form`, regrouper les champs en `<fieldset>` + `<legend class="h3">`
- Le titre du formulaire est porte par `legend.h3`
- Stepper (`.c-stepper`) au-dessus du formulaire pour indiquer la progression
- Actions : annuler (`.btn-link.btn-ico`) + suivant/enregistrer (`.btn-primary`)

---

## Attributs `data-it-*` (comportements JS du theme)

| Attribut | Valeur | Usage |
|---|---|---|
| `data-it-sliding-tabs` | `"true"` | Active le slider Tiny Slider sur un `nav-tabs` |
| `data-it-sliding-tabs-startindex` | `"N"` | Index de depart du slider |
| `data-it-clipboard-button` | `"copy"` | Active le comportement copie presse-papier sur le bouton |
| `data-it-copy-to-clipboard` | `"valeur"` | Valeur a copier (sur le meme element que `data-it-clipboard-button`) |
| `data-it-expandable` | `"true"` | Textarea auto-extensible |
| `data-it-state-label-off` | `"Desactive"` | Label switch quand off |
| `data-it-state-label-on` | `"Active"` | Label switch quand on |
| `data-it-collapse-text-show` | `"Afficher"` | Texte du caret collapse quand ferme |
| `data-it-collapse-text-hide` | `"Masquer"` | Texte du caret collapse quand ouvert |
| `data-it-text` | `"ou"` | Affiche un texte centre sur un `<hr>` |
| `data-it-select2` | (sur `<select>`) | Active Select2 sur le select (theme bootstrap-5) |
| `data-it-action` | varies | Actions JS diverses du theme |
| `data-it-easymde` | `"true"` | Active l'editeur Markdown EasyMDE |

---

## Bibliotheques externes

| Lib | Usage | Integration |
|---|---|---|
| **Remix Icon** | Icones | Police d'icones en vendor, `<i class="ri-{nom}-{style}">` |
| **Select2** | Selects enrichis | Plugin jQuery, theme `bootstrap-5`, active via `data-it-select2` sur `<select>` |
| **Duet Date Picker** | Date picker | Web component `<duet-date-picker>`, format `DD/MM/YYYY` |
| **Intro.js** | Tutoriels in-app | Overlay pas-a-pas |
| **Tarte au citron** | Consentement cookies | Gestionnaire RGPD |
| **Tiny Slider** | Carrousel/slider | Slider responsive, utilise avec `data-it-sliding-tabs` |

### Select2

Activation : ajouter `data-it-select2` sur le `<select>`. Options via attributs `data-*` :

```html
<select class="form-select" data-it-select2 data-placeholder="Choisir..." data-allow-clear="true">
  <option></option>
  <option value="1">Option 1</option>
  <option value="2">Option 2</option>
</select>
```

Multi-select : ajouter `data-multiple` et `multiple` sur le `<select>`.
AJAX : initialisation JS specifique avec `$.fn.select2({ajax: {...}})`.

### Duet Date Picker

```html
<duet-date-picker identifier="date-debut" value="2024-07-05"></duet-date-picker>
```

Format d'affichage : `DD/MM/YYYY`. Valeur interne : `YYYY-MM-DD`.

---

## Logos

48 logos et monogrammes des services de la plateforme de l'inclusion.

**Services** : Emplois, Marche, Communaute, Pilotage, Dora, GPS, data·inclusion, Inclusion Connect, rdv-insertion, Plateforme, immersion facilitee, Mon recap, Generique-plateforme.

**Convention de nommage** : `{service}-{type}-{theme}.{ext}`
- Types : `logo`, `monogramme`
- Themes : `light` (fond clair), `dark` (fond sombre)
- Formats : SVG (prefere), PNG (quand SVG indisponible)

Exemples : `emplois-logo-light.svg`, `dora-monogramme-dark.png`

---

## Accessibilite

- Icones decoratives : toujours `aria-hidden="true"`
- Bouton icone seule : `aria-label` obligatoire
- Alertes : `role="status"` (info) ou `role="alert"` (erreur critique)
- Titres caches : `.visually-hidden` pour le contexte screen-reader
- Focus ring : `0.2rem`, opacity 1, couleur tertiary a 30%
- Skiplinks : composant d'accessibilite pour sauter au contenu
- Navigation : `aria-label` sur les `<nav>`, `aria-current="page"` sur le lien actif

---

## Demarrage rapide — Prototype

Pour generer un prototype HTML fonctionnel avec le theme itou, utiliser les assets fournis avec ce skill (dossiers `stylesheets/`, `javascripts/`, `fonts/`, `images/`) :

### En-tete minimal

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Titre de la page</title>
  <link rel="shortcut icon" href="./images/favicon.ico" type="image/ico">
  <link rel="stylesheet" crossorigin href="./stylesheets/app.css">
  <script type="module" crossorigin src="./javascripts/app.js"></script>
</head>
```

### Scripts en pied de page (obligatoires)

```html
<script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.8/dist/umd/popper.min.js" integrity="sha384-I7E8VVD/ismYTF4hNIPjVp/Zjvgyol6VFvRkX/vR+Vc4jQkC+hVqc2pM8ODewa9r" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/js/bootstrap.min.js" integrity="sha384-G/EV+4j2dNv+tEPo3++6LCgdCROaejBqfUeNjuKAiuXbjrxilcCdDz6ZAVfHWe1Y" crossorigin="anonymous"></script>
```

### Scripts optionnels (selon composants utilises)

```html
<!-- Select2 (si <select data-it-select2>) -->
<script src="https://code.jquery.com/jquery-3.7.1.min.js" integrity="sha256-/JqT3SQfawRcv/BIHPThkBvs0OEvtFFmqPF/lYI/Cxo=" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/select2@4.0.13/dist/js/select2.full.min.js"></script>

<!-- Duet Date Picker (si <duet-date-picker>) -->
<script type="module" src="https://cdn.jsdelivr.net/npm/@nicktomlin/duet-date-picker@1.4.0/dist/duet/duet.esm.js"></script>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@nicktomlin/duet-date-picker@1.4.0/dist/duet/themes/default.css">
```

### Polices incluses dans app.css

Le CSS compile embarque les declarations `@font-face` pour :
- **Marianne** (Regular, Medium, Bold, ExtraBold + italiques) — woff/woff2
- **Covered By Your Grace** — woff/woff2
- **Remix Icon** — eot/ttf/woff/woff2

Les fichiers de polices sont egalement fournis dans le dossier `fonts/` de ce skill. Pas besoin de lien Google Fonts ou CDN supplementaire.

### Version

itoutheme v3.6.3, Bootstrap 5.3.8

---

## Architecture SCSS

Le theme s'organise en couches importees dans `src/stylesheets/app.scss` :

```
app.scss
├── base/
│   ├── _variables.scss     — Toutes les variables Bootstrap + personnalisees ($it-*)
│   ├── _mixins.scss        — Mixins personnalises (responsive, composants)
│   ├── _utilities.scss     — Extension de la map $utilities Bootstrap
│   ├── _custom.scss        — Surcharges globales (body, liens, titres)
│   ├── _utilities-custom.scss — Classes utilitaires personnalisees (.has-*, .img-*, .text-disabled)
│   └── _print.scss         — Styles d'impression
│
├── vendors/
│   ├── _core.scss          — Import noyau Bootstrap
│   ├── _remixicon.scss     — @font-face Remix Icon
│   ├── _select2.scss       — Theme Select2 Bootstrap 5 complet
│   ├── _duetdatepicker.scss — Surcharges styles Duet Date Picker
│   ├── _tarteaucitron.scss — Bandeau cookies
│   ├── _tiny-slider.scss   — Carousel Tiny Slider
│   ├── _introjs.scss       — Onboarding Intro.js
│   └── _easymde.scss       — Editeur markdown EasyMDE
│
├── components/             — Composants personnalises BEM (.c-*)
│   ├── _alert.scss         — Alertes + global-alert + alert-dismissible-once
│   ├── _accordion.scss     — Accordion flush
│   ├── _badge.scss         — 5 tailles, badge-group, circular
│   ├── _box.scss           — Toutes variantes c-box (results, summary, dashboard, etc.)
│   ├── _button.scss        — Boutons personnalises (btn-ico, btn-dropdown-filter)
│   ├── _card.scss          — Cards + c-card + has-rich-radio
│   ├── _dropdown.scss      — Dropdown + dropdown-organization + dropdown-nexus
│   ├── _dropzone.scss      — Upload zone
│   ├── _form.scss          — c-form, form-group, form-group-required, label widths
│   ├── _info.scss          — c-info (bandeau promotionnel)
│   ├── _list.scss          — list-data, list-step, list-note, list-ordered
│   ├── _list-group.scss    — Variantes list-group
│   ├── _navbar.scss        — c-navinfo (navigation laterale)
│   ├── _offcanvas-filters.scss — Filtres en panneau lateral
│   ├── _search.scss        — c-search (barre de recherche)
│   ├── _skiplinks.scss     — Liens d'evitement accessibilite
│   ├── _stepper.scss       — c-stepper (progress multi-etapes)
│   ├── _table.scss         — Tables sortable + selection
│   ├── _tabs.scss          — Onglets + sliding-tabs + pills personnalises
│   ├── _tag.scss           — Tags filtres
│   ├── _title.scss         — c-title (titre de page)
│   └── _toast.scss         — Toasts personnalises
│
├── sections/               — Sections de mise en page (.s-*)
│   ├── _main.scss          — s-main
│   ├── _header.scss        — s-header + s-header-authenticated + s-header-print
│   ├── _footer.scss        — s-footer-community, s-footer-quick, s-footer-gip, s-footer-legal
│   ├── _section.scss       — s-section generique
│   ├── _title-01.scss      — s-title-01 (bandeau hero pleine largeur)
│   ├── _title-02.scss      — s-title-02 (en-tete de page standard)
│   ├── _tabs-01.scss       — s-tabs-01 (section avec onglets)
│   ├── _home-title-01.scss — Section homepage avec cartes illustrees
│   ├── _article-figure-01.scss — Section article avec figure
│   ├── _article-picture-01.scss — Section article avec image
│   ├── _article-picture-group-01.scss — Groupe d'articles image/texte alternes
│   ├── _articles-cols-01.scss — Grille d'articles en colonnes
│   ├── _cards-grid-01.scss    — Grille de cartes avec illustration optionnelle
│   ├── _page-menu-01.scss  — Menu lateral de page
│   ├── _form-01.scss       — Section formulaire
│   ├── _cms.scss           — Contenu CMS rich text
│   ├── _box.scss           — Section conteneur de box
│   └── _postheader.scss    — Espace sous le header
│
├── layouts/
│   └── _layout.scss        — l-authenticated (sidebar + main grid)
│
└── pages/
    └── _page.scss          — Styles specifiques de pages (p-home, etc.)
```

---

## Modeles HTML de reference

Les modeles du dossier `modeles/` servent de reference pour la structure des pages (copies depuis `dist/` du repo).

**Note chemins** : les modeles referencent les assets via `./images/`, `./stylesheets/`, `./javascripts/`. Pour les utiliser directement, copier les modeles a la racine du skill ou ajuster les chemins vers `../images/` etc.

### Catalogue des modeles

**Pages non-authentifiees** (en-tete `.s-header` + pied de page complet) :
- `layout-itou-not-authenticated-homepage.html` — Page d'accueil avec recherche
- `layout-itou-not-authenticated-search-result.html` — Resultats de recherche (2176 lignes)
- `layout-itou-not-authenticated-mentions.html` — Mentions legales
- `layout-itou-not-authenticated-signup.html` — Inscription etape initiale
- `layout-itou-not-authenticated-signup-step-*.html` — Etapes inscription (structure, proconnect, confirmation)
- `layout-itou-not-authenticated-test.html` — Page de test composants

**Pages authentifiees** (`body.l-authenticated` + en-tete `.s-header-authenticated` + barre laterale offcanvas) :
- `layout-itou-authenticated-dashboard.html` — Tableau de bord (896 lignes)
- `layout-itou-authenticated-form.html` — Formulaire multi-etapes (541 lignes)
- `layout-itou-authenticated-detail-candidature.html` — Fiche detail candidature (924 lignes)
- `layout-itou-authenticated-search-result.html` — Resultats recherche authentifie (3445 lignes)
- `layout-itou-authenticated-candidature-result.html` — Resultats candidatures
- `layout-itou-authenticated-cms.html` — Page contenu CMS
- `layout-itou-authenticated-mentions.html` — Mentions legales (authentifie)
- `layout-itou-authenticated-test.html` — Page de test composants

**Librairies externes** :
- `external-libs-itou-s2.html` — Demonstration Select2
- `external-libs-itou-ddp.html` — Demonstration Duet Date Picker
- `external-libs-itou-in.html` — Demonstration Intro.js
- `external-libs-itou-slider.html` — Demonstration Tiny Slider
- `external-libs-itou-tac.html` — Demonstration Tarte au citron

**Autre sous-produit** :
- `layout-not-itou-pilotage-form.html` — Formulaire Pilotage (style different)

### Squelette : Page non-authentifiee

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Titre — Les emplois de l'inclusion</title>
  <link rel="shortcut icon" href="./images/favicon.ico" type="image/ico">
  <script type="module" crossorigin src="./javascripts/app.js"></script>
  <link rel="stylesheet" crossorigin href="./stylesheets/app.css">
</head>
<body id="top">
  <!-- Skiplinks -->
  <nav role="navigation" aria-label="Acces rapide" class="c-skiplinks">
    <ul>
      <li><a href="#nav-primary">Aller au menu principal</a></li>
      <li><a href="#main">Aller au contenu principal</a></li>
    </ul>
  </nav>

  <!-- Global alerts (optionnel) -->
  <div class="global-messages-container">
    <!-- <div class="alert alert-danger alert-dismissible fade show" role="status">...</div> -->
  </div>

  <!-- Header non-authentifie -->
  <header role="banner" id="header">
    <section class="s-header-print">
      <div class="container">
        <div class="row">
          <div class="col-md-auto d-flex align-items-center py-2">
            <img src="./images/logo-republique-francaise.svg" height="70" alt="Republique Francaise">
          </div>
          <div class="col d-flex align-items-center">
            <img src="./images/logo-emploi-inclusion.svg" height="60" alt="Les emplois de l'inclusion">
          </div>
        </div>
      </div>
    </section>
    <section class="s-header">
      <div class="s-header__container container">
        <div class="s-header__row row">
          <div class="s-header__col s-header__col--logo-ministere col col-md-auto d-flex align-items-center pe-0">
            <a href="/" class="s-header__logo-ministere">
              <img src="./images/logo-republique-francaise.svg" alt="Republique Francaise">
            </a>
          </div>
          <div class="s-header__col s-header__col--logo-service col-auto d-flex align-items-center px-0">
            <a href="/"><img src="./images/logo-emploi-inclusion.svg" alt="Les emplois de l'inclusion" height="90"></a>
          </div>
          <div class="s-header__col s-header__col--nav col d-none d-lg-inline-flex d-lg-flex align-items-center justify-content-end pe-0 pe-xl-3">
            <nav role="navigation" id="nav-primary" aria-label="Navigation principale">
              <ul>
                <!-- Liens navigation -->
                <li><a href="/connexion" class="btn btn-primary btn-ico">
                  <i class="ri-account-circle-line" aria-hidden="true"></i>
                  <span>Connexion</span>
                </a></li>
              </ul>
            </nav>
          </div>
          <div class="s-header__col s-header__col--burger col-auto d-flex d-lg-none align-items-center ps-0">
            <button type="button" class="btn btn-link btn-ico pe-0" data-bs-toggle="offcanvas" data-bs-target="#offcanvasNav" aria-controls="offcanvasNav">
              <i class="ri-menu-line" aria-hidden="true"></i>
              <span>Menu</span>
            </button>
          </div>
        </div>
      </div>
    </section>
  </header>

  <!-- Contenu principal -->
  <main class="s-main" role="main" id="main">
    <section class="s-title-01">
      <div class="s-title-01__container container">
        <div class="s-title-01__row row">
          <div class="s-title-01__col col-12 col-lg-8">
            <h1>Titre de la page</h1>
            <p>Description de la page</p>
          </div>
        </div>
      </div>
    </section>
    <section class="s-section">
      <div class="s-section__container container">
        <div class="s-section__row row">
          <div class="s-section__col col-12">
            <!-- Contenu ici -->
          </div>
        </div>
      </div>
    </section>
  </main>

  <!-- Footer complet (4 sections) -->
  <footer role="contentinfo">
    <section class="s-footer-community">
      <div class="s-footer-community__container container">
        <div class="s-footer-community__row row">
          <div class="s-footer-community__col col-12">
            <!-- Lien communaute -->
          </div>
        </div>
      </div>
    </section>
    <section class="s-footer-quick">
      <div class="s-footer-quick__container container">
        <div class="s-footer-quick__row row">
          <div class="s-footer-quick__col col-12 col-lg-auto">
            <strong>A propos</strong>
            <ul><!-- Liens --></ul>
          </div>
          <div class="s-footer-quick__col col-12 col-lg-auto">
            <strong>Reseaux sociaux</strong>
            <ul><!-- Liens sociaux avec icones ri-*-fill --></ul>
          </div>
        </div>
      </div>
    </section>
    <section class="s-footer-gip">
      <div class="s-footer-gip__container container">
        <div class="s-footer-gip__row row">
          <div class="s-footer-gip__col s-footer-gip__col--logo col-12 col-md-6 col-lg-auto">
            <a href="https://inclusion.beta.gouv.fr/" target="_blank">
              <img src="./images/logo-plateforme-inclusion.svg" height="80" alt="Plateforme de l'inclusion">
            </a>
          </div>
          <div class="s-footer-gip__col col-12 col-md-6 col-lg">
            <p><strong>Ce service fait partie de la Plateforme de l'inclusion</strong></p>
          </div>
        </div>
      </div>
    </section>
    <section class="s-footer-legal">
      <div class="s-footer-legal__container container">
        <div class="s-footer-legal__row row">
          <div class="s-footer-legal__col col-12">
            <ul>
              <li><a href="">Accessibilite : partiellement conforme</a></li>
              <li><a href="">Mentions legales</a></li>
              <li><a href="">Conditions generales</a></li>
              <li><a href="">Confidentialite</a></li>
            </ul>
            <p>Sauf mention contraire, contenus sous licence <a href="https://github.com/etalab/licence-ouverte/blob/master/LO.md" target="_blank">etalab-2.0</a></p>
          </div>
        </div>
      </div>
    </section>
  </footer>

  <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.8/dist/umd/popper.min.js" crossorigin="anonymous"></script>
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/js/bootstrap.min.js" crossorigin="anonymous"></script>
</body>
</html>
```

### Squelette : Page authentifiee (tableau de bord)

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Tableau de bord — Les emplois de l'inclusion</title>
  <link rel="shortcut icon" href="./images/favicon.ico" type="image/ico">
  <script type="module" crossorigin src="./javascripts/app.js"></script>
  <link rel="stylesheet" crossorigin href="./stylesheets/app.css">
</head>
<body id="top" class="l-authenticated">
  <!-- Skiplinks -->
  <nav role="navigation" aria-label="Acces rapide" tabindex="0" class="c-skiplinks">
    <ul>
      <li><a href="#nav-primary">Aller au menu principal</a></li>
      <li><a href="#main">Aller au contenu principal</a></li>
    </ul>
  </nav>

  <header role="banner" id="header">
    <!-- Section impression -->
    <section class="s-header-print">
      <div class="container">
        <div class="row">
          <div class="col-md-auto d-flex align-items-center py-2">
            <img src="./images/logo-republique-francaise.svg" height="70" alt="Republique Francaise">
          </div>
          <div class="col d-flex align-items-center">
            <img src="./images/logo-emploi-inclusion.svg" height="60" alt="Les emplois de l'inclusion">
          </div>
        </div>
      </div>
    </section>

    <!-- Header authentifie -->
    <section class="s-header-authenticated">
      <div class="s-header-authenticated__container container">
        <div class="s-header-authenticated__row row">
          <div class="s-header-authenticated__col s-header-authenticated__col--logo-service col-auto d-flex align-items-center pe-0">
            <a href="/"><img src="./images/logo-emploi-inclusion.svg" alt="Les emplois de l'inclusion" height="90"></a>
          </div>
          <div class="s-header-authenticated__col s-header-authenticated__col--nav col d-flex align-items-center justify-content-end pe-0">
            <nav role="navigation" id="nav-primary" aria-label="Navigation principale">
              <ul>
                <!-- Dropdown utilisateur -->
                <li class="dropdown">
                  <button type="button" class="btn btn-outline-primary btn-ico bg-white dropdown-toggle" data-bs-toggle="dropdown" aria-expanded="false">
                    <i class="ri-account-circle-line" aria-hidden="true"></i>
                    <span class="d-none d-sm-inline-block ms-0 ms-sm-2">Mon espace</span>
                  </button>
                  <div class="dropdown-menu dropdown-menu-end">
                    <ul class="list-unstyled">
                      <li class="dropdown-item">
                        <div class="d-flex align-items-center">
                          <span class="flex-shrink-0"><i class="ri-user-line ri-2x"></i></span>
                          <div class="flex-grow-1 ms-2 lh-sm">
                            <span>Prenom NOM</span><br>
                            <span class="fs-sm lh-sm text-muted">email@example.com</span>
                          </div>
                        </div>
                      </li>
                      <li><div class="dropdown-divider"></div></li>
                      <li><a class="dropdown-item" href="">Tableau de bord</a></li>
                      <li><a class="dropdown-item" href="">Mes notifications</a></li>
                      <li class="dropdown-divider"></li>
                      <li class="dropdown-item"><button class="text-danger">Deconnexion</button></li>
                    </ul>
                  </div>
                </li>
                <!-- Dropdown organisation -->
                <li class="d-none d-lg-inline-block dropdown dropdown-organization">
                  <button type="button" class="btn btn-outline-primary btn-ico bg-white dropdown-toggle" data-bs-toggle="dropdown" aria-expanded="false">
                    <i class="ri-community-line" aria-hidden="true"></i>
                    <span>TYPE - Nom structure</span>
                  </button>
                  <div class="dropdown-menu w-100">
                    <form method="post">
                      <ul class="list-unstyled">
                        <li>
                          <button class="dropdown-item dropdown-item__summary active" name="organization_id" value="123">
                            <i class="ri-community-line" aria-hidden="true"></i>
                            <span>TYPE</span>
                            <strong>Nom structure</strong>
                          </button>
                        </li>
                      </ul>
                    </form>
                    <a href="" class="dropdown-item dropdown-item__summary is-last-sticky">
                      <i class="ri-add-line" aria-hidden="true"></i>
                      <span>Creer ou rejoindre</span>
                      <strong>une nouvelle structure</strong>
                    </a>
                  </div>
                </li>
              </ul>
            </nav>
          </div>
          <div class="s-header-authenticated__col s-header-authenticated__col--burger col-auto d-flex align-items-center ps-0">
            <button type="button" class="btn btn-link btn-ico pe-0" data-bs-toggle="offcanvas" data-bs-target="#offcanvasNav" aria-controls="offcanvasNav">
              <i class="ri-menu-line" aria-hidden="true"></i>
              <span>Menu</span>
            </button>
          </div>
        </div>
      </div>
    </section>

    <!-- Offcanvas mobile navigation -->
    <div class="offcanvas" id="offcanvasNav" aria-label="Navigation principale pour mobile">
      <div class="offcanvas-header offcanvas-header--organization">
        <div class="dropdown dropdown-organization flex-grow-1 py-4">
          <button type="button" class="dropdown-toggle dropdown-toggle__summary" data-bs-toggle="dropdown" aria-expanded="false">
            <i class="ri-community-line" aria-hidden="true"></i>
            <span>TYPE</span>
            <strong>Nom structure</strong>
          </button>
          <!-- dropdown-menu identique au header -->
        </div>
        <div class="border-start border-nuance-08 d-xl-none">
          <button type="button" class="btn-link ps-4 pt-5 pe-2 me-n2" data-bs-dismiss="offcanvas" aria-label="Fermer">
            <i class="ri-close-line" aria-hidden="true"></i>
          </button>
        </div>
      </div>
      <div class="offcanvas-body d-flex flex-column">
        <nav class="flex-grow-1" role="navigation" aria-label="Navigation principale pour mobile">
          <ul class="nav nav-tabs flex-column">
            <li class="nav-item">
              <a href="" class="nav-link active">
                <i class="ri-home-line fw-medium" aria-hidden="true"></i>
                <span>Accueil</span>
              </a>
            </li>
            <li class="nav-item">
              <a href="" class="nav-link">
                <i class="ri-draft-line fw-medium" aria-hidden="true"></i>
                <span>Candidatures</span>
              </a>
            </li>
            <li class="nav-item">
              <button class="nav-link has-collapse-caret w-100 text-start" data-bs-toggle="collapse" data-bs-target="#collapseNavSection" type="button" aria-expanded="false">
                <i class="ri-team-line fw-medium" aria-hidden="true"></i>
                <span>Section</span>
              </button>
              <div class="collapse" id="collapseNavSection">
                <ul>
                  <li><a href="">Sous-menu 1</a></li>
                  <li><a href="" class="active">Sous-menu 2</a></li>
                </ul>
              </div>
            </li>
          </ul>
        </nav>
        <!-- Dropup portail Nexus (optionnel) -->
        <div class="dropup dropup-center dropdown-nexus">
          <button class="btn btn-outline-primary btn-block bg-white dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
            <span>Mon portail</span>
          </button>
          <!-- dropdown-menu services -->
        </div>
      </div>
      <div class="offcanvas-footer flex-column align-items-stretch">
        <div class="offcanvas-footer__legal">
          <ul>
            <li><a href="">Accessibilite</a></li>
            <li><a href="">Mentions legales</a></li>
            <li><a href="">CGU</a></li>
          </ul>
        </div>
      </div>
    </div>
  </header>

  <!-- Contenu principal -->
  <main class="s-main" role="main" id="main">
    <section class="s-title-02">
      <div class="s-title-02__container container">
        <div class="s-title-02__row row">
          <div class="s-title-02__col col-12">
            <h1>Nom de la structure</h1>
            <p>TYPE - SIRET 000 000 000 00000</p>
          </div>
        </div>
      </div>
    </section>
    <section class="s-section">
      <div class="s-section__container container">
        <div class="s-section__row row">
          <div class="s-section__col col-12">
            <!-- Contenu dashboard : c-box en grille -->
            <div class="row row-cols-1 row-cols-md-2 row-cols-xxl-3 mt-3 mt-md-5">
              <div class="col mb-3 mb-md-4">
                <div class="c-box p-0 h-100">
                  <div class="p-3 p-lg-4">
                    <span class="h4 mb-0">Titre bloc</span>
                  </div>
                  <div class="px-3 px-lg-4">
                    <!-- Contenu du bloc -->
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>

  <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.8/dist/umd/popper.min.js" crossorigin="anonymous"></script>
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/js/bootstrap.min.js" crossorigin="anonymous"></script>
</body>
</html>
```

### Squelette : Page authentifiee (formulaire multi-etapes)

```html
<!-- Meme head et header que le squelette dashboard ci-dessus -->
<body id="top" class="l-authenticated">
  <!-- ... skiplinks + header identique ... -->

  <main class="s-main" role="main" id="main">
    <!-- En-tete de page -->
    <section class="s-title-02">
      <div class="s-title-02__container container">
        <div class="s-title-02__row row">
          <div class="s-title-02__col col-12">
            <div class="c-title">
              <div class="c-title__main">
                <h1>Titre du formulaire</h1>
                <p>Sous-titre ou contexte</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Contenu formulaire -->
    <section class="s-section">
      <div class="s-section__container container">
        <div class="s-section__row row">
          <div class="s-section__col col-12">
            <!-- Stepper progress -->
            <div class="c-stepper mb-3 mb-md-4">
              <div class="progress">
                <div class="progress-bar progress-bar-33" role="progressbar" aria-valuenow="33" aria-valuemin="0" aria-valuemax="100"></div>
              </div>
              <p><strong>Etape 1</strong>/3 : Nom de l'etape</p>
            </div>
          </div>
        </div>
        <div class="s-section__row row">
          <!-- Colonne formulaire (principale) -->
          <div class="s-section__col col-12 col-xxl-8 col-xxxl-9 order-2 order-xxl-1">
            <div class="c-form">
              <form method="post" class="js-prevent-multiple-submit">
                <fieldset>
                  <legend class="h3">Informations</legend>
                  <div class="form-group form-group-required">
                    <label class="form-label" for="id_field">Label</label>
                    <input type="text" name="field" class="form-control" required id="id_field">
                  </div>
                  <!-- Autres champs... -->
                  <div class="row">
                    <div class="col-12">
                      <hr class="mb-3">
                      <small class="d-inline-block mb-3">* champs obligatoires</small>
                      <div class="form-row align-items-center justify-content-end gx-3">
                        <div class="form-group col-12 col-lg order-3 order-lg-1">
                          <a href="" class="btn btn-link btn-ico ps-lg-0 w-100 w-lg-auto">
                            <i class="ri-close-line ri-lg" aria-hidden="true"></i>
                            <span>Annuler</span>
                          </a>
                        </div>
                        <div class="form-group col col-lg-auto order-2 order-lg-3">
                          <button type="submit" class="btn btn-block btn-primary">
                            <span>Suivant</span>
                          </button>
                        </div>
                      </div>
                    </div>
                  </div>
                </fieldset>
              </form>
            </div>
          </div>
          <!-- Colonne sidebar (info structure) -->
          <div class="s-section__col col-12 col-xxl-4 col-xxxl-3 order-1 order-xxl-2">
            <div class="c-box c-box--organization mb-3 mb-md-4">
              <button class="c-box--organization__summary w-100" type="button" data-bs-toggle="collapse" data-bs-target="#collapseBoxOrg" aria-expanded="true">
                <i class="ri-community-line" aria-hidden="true"></i>
                <div>
                  <span>TYPE</span>
                  <span class="d-block h3">Nom structure</span>
                </div>
              </button>
              <div class="c-box--organization__detail collapse show" id="collapseBoxOrg">
                <hr class="my-4">
                <ul class="c-box--organization__list-contact">
                  <li>
                    <i class="ri-map-pin-2-line fw-normal me-2" aria-hidden="true"></i>
                    <address class="m-0">Adresse complete</address>
                  </li>
                  <li>
                    <i class="ri-mail-line fw-normal me-2" aria-hidden="true"></i>
                    <a href="mailto:contact@example.com">contact@example.com</a>
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
  <!-- Scripts identiques -->
</body>
```

### Conventions des modeles

- **`body` sans classe** : page non-authentifiee, header `.s-header` avec logo ministere + logo service + nav
- **`body.l-authenticated`** : page authentifiee, header `.s-header-authenticated` avec logo service + dropdowns utilisateur/organisation + burger mobile
- **`body.p-home`** : page d'accueil (classe specifique pour styles homepage)
- **Header print** : `.s-header-print` present dans tous les templates, masque a l'ecran, visible a l'impression
- **Offcanvas navigation** : present dans toutes les pages authentifiees, contient nav mobile + dropups portail/utilisateur + footer legal
- **Footer 4 sections** : community → quick links → GIP plateforme → legal (pages non-auth uniquement ; les pages auth n'ont pas de footer visible)
- **Scripts en bas de `</body>`** : Popper.js 2.11.8 + Bootstrap 5.3.8 obligatoires ; jQuery 3.7.1 + Select2 4.0.13 si composants Select2 utilises

### Fichiers fournis avec ce skill

**Polices** (embarquees dans app.css via @font-face) :
- `fonts/marianne/` — Marianne Regular, Medium, Bold, ExtraBold + italiques (woff + woff2)
- `fonts/coveredbyyourgrace/` — Covered By Your Grace (woff + woff2)
- `fonts/remixicon/` — Remix Icon (eot, ttf, woff, woff2, svg, glyph.json)

**Images** (43 fichiers inclus) :
- `images/favicon.ico` — Favicon
- `images/logo-republique-francaise.svg` — Logo Republique Francaise (en-tete)
- `images/logo-emploi-inclusion.svg` — Logo principal du service
- `images/logo-emploi-inclusion-{light,dark,mono,simple}.svg` — Variantes logo
- `images/logo-plateforme-inclusion.svg` — Logo plateforme (pied de page GIP)
- `images/logo-{service}-*.svg` — Logos des sous-produits (dora, marche, pilotage, communaute, monrecap, inclusion-connect, etc.)
- `images/logo-beta-gouv.svg`, `logo-ministere-emploi.svg`, `logo-france-travail.svg` — Logos institutionnels

**Fichiers JS** :
- `javascripts/app.js` — JS du theme (infobulles, popovers, presse-papier, textareas extensibles, bascule mot de passe, alerte fermable une fois, impression, conseil)

---

## Liens et references

**Fichiers locaux (fournis avec ce skill)** :
- CSS compile : `stylesheets/app.css`
- JS du theme : `javascripts/app.js`
- Polices : `fonts/` (marianne, coveredbyyourgrace, remixicon)
- Logos : `images/` (43 logos et favicon)
- Modeles HTML : `modeles/` (22 pages de reference)

**Sources dans le repo** :
- Configurations SCSS : `src/stylesheets/base/_variables.scss`
- Composants personnalises : `src/stylesheets/components/`
- Architecture SCSS : `src/stylesheets/app.scss`
- Stories Storybook : `src/stories/`

**Liens externes** :
- Repo : https://github.com/gip-inclusion/itou-theme
- Storybook : https://gip-inclusion.github.io/itou-theme
- Version : itoutheme 3.6.3
