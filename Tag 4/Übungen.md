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
# Map und Filter
## Übung 1
```Java
mitarbeiterList.filter(mitarbeiter -> mitarbeiter.gehalt >= 50000).map(mitarbeiter -> mitarbeiter.name.split(" ")[0].toUpperCase)
```
## Übung 2
```Java
kurse.filter(kurs -> kurs.includes("daten").map(kurs -> kurs.replace(" ", "")).sorted()
kurse.filter(kurs -> kurs.includes("daten").map(kurs -> kurs.replace(" ", "")).sort((a, b) -> b.compareTo(a))
```
# foldLeft
## Übung 1
```Java
numbers.foldLeft(0)((sum, x) -> sum + x)
```
## Übung 2
```Java
strings.foldLeft("")((combined, x) -> combined + x)
```
## Übung 3
```Java
val n = points.size
val (sumX, sumY) = points.foldLeft((0, 0)) { case ((sx, sy), (x, y)) =>
  (sx + x, sy + y)
}
val center = (sumX.toDouble / n, sumY.toDouble / n)
```
# FlatMap
## Übung 1
```Java
numbers.flatmap(number -> number).map(number -> number * 2)
```
## Übung 2
```Java
list.flatMap(element -> element.color).distinct()
```
# For Comprehensions
## Übung 1
```Scala
val function = for {
n <- numbers
} yield n * n
```
## Übung 2
```Scala
val function = for {
n <- numbers
if n % 2 == 0
} yield n
```
## Übung 3
```Scala
val combinations = for {
x <- list1
y <- list2
} yield (x, y)
```
## Übung 4
```Scala
val pendingTasks = for {
x <- user
y <- user.tasks
if !tasksCompleted.contains(y)
} yield (x, y)
```
