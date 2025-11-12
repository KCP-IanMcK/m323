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

# Aufgabe 2
```Java
public class ShoppingCart {
    boolean bookAdded = false;
    List<String> items = new ArrayList<>();

    public void addItem(String item) {
        items.add(item);
        if (item.equals("Book")) {
            bookAdded = true;
        }
    }

    public void removeItem(String item) {
        for (int i = 0; i < items.size(); i++) {
            if (items.get(i).equals(item)) {
                items.remove(i);
                break;
            }
        }
        bookAdded = false;
        for (String s : items) {
            if (s.equals("Book")) {
                bookAdded = true;
            }
        }
    }

    public List<String> getItems() {
        return items;
    }
    
    public int getDiscount() {
        if (bookAdded) {
            return 5;
        } else {
            return 0;
        }
    }
}
```
```Java
public int getDiscountPercentage(List<String> shoppingCart) {
        for (String s : shoppingCart) {
            if (s.equals("Book")) {
                return 5;
            }
        }
        return 0;
    }
```
