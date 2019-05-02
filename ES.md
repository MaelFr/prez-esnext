<!-- $theme: gaia -->

ES.Next
===

---
<!-- template: invert -->

# C'est quoi ES ?

- **ECMA Script** ou ECMA-262
- ECMA: European Computer Manufacturers Association
- JavaScript, ActionScript, V8, ...
- Orienté **prototype**

---
<!-- template: default -->

# Un peu d'histoire

- 1995: création par Brendan Eich
- juin 1997: première version standardisée ECMA
- 1999: troisième version
- 2009: version suivante... la cinquième
- juin 2015: ES6 :heart: :heart_eyes:
- juin X: ES(X-2009)

---
<!-- template: gaia -->

# ES6
##### (R)évolution
###### et officiellement c'est ECMAScript 2015

---
<!-- template: default -->

# ES 2015
### Arrows
```js
v => v + 1

(v, i) => v + i

v => {
  if (typeof v === 'number') {
  	numbers.push(v);
  }
}
```

---

# ES 2015
### Classes


```js
class Car extends Vehicle {
  constructor(brand, name, price) {
    super(brand, name, price);
    ...
  }
}
```

---

# ES 2015
### Object literals


```js
// Todo
```

---

# ES 2015
### Template strings


```js
let myVar = "ma variable"
function myFunction(){
  return "ma fonction"
} 

let myString = `
  Les littéraux de gabarits permettent d'utiliser des chaînes de caractères multi-lignes.
  Aussi, on peut afficher la valeur d'une variable de cette manière:
  ${myVar}
  On peut de la même façon afficher toute sorte d'expression, comme des retours de fonctions:
  ${myFunction()}
`
```

---

# ES 2015
### Destructuring


```js
[firstname, lastname, password] = ["Clark", "Kent", "azerty"]
({firstname, lastname, password} = {firstname: "Kal", lastname: "El", password: "012345"})
```

---

# ES 2015
### Let


```js
function fn() {
  let variableLet = "permier let";
  var variableVar = "premier var";
  if (true) {
    let variableLet; 
    var variableVar;
    
    variableLet = "second let";
    variableVar = "second var";

    console.log(variableLet); // second let
    
    console.log(variableVar); // second var
  }
  console.log(variableLet); // premier let
  
  console.log(variableVar); // second var
}
```
### Const
```js
function fn(){
  const myConst; // erreur, constante doit être initialisée
  const myConst = "ma constante"
  
  myConst = "modif" // erreur, la constante ne peut être réaffectée

  if(myConst === "ma constante"){
    let myConst = "modif let"

    var myConst = "modif var" // erreur, la variable est déjà déclarée
  }
}
```
---

# ES 2015
### Modules


```js
// Todo
```


---

# ES 2015
### Module loaders


```js
// Todo
```

---

# ES 2015
### Map, Set


```js
// Todo
```

---

# ES 2015
### Promises


```js
// Todo
```

---

# ES 2015
#### Mais aussi
// Todo

---

# ES 2016
- Array.includes()
- `7**2` raccourci `Math.pow(7, 2)`

---

# ES 2017
- **async/await** :fire:
- Object.values() && Object.entries()
- String.pad{Start,End}

---

# ES 2017
#### Async/Await

```js
// ES 2015
function doTheJob(id) {
  getUser(id)
      .then(runALongProcess)
      .then(result => {
        console.log(result);
      })
}

// ES 2017
asyncv function doTheJob(id) {
  const user = await getUser(id);
  const result = await runALongProcess(user);
  console.log(result);
}

```

---

# ES 2018
- Object rest/spread operator
- Promise.finally
- Boucles asynchrones
- RegExp: groupes de captures nommés

---

# ES... Next ?
TC39
[Proposals](https://github.com/tc39/proposals)
Stages
Feature doit être dans la dernière étape au 1er février, sinon passe l'année suivante
- 4 (Finished): Spec complète et 2 implémentations réelles
- 3 (Candidate): Spec complète, doit être implémenté
- 2 (Draft): Formaliser les specs
- 1 (Proposal): A un "Champion", Identifie un problème et propose une solution, Specs en cours d'écriture
- 0 (Strawman): Spec à la louche, attente de feedback 

---

# ES.Next
Optional catch binding (stage 4)
[Static class features](https://github.com/tc39/proposal-static-class-features/) (stage 3)
[Private methods](https://github.com/tc39/proposal-private-methods) (stage 3)
[Optional Chaining](https://github.com/tc39/proposal-optional-chaining) (stage 1)

---

# ES.Next
#### On peut déjà en utiliser certaines
Babel, TS

---
# Sources
- [ES6 sur Wikipédia](https://en.wikipedia.org/wiki/ECMAScript)
- [medium.freecodecamp.org/here-are-examples-of-everything-new-in-ecmascript-2016-2017-and-2018](https://medium.freecodecamp.org/here-are-examples-of-everything-new-in-ecmascript-2016-2017-and-2018-d52fa3b5a70e)
- [GitHub TC39](https://github.com/tc39)
- ["ES Next Features That'll Make You Dance" by Ben Ilegbodu at Node Summit 2018](https://www.youtube.com/watch?v=9yK4t2CuIHQ)