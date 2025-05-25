# Javacript

## les boucles

| Partie           | Nom              | Rôle                                                        | Exemple         |
|------------------|------------------|-------------------------------------------------------------|-----------------|
| `let i = 0`      | Initialisation   | Déclare et initialise la variable de boucle                 | `let i = 0`     |
| `i <= 10`        | Condition        | Définit si la boucle doit continuer (tant que c'est vrai)   | `i <= 10`       |
| `i++`            | Mise à jour      | Modifie la variable à chaque tour (le **pas** de la boucle) | `i++`           |

### While
- Si la condition est fausse dès le début, le bloc ne s’exécute pas du tout sinon s'arrête des qu'elle devient fausse.
```js
let i = 0 ;
while (i <=10){
    console.log ("le chiffre est" +i);
    i++;
}
```
### do while 

 - Le bloc s’exécute au moins une fois, même si la condition est fausse dès le départ.

-  La condition est testée après l’exécution du bloc.


```js
let i= 0;
do {
    console.log  ("le chiffre est" +i);
    i++
} while(i<=20)
```
### for
- Elle est idéale quand on sait à l'avance combien de fois on veut boucler.

```js
for (let i = 0 ; i<=15 ; i++) {
console.log ("le chiffre est" +i);
}
```
## fonctions
```js
function nomdemafonction (parametre1 , parametre2){
  console.log ('bonjour');
}
nomdemafonction();
```
#### exemple avec parametre :

```js
function aircarre(cote) {
    let air = cote * cote
    return air
}
let airdemoncarre = aircarre(5)
console.log(airdemoncarre)
```

### fonction avec variable externe

```js
let nom = 'Nicolas' ; 
function nomdemafonction() {
    let message = 'bonjour, '+ nom;
    console.log(message)
}
nomdemafonction();
```
### fonction avec variable interne

La variable sera qu'utilisable dans ma fonction
```js
function nomdemafonction() {
    let nom = 'Nicolas';
    let message = 'Bonjour,' + nom;
    console.log(message)
}
nomdemafonction();
```
### fonction expression 

une fonction expression est souvent définie dans une variable ou constante

```js
const multiplier = function(a, b) {
  return a * b;
};

console.log(multiplier(5, 10)); // Affiche 50
```
### fonction arrow
```js
const addition = (a, b) => a * b;

console.log(addition(5, 10)); // Affiche 50
```

## Variables et Constantes

### Variable

```js
let age = '19 ans'
let nom = 'Lafuente'
let message = 'Bonjour'
```

### Constantes

Une constante ne peut __jamais__ être réassignée après sa déclaration. Une fois une valeur assignée à une constante, tu ne peux pas changer cette valeur.

```js
const nom = 'Lafuente';
console.log(nom); // Affiche Lafuente
nom = 'Dupont'; // Erreur ! Impossible de réassigner une constante
```

## Objets

```js
let utilisateur = {
  nom: "Lafuente",
  prenom: "Nicolas",
  age: 19
};
console.log(utilisateur); 
```
Ne surtout pas oublier les `,`

résultat :

```js
[object Object] {
  age: 25,
  nom: "Lafuente",
  prenom: "Nicolas"
}
```
## This

En utilisant this, tu peux accéder aux propriétés et méthodes d'un objet sans avoir à répéter le nom de l'objet chaque fois. Cela rend le code plus concis et réutilisable.

Exemple :
```js
const voiture = {
  marque: 'Toyota',
  modele: 'Corolla',
  annee: 2021,
  afficherDetails: function() {
    console.log('Marque: ' + this.marque); // 'this' fait référence à l'objet 'voiture'
    console.log('Modèle: ' + this.modele);
    console.log('Année: ' + this.annee);
  }
};

voiture.afficherDetails();
```

Ici, `this.marque`, `this.modele` et `this.annee` font référence aux propriétés de l'objet voiture, ce qui te permet d'afficher facilement ces informations à partir de la méthode afficherDetails.

## Tableau 

### Créer un tableau 

```js
let nombres = new Array(1, 2, 3, 4);
```
### Créer un tableau vide puis ajouter des éléments

```js
let animaux = [];
animaux.push('chat');
animaux.push('chien');
```
## Opérateurs de comparaison

| Opérateur | Signification                  | Exemple             | Résultat (si x = 5, y = 10) |
|-----------|--------------------------------|---------------------|-----------------------------|
| `===`      | Égal à                         | `x === y`            | `false`                     |
| `!=`      | Différent de                   | `x != y`            | `true`                      |
| `>`       | Supérieur à                    | `y > x`             | `true`                      |
| `<`       | Inférieur à                    | `x < y`             | `true`                      |
| `>=`      | Supérieur ou égal à            | `x >= 5`            | `true`                      |
| `<=`      | Inférieur ou égal à            | `y <= 5`            | `false`                     |

## Opérateurs logiques 

| Opérateur | Nom         | Signification                        | Exemple                          | Résultat                         |
|-----------|-------------|--------------------------------------|----------------------------------|----------------------------------|
| `&&`      | ET logique  | Vrai si les 2 conditions sont vraies | `x > 0 && y > 0`                 | `true` si x=5, y=10              |
| `||`     | OU logique  | Vrai si **au moins une** est vraie   | `x < 0 || y > 0`                 | `true`                           |
| `!`       | NON logique | Inverse une condition                | `!(x == 5)`                      | `false`                          |


#  Cheat Sheet DOM JavaScript avec Exemples

##  Sélection d’éléments

###  Par ID
HTML :
```html
<p id="titre">Bonjour</p>
```
JS :
```js
const titre = document.getElementById('titre');
console.log(titre.textContent); // Bonjour
```

###  Par classe
HTML :
```html
<p class="texte">Texte 1</p>
<p class="texte">Texte 2</p>
```
JS :
```js
const textes = document.getElementsByClassName('texte');
console.log(textes[0].textContent); // Texte 1
```

###  Par balise
HTML :
```html
<div>Zone 1</div>
<div>Zone 2</div>
```
JS :
```js
const zones = document.getElementsByTagName('div');
console.log(zones.length); // 2
```
