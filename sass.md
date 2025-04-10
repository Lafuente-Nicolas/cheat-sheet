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
