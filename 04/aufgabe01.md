übung 1
```
List<Integer> zahlen = Array.asList(1, 2, 3, 4, 5);
List<Integer> verdoppelt = zahlen.stream().map(n -> n*2).collect(Collectors.toList());
```
übung 2
```
List<String> namen = Arrays.asList("Alice", "Bob", "Charlie");
List<String> grossbuchstaben = namen.stream().map(String::toUpperCase).collect(Collectors.toList());
```
übung 3
```
List<Double> zahlen = Arrays.asList(12.0, 45.0, 68.0, 100.0);
List<Double> halbiert = zahlen2.stream().map(n -> n * 0.5).collect(Collectors.toList());
```
übung 4
```
List<Adresse> adressen = Arrays.asList(
            new Adresse("Hauptstrasse", 10, "12345", "Musterstadt"),
            new Adresse("Nebenstrasse", 5, "23456", "Beispielburg")
        );

List<String> formatierteAdressen = adressen.stream().map(a -> a.getStrasse() + " " + a.getHausnummer() + ", " + a.getPostleitzahl() + " " + a.getStadt()).collect(Collectors.toList());
```
übung 5 
```
List<String> namen = Arrays.asList("Max Mustermann", "Erika Mustermann");
List<String> grossVornamen = namen.stream().map(n -> n.split(" ")[0].toUpperCase()).collect(Collectors.toList());
```
