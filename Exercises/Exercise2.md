# Übung 2

## Aufgabe

- Implementiert die CRUD-Funktionalität für die Ressource "Task"
- Für die Persistenz nutzen wir Spring-Data-JPA
- Als Datenbank nutzen wir eine Filebasierte H2-Datenbank
- Stellt mit einer Testklasse sicher, dass die CRUD-Operationen funktionieren

## Erste Schritte

- Im neuen Package `onsite.academy.myworkday.repository` legt ihr ein Interface `TaskRepository` an. 

## Experimente

### Ein JPA-Entity

- Kommentiert die Klassendefinition von Task aus und fügt Imports hinzu:

```java
import jakarta.persistence.Entity;
import jakarta.persistence.EnumType;
import jakarta.persistence.Enumerated;
import jakarta.persistence.Id;
```

- Was wird generiert? Im Ergebnis soll ein JPA-Entity entstehen. 

### Spring-Boot DB-Config

- Öffnet den GithubCopilot Chat. Findet mit Hilfe des Chat heraus, wie ihr die `application.properties` anpassen müsst, um eine Filebasierte H2-Datenbank zu konfigurieren. Wenn ihr den Chat nicht nutzen könnt, fügt folgenden Kommentar in die Datei ein und schaut was generiert wird:

```
# H2 file based DB for storing the data
```

### Ein Repository
- Im neuen Package `onsite.academy.myworkday.repository` legt ihr ein Interface `TaskRepository` an. 
- Löscht den Inhalt von `TaskRepository` und lasst euch von GithubCopilot helfen, das Interface zu implementieren.
- Vergleicht die Vorschläge: Was passiert wenn nur der Reiter mit dem Interface in der IDE geöffnet ist? Was passiert wenn daneben der Reiter mit der Klasse Task geöffnet ist?
Hier eine funktionierende Variante für Leute die Spring-Data-JPA noch nicht kennen:
```java
package onsite.academy.myworkday.repository;

import onsite.academy.myworkday.model.Task;
import org.springframework.data.jpa.repository.JpaRepository;

public interface TaskRepository extends JpaRepository<Task, Long> {
}
``` 

### Testen mit JUnit

- Legt eine Klasse `TaskRepositoryTest` an und implementiert diese mit Hilfe von GithubCopilot-Chat. Markiere dazu den Code des Repository und gib im Chat das Kommando `/tests`ein. 
- Achtung: Der Chat kann euch eine komplette Implementierung liefern - ihr müsst aber prüfen ob die Implementierung wirklich das Speichern und Laden in der H2-DB testet. Wenn der generierte Test nicht das testet was ihr testen wollt, konkretisiert eure Intention im Chat. 
- Falls ihr den Chat nicht nutzen könnt, öffnet die Datei `TaskRepositoryTest` und achtet darauf dass sonst die Datei `TaskRepository` sowie die Klasse `Task` und das Enum `Effort` geöffnet sind. Dann lasst ihr euch zeilenweise von GithubCopilot zunächst die Imports und dann die Testmethoden generieren. 
- Wenn Fehler auftreten, kopiert die Fehlermeldung in das Chatfenster um das Problem zu lösen. stellt sie dem Chat zur Verfügung. 


## Erreichter Zustand

- Ihr habt mit einem Test nachgewiesen, dass Task gespeichert und geladen werden kann.