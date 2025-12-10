# Übungen zu Map
## Aufgabe 1
```Scala
val m1: Map[String, String] =
Map(("key") -> ("value"));

```
## Aufgabe 2
```Scala
val m1: Map[String, String] =
Map(("key1") -> ("value1"));
m1.update("key2", "value2");
```

## Aufgabe 3
```Scala
val m1: Map[String, String] =
Map(("key1") -> ("value1"));
m1.update("key2", "value2");
m1.update("key2", "anotherValue");
```

## Aufgabe 4
```Scala
val m1: Map[String, String] =
Map(("key1") -> ("value1"));
m1.removed("key1", "value1");
```

## Aufgabe 5
```Scala
val m3: Map[String, String] =
Map(("key1") -> ("value1"));
val valueFromM3: Option[String] = m3.get("key1");
```

## Aufgabe 6
```Scala
val m3: Map[String, String] =
Map(("key1") -> ("value1"));
val valueFromM3: Option[String] = m3.get("key2");
```

# Übungen zu Tupel
## Aufgabe 1
```Scala
val getWeather: () => (String, LocalDate, Double) =
  () => ("sonnig", LocalDate.now(), 12.5)
```

## Aufgabe 2
```Scala
val t1: (String, Double) = [("sonnig", 12.5), ("regnerisch", 10.2), ("sonnig", 21.5)];
val getWeatherAbove: (Double, List[(String, Double)]) => List[(String, Double)] = (temperature, list) => list.filter(item => item._2 > temperature);
```
