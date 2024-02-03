# Übung 1

## Aufgabe

In dieser Übung sollt ihr ein einfacher REST-Service erstellt werden. Das Service soll die Ressource "Task" verwalten. Eine Task hat folgende Eigenschaften:

- id: Long
- description: String
- isCompleted: Boolean
- maxEffortHrs: Effort

Das Enum Effort hat folgende Werte:

- ONE_HOUR(1)
- TWO_HOURS(2)
- FOUR_HOURS(4)

Wir brauchen ein Package `onsite.academy.myworkday.model` und ein weiteres Package `onsite.academy.myworkday.controller`.

## Vorbereitung

- Forked das Repository oder downloaded den Code "https://"
- Öffnet das Projekt in einer IDE (z.B. IntelliJ IDEA)
- Baut das Projekt mit gradle `./gradlew build` oder `gradlew.bat build` (Windows) bzw. mit der Gradle-View in IntelliJ IDEA

## Experimente

- Legt die Datei für die Klasse Task an. Löscht die Klassendefinition. Direkt unterhalb der Package-Deklaration startet ihr einen Kommentar wie unten sichtbar. Was passiert?
```
package onsite.academy.myworkday.model;
// Task 
```
- Verwerft den Vorschlag mit Esc oder löscht den generierten Code. Erstellt einen Kommentarblock mit folgendem Inhalt. Was passiert nachdem ihr den Kommentarblock geschlossen habt?
```
/*
Eine Task hat folgende Eigenschaften:

- id: Long
- description: String
- isCompleted: Boolean
- maxEffortHrs: Effort

 */
```

- Legt die Klasse TaskController an. Löscht die Klassendefinition. Experimentiert mit präzisens Top-Level Kommentaren. Beispiel:

```
// Spring-Boot Controller
```

## Ergebnisse

- Für das Fachobjekt "Task" wurden REST-Endpunkte implementiert. Die Endpunkte sind unter `/tasks` erreichbar.
- Die HTTP GET-Methode gibt eine (fest verdratete) Liste aller Tasks zurück. Testet das mit dem Http-Client von IntelliJ IDEA oder mit einem Browser.
- Die anderen Methoden sind noch nicht ausimplementiert, die Restendpunkte sind aber schon vorhanden.
