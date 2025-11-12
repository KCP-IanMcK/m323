# Aufgabe 1
Imperativ:
```Java
public static int calculateScore(String word) {
        int score = 0;
        for (char c : word.toCharArray()) {
            if (c != 'a') {
                score++;
            }
        }
        return score;
    }
```

Deklarativ:
```Java
public static int wordScore(String word) {
        word = word.replaceAll("a", "");
        return word.length();
    }
```
