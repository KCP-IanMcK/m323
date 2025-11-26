# Aufgabe 1
| Aufgabe | Nur ein Rückgabewert | Resultat nur abhängig von Parametern | Verändert keine existierenden Werte | pure oder impure |
|--------|------------------------|---------------------------------------|--------------------------------------|-------------------|
| 1.1    | Ja                     | Ja                                  | Nein                                   | impure            |
| 1.2    | Ja                     | Ja                                    | Ja                                   | pure              |
| 1.3    | Ja                     | Ja                                    | Ja                                   | pure              |
| 1.4    | Ja                     | Nein                                    | Ja                                   | impure              |
| 1.5    | Ja                     | Ja                                    | Ja                                   | pure              |
| 1.6    | Nein                     | Ja                                    | Ja                                   | impure              |

# Aufgabe 2
## 2.1
```JavaScript
let cartItems = [];

function addToCart(item, cartItems) {
let newCart = cartItems;
    newCart.push(item);
    return newCart;
}

```
## 2.2
```JavaScript
function multiplyWithRandom(number, randomValue) {
    return number * randomValue;
}

console.log(multiplyWithRandom(number, Math.random());
```
Da bei einer pure function der gleiche Eingabewert auch immer den gleichen Ausgabewert geben muss, kann man den randomValue nicht direkt in der Funtktion erzeugen.
## 2.3
```JavaScript
function printAndReturnString(str) {
    return str;
}

console.log(printAndReturnString(str);
```
Da per Definition eine Funktion impure ist, wenn sie einen console.log macht, muss dieser ausserhalb der Funktion geschehen.
# Aufgabe 3
## 3.1
```JavaScript
function getSum(list) {
    let listCopy = [...list];
    if (listCopy.length == 0) {
        return 0;
    }
    let lastNumber = listCopy.pop();
    return lastNumber + getSum(listCopy);
}
```
## 3.2
```JavaScript
function getMittelwert(list) {
    if (list.length === 0) return 0;
    return getSum(list) / list.length;
}

function getMittelwert(list) {
    return getSum(list) / list.length;
}
```
## 3.3
```JavaScript
function sortList(stringList) {
    let listCopy = [...stringList];
    let sorted = true; 
    for (let i = 0; i < listCopy.length - 1; i++) {
        if (listCopy[i].localeCompare(listCopy[i + 1]) > 0) {
            let tempVar = listCopy[i];
            listCopy[i] = listCopy[i + 1];
            listCopy[i + 1] = tempVar;
            sorted = false;
        }
    }
    if (sorted) {
        return listCopy;
    }
    return sortList(listCopy);
}
```
## 3.4
```JavaScript



```
