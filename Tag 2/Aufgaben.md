# Aufgabe 1
addDestinationToRoute(Destination, Destination[], Position): Destination[]  -> Destination[] = Route
```Java
public List<Destination> addDestinationToRoute(Destination destination, List<Destination> route, int position) {
        return Stream.concat(
                Stream.concat(route.stream().limit(position), Stream.of(destination))
                , route.stream().skip(position)
        ).toList();
    }
```

# Aufgabe 2
getWordPoints(Word): int
evaluateWords(Word[]): RankingList
```Java
public int getWordPoints(String word) {
        return (int) word.chars().filter(c -> c != 'a').count();
    }

public static List<String> evaluateWords(List<String> words) {
        return words.stream().sorted(Comparator.comparingInt(Main::getWordPoints).reversed()).toList();
    }
```
# Aufgabe 3
getAccumulatedRoundTime(Time[]): Time
calculateAverageRoundTime(Time[]): Time
```Java
public static double getAccumulatedRoundTime(List<Double> times) {
        return times.stream()
                .skip(1)
                .mapToDouble(Double::doubleValue)
                .sum();
    }

public static double calculateAverageRoundTime(List<Double> times) {
        return times.stream()
                .skip(1)
                .mapToDouble(Double::doubleValue)
                .average()
                .orElse(0);
    }
```
