# 💎 SASS (SCSS) Cheat Sheet avec Explications

SASS (ou SCSS) est une extension puissante de CSS. Elle permet une écriture plus rapide, modulaire et organisée du style.

---

## Variables

Les variables permettent de stocker des valeurs (couleurs, tailles, etc.) réutilisables dans tout le code.

```scss
$primary-color: #f4c6c8;
$padding: 1rem;

.button {
  background-color: $primary-color;
  padding: $padding;
}
```

## Imbrication (Nesting)

Permet de garder une structure logique dans les sélecteurs CSS.
```scss
nav {
  ul {
    li {
      a {
        text-decoration: none;
        color: black;
      }
    }
  }
}
```
⚠️ Évite d’imbriquer trop profondément (max 3 niveaux).

## Importation de fichiers

Pour organiser ton code en plusieurs fichiers.
```scss
@import 'header'; // header.scss ou _header.scss
```
🔔 `@import` est obsolète, on préfère maintenant `@use` et `@forward` :

_colors.scss
```scss
$bg-color: #fff;
```
main.scss
```scss
@use 'colors';

body {
  background-color: colors.$bg-color;
}
```

 ## Mixins

Blocs de code réutilisables, avec ou sans paramètres.

```scss
@mixin btn($color) {
  background-color: $color;
  border-radius: 5px;
  padding: 10px 20px;
  color: white;
}

.button {
  @include btn(#f4c6c8);
}
```
si pas de paramètre, il est favorable d'utiliser `extend`

## Fonctions

Les fonctions retournent une valeur. Parfait pour les tailles, les calculs dynamiques, etc.
```scss
@function rem($px) {
  @return $px / 16 * 1rem;
}

.title {
  font-size: rem(32); // = 2rem
}
```

 ## Extend (%placeholder)

Réutilise des blocs de styles sans répéter le code :
```scss
%card {
  border: 1px solid #ddd;
  padding: 1rem;
  border-radius: 10px;
}

.product {
  @extend %card;
  background-color: #fff;
}
```

## Media Queries imbriquées

Les __media queries imbriquées__ permettent d’intégrer directement __les règles CSS responsive__ dans le bloc du composant concerné, __au lieu de les écrire séparément__ comme en CSS classique.

```scss
.container {
  padding: 1rem;

  @media (min-width: 768px) {
    padding: 2rem;
  }
}
```