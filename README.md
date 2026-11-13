# README de rendu — Site vitrine d'un événement

## Groupe

| | |
|---|---|
| Nom du groupe | sous-sol |
| Membres (et rôle référent) | NOM Prénom — travail individuel, les trois rôles |
| Événement / thème | Festival de musique : « SOUS-SOL », festival de rap underground |
| Lien du dépôt Git | https://github.com/Tomlzzzzz/PROJET-CSS-TS |
| Convention de nommage | BEM : `.bloc`, `.bloc__element`, `.bloc--variante` ; utilitaires préfixés `u-` |

## Localisation des exigences

| Exigence | Élément attendu | Fichier:ligne | Commentaire (ce que ça fait, pourquoi) |
|---|---|---|---|
| 1. Architecture | Déclaration de l'ordre des `@layer` | `css/main.css:3` | Déclaré une seule fois, avant les imports. |
| 1. Architecture | Tokens primitifs | `css/tokens.css:5` | Palette, espacements, rayons, durées. |
| 1. Architecture | Tokens sémantiques | `css/tokens.css:47` | Seuls tokens utilisés par les composants. |
| 1. Architecture | Nesting natif (exemple représentatif) | `css/components.css:104` | `.btn` avec `&:hover`, `&:active`. |
| 2. Mise en page | `grid-template-areas` (mobile → desktop) | `css/layout.css:48` | Hero : le visuel passe à droite en desktop. Aussi le programme `css/layout.css:74`. |
| 2. Mise en page | `subgrid` | `css/layout.css:111` | Cartes artistes : nom, bio et lien alignés. Aussi les créneaux `css/components.css:236`. |
| 2. Mise en page | Flexbox pour un composant | `css/components.css:40` | Navigation avec `flex-wrap` et `gap`. Raccourci `flex` `css/components.css:172`. |
| 3. Responsive | Première media query mobile-first | `css/layout.css:40` | `@media (width >= 48rem)`. |
| 3. Responsive | Typographie fluide `clamp()` | `css/tokens.css:68` | Échelle de tailles dans les tokens. |
| 3. Responsive | Container query (`container-type` + `@container`) et ses 2 contextes | `css/layout.css:136` + `css/components.css:335` | Carte horizontale (tête d'affiche) ou verticale (révélation), côte à côte. |
| 3. Responsive | Test 320 px sans défilement horizontal (correctif principal) | `css/reset.css:37` | `overflow-wrap: break-word`. |
| 4. Sélecteurs | `:has()` pertinent | `css/components.css:369` | L'offre qui contient un badge est mise en avant. |
| 4. Sélecteurs | `:is()` / `:where()` | `css/base.css:19` | Titres à spécificité nulle. |
| 5. Thème | `light-dark()` / `prefers-color-scheme` + `color-scheme` | `css/tokens.css:48` | Couleurs sémantiques en `light-dark()`. |
| 5. Thème (bonus technique) | Bascule CSS-only | `css/tokens.css:124` | La case change `color-scheme`. |
| 6. Animations | Transition n°1 | `css/components.css:118` | Bouton : `translate` et `box-shadow`. |
| 6. Animations | Transition n°2 | `css/components.css:276` | Carte : `translate` et `box-shadow`. |
| 6. Animations | `@keyframes` | `css/components.css:483` | Apparition du titre du hero. |
| 6. Animations | `prefers-reduced-motion` | `css/utilities.css:14` | Coupe toutes les animations et transitions. |
| 6. Animations (bonus technique) | Scroll-driven (`@supports`), View Transitions, `@starting-style`/popover… | `css/components.css:506` | Apparition au scroll, ignorée par Firefox. |
| 7. Accessibilité | Landmarks + hiérarchie de titres | `index.html:19` | `header`, `nav`, `main`, `footer`, un seul `h1`. |
| 7. Accessibilité | `:focus-visible` | `css/base.css:60` | Contour de 3 px sur tous les éléments interactifs. |
| 7. Accessibilité | Contrastes AA vérifiés (outil + paires de couleurs testées, 2 thèmes) | `css/tokens.css:50` | Clair : texte/fond 16,2:1, texte atténué 6,3:1. Sombre : texte/fond 17,2:1, lien jaune 12,3:1. Texte sur jaune 13,0:1, blanc sur rouge 6,1:1. |
| 7. Accessibilité | Images avec `alt` | `index.html:138` | « Portrait dessiné de … ». |
| 8. Qualité | Résultat du validateur W3C | — | |
| 8. Qualité | `!important` (aucun, ou utilitaire justifié) | — | Aucun. |

## Avertissements du validateur W3C non corrigés

| Fichier:ligne | Message du validateur | Pourquoi c'est valide |
|---|---|---|
| | | |

## Bonus technique revendiqué

| Fonctionnalité | Fichier:ligne | Explication (et repli prévu pour les navigateurs qui ne la gèrent pas) |
|---|---|---|
| Bascule de thème CSS-only | `css/tokens.css:124` | `:root:has(#theme-toggle:checked)` change `color-scheme`. |
| Animation au scroll | `css/components.css:506` | Dans `@supports` : sans prise en charge (Firefox), le contenu reste visible. |

## JavaScript (facultatif, ≤ 20 lignes)

Aucun.

## Déclaration d'usage d'outils d'IA

| Outil | Pour quoi faire (textes, explication d'une erreur, revue…) | Parties du code concernées |
|---|---|---|
| Claude (Anthropic) | Choix du thème, génération du code, textes fictifs, correction d'un bug de subgrid, calcul des contrastes, README | `index.html`, `css/`, `README.md` |
| DiceBear | Génération des portraits des artistes | Images des cartes |

## Qui a fait quoi

| Membre | Principales contributions |
|---|---|
| NOM Prénom | Travail individuel : tout le projet, avec l'IA déclarée ci-dessus |

## Crédits

- Police Anton (Vernon Adams), licence SIL OFL, Google Fonts.
- Portraits : DiceBear, style Notionists (Zoish), licence CC0.
