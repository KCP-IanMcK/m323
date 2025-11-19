# Aufgabe 1
addDestinationToRoute(Destination, Destination[], Position): Destination[]  -> Destination[] = Route
```Java
public List<Destination> addDestinationToRoute(Destination destination, List<Destination> route, int position) {
        List<Destination> routeToReturn = new ArrayList<>(route);
        routeToReturn.add(position, destination);
        return routeToReturn;
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
        List<Double> valuedRounds = new ArrayList<>(times);
        valuedRounds.removeFirst();
        double accumulatedRoundTime = 0;
        for (Double time : valuedRounds) {
            accumulatedRoundTime += time;
        }
        return accumulatedRoundTime;
    }

public static double calculateAverageRoundTime(List<Double> times) {
        double allRoundTimesAccumulated = getAccumulatedRoundTime(times);
        return allRoundTimesAccumulated / (times.size() - 1);
    }
```
