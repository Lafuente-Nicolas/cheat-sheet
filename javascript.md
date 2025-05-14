# Javacript


| Partie           | Nom              | Rôle                                                        | Exemple         |
|------------------|------------------|-------------------------------------------------------------|-----------------|
| `let i = 0`      | Initialisation   | Déclare et initialise la variable de boucle                 | `let i = 0`     |
| `i <= 10`        | Condition        | Définit si la boucle doit continuer (tant que c'est vrai)   | `i <= 10`       |
| `i++`            | Mise à jour      | Modifie la variable à chaque tour (le **pas** de la boucle) | `i++`           |

## While

```js
let i = 0 ;
while (i <=10){
    console.log ("le chiffre est" +i);
    i++;
}
```
## do while 

```js
let i= 0;
do {
    console.log  ("le chiffre est" +i);
    i++
} while(i<=20)
```
## for

```js
for (let i = 0 ; i<=15 ; i++) {
console.log ("le chiffre est" +i);
}
```
## fonction 
```js
function nomdemafonction (parametre1 , parametre2){
  console.log ('bonjour');
}
nomdemafonction();
```

## fonction avec variable externe

```js
let nom = 'Nicolas' ; 
function nomdemafonction() {
    let message = 'bonjour, '+ nom;
    console.log(message)
}
nomdemafonction();
```
## fonction avec variable interne

La variable sera qu'utilisable dans ma fonction
```js
function nomdemafonction() {
    let nom = 'Nicolas';
    let message = 'Bonjour,' + nom;
    console.log(message)
}
nomdemafonction();
```
