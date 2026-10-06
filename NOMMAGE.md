# NOMMAGE : conventions du projet Résonances

## 1. Règles générales

- **Méthode** : BEM, `bloc__element--modificateur`.
- **Langue des noms** : anglais, en minuscules, mots séparés par des tirets (`btn`, `form-field`).
- **Documentation** : en français.
- **Pas d'identifiants** : aucun sélecteur `#id` (les `id` servent au JavaScript et aux ancres).
- **JavaScript** : il cible uniquement des attributs `data-*` (ex. `data-filter`), jamais des classes de style.

## 2. Préfixes

| Catégorie SMACSS | Préfixe | Exemple |
|---|---|---|
| Mise en page (layout) | `l-` | `l-header`, `l-footer`, `l-container` |
| Composants (modules) | aucun | `btn`, `card`, `badge` |
| États (state) | `is-` / `has-` | `is-active`, `is-open`, `has-error` |
| Thèmes (theme) | `theme-` | `theme-lac`, `theme-foret`, `theme-kiosque`, `theme-dark` |

## 3. Jetons de conception

- Variables et maps Sass dans `scss/abstracts/_variables.scss`.
- Propriétés personnalisées sur `:root`, nommées `--categorie-role` : `--color-primary`, `--font-size-m`, `--spacing-s`, `--radius-small`.
- Les noms décrivent le **rôle** (`primary`, `border-field`), jamais la valeur (`red`).

## 4. Inventaire des composants (modules)

| Bloc | Rôle | Éléments | Modificateurs | Pages |
|---|---|---|---|---|
| `btn` | Bouton d'action | `btn__icon` | `btn--primary`, `btn--secondary`, `btn--small` | toutes |
| `badge` | Pastille d'information (scène, statut) | | `badge--lac`, `badge--foret`, `badge--kiosque` | accueil, programme, artiste |
| `card` | Carte d'artiste | `card__image`, `card__body`, `card__title`, `card__meta` | `card--featured` | accueil, artiste |
| `pass` | Carte de formule de billet | `pass__title`, `pass__price`, `pass__list` | `pass--highlight` | billetterie |
| `concert` | Ligne de concert du programme | `concert__time`, `concert__artist`, `concert__stage` | | programme |
| `form-field` | Champ de formulaire avec libellé | `form-field__label`, `form-field__input`, `form-field__error` | `form-field--error` | billetterie |
| `filter` | Filtre par scène | `filter__item` | | programme |
| `faq` | Question fréquente repliable | `faq__question`, `faq__answer` | | infos |
| `banner` | Bandeau d'information ou bannière | `banner__title`, `banner__text` | `banner--hero`, `banner--info` | accueil, infos |

## 5. Zones de mise en page (layout)

| Bloc | Rôle | Pages |
|---|---|---|
| `l-header` | En-tête et navigation | toutes |
| `l-footer` | Pied de page | toutes |
| `l-container` | Conteneur centré à largeur maximale | toutes |
| `l-grid` | Grille de cartes et du programme | accueil, programme, artiste |
| `l-doc` | Mise en page de la page `composants.html` | composants |

## 6. États

| Classe | Utilisation |
|---|---|
| `is-active` | élément sélectionné (filtre actif) |
| `is-open` | élément déplié (question de la FAQ) |
| `is-disabled` | élément désactivé |
| `has-error` | champ ou formulaire en erreur |

## 7. Thèmes

| Classe | Utilisation |
|---|---|
| `theme-lac` | Scène du Lac, bleu profond |
| `theme-foret` | Scène de la Forêt, vert sapin |
| `theme-kiosque` | Le Kiosque, ocre |
| `theme-dark` | mode sombre |

## 8. Historique

- Étape 1 : inventaire initial des composants et des préfixes.
- Étape 2 : ajout des jetons de conception et de la page `composants.html` (bloc `l-doc`).