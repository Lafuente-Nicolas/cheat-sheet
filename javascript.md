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