# Map
## Übung 1
```Java
numbers.map(number -> number * 2)
```
## Übung 2
```Java
names.map(name -> name.toUpperCase)
```
## Übung 3
```Java
numbers.map(number -> number / 2)
```
## Übung 4
```Java
addresses.map(address -> address.strasse + " " + address.hausnummer + ", " + address.postleitzahl + " " + address.stadt)
```
## Übung 5
```Java
names.map(name -> name.split(" ")[0].toUpperCase)
```
# Filter
## Übung 1
```Java
numbers.filter(number -> number % 2 == 0)
```
## Übung 2
```Java
names.filter(name -> name.length > 4)
```
## Übung 3
```Java
numbers.filter(number -> number > 50)
```
## Übung 4
```Java
words.filter(word -> word.chatAt(0) == 'S')
```
## Übung 5
```Java
books.filter(book -> book.jahr < 1950).map(book -> book.titel)
```
