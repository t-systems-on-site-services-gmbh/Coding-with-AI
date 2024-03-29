# Übung 1

## Aufgabe

In dieser Übung soll ein einfacher REST-Service erstellt werden. Das Service soll die Ressource "Task" verwalten. Eine Task hat folgende Eigenschaften:

- id: Long
- description: String
- isCompleted: Boolean
- maxEffortHrs: Effort

Das Enum Effort hat folgende Werte:

- ONE_HOUR(1)
- TWO_HOURS(2)
- FOUR_HOURS(4)

## Erste Schritte

- Repository forken oder den Code downloaden: https://github.com/t-systems-on-site-services-gmbh/MyWorkday/tree/main
- Öffnet das Projekt in einer IDE (z.B. IntelliJ IDEA)
- Wir brauchen ein Package `onsite.academy.myworkday.model` und ein weiteres Package `onsite.academy.myworkday.controller`.
- Baut das Projekt mit gradle `./gradlew build` oder `gradlew.bat build` (Windows) bzw. mit der Gradle-View in IntelliJ IDEA

## Experimente

### Eine Datenklasse und ein Enum

- Legt die Datei für die Klasse `Task` im Package im Package `onsite.academy.myworkday.model` an. Löscht die Klassendefinition. Direkt unterhalb der Package-Deklaration startet ihr einen Kommentar wie unten sichtbar. Was passiert?

```
package onsite.academy.myworkday.model;
// Task 
```
  
- Was passiert wenn ihr `Tab` drückt und mit `<Enter>` in die nächste Zeile springt?  
- Verwerft den Vorschlag mit Esc oder löscht den generierten Code. Erstellt einen Kommentarblock mit folgendem Inhalt. Was passiert nachdem ihr den Kommentarblock geschlossen habt und der Curser in der Zeile darunter steht?
```
/*
 * 
 * Eine Task hat folgende Eigenschaften:
 *
 * - id: Long
 * - description: String
 * - isCompleted: Boolean
 * - maxEffortHrs: Effort
 * 
 */
```

- Bestätigt jeden Vorschlag mit `Tab` und wechslt mit `<Enter>` in die nächste Zeile. Fahrt so lange fort, bis keine Vorschläge mehr kommen.
- Nachdem die schließende Klammer für die Klasse vorgeschlagen und von euch akzeptiert wurde, plaziert den Curser in die Zeile vor der schließenden Klammer. Was wird noch generiert?
- Wenn Dinge generiert wurden, die ihr nicht braucht, löscht diese einfach.
- Legt die Datei für das Enum ´Effort´ im Package ´onsite.academy.myworkday.model´ an. Geht bei der Implementierung so vor, wie schon beim Erstellen der Klasse Task.

### Ein Controller
- Legt die Klasse TaskController an. Löscht die Klassendefinition. Experimentiert mit präzisen Top-Level Kommentaren. Beispiel:

```
// Spring-Boot Controller
```
- Was wird vorgeschlagen? Was passiert, wenn ihr die Vorschläge akzeptiert?
- Wenn zunächst weitere Zeilenkommentare vorgeschlagen werden, akzeptiert diese so weit, wie sie euch sinnvoll erscheinen. Löscht dann die Zeilen, die ihr nicht braucht.
- Was passiert, wenn ihr nach dem letzten Zeilenkommentar eine Zeile leer lasst?
- Werden Imports vorgeschlagen? Werden Annotationen wie `@RestController` vorgeschlagen?	
- Wird ein TaskService Autowired, der noch garnicht existiert?
- Implementiert und testet den Controller. Beim Zugriff auf die GET-Schnittstelle soll die Annwendung dem Bowser mit einer fest verdrateten Liste von Tasks antworten.

## Erreichter Zustand

- Für das Fachobjekt `Task` wurden REST-Endpunkte implementiert. Die Endpunkte sind unter `http://localhost:8080/tasks` erreichbar.
- Die HTTP GET-Methode gibt eine (fest verdratete) Liste aller Tasks zurück. Testet das mit einem RESTClient oder mit einem Browser.
- Die anderen Methoden sind ggf. noch nicht ausimplementiert, die Restendpunkte sind aber schon vorhanden. Es wird mindestens HTTP 200 als Status zurück gegeben.
