# Übung 2

## Aufgabe

- Implementiert die CRUD-Funktionalität für die Ressource "Task"
- Für die Persistenz nutzen wir Spring-Data-JPA
- Als Datenbank nutzen wir eine Filebasierte H2-Datenbank
- Stellt mit einer Testklasse sicher, dass die CRUD-Operationen funktionieren

## Experimente

- Kommentiert die Klassendefinition von Task aus und fügt Imports hinzu:

```java
import jakarta.persistence.Entity;
import jakarta.persistence.EnumType;
import jakarta.persistence.Enumerated;
import jakarta.persistence.Id;
```

- Was wird generiert? Im Ergebnis soll ein JPA-Entity entstehen. 
- Öffnet den GithubCopilot Chat. Findet mit Hilfe des Chat heraus, wie ihr die `application.properties` anpassen müsst, um eine Filebasierte H2-Datenbank zu konfigurieren.
- Im neuen Package `onsite.academy.myworkday.repository` legt ihr ein Interface `TaskRepository` an. 
- Vergleicht die Vorschläge: Was passiert wenn nur der Reiter mit dem Interface in der IDE geöffnet ist? Was passiert wenn daneben der Reiter mit der Klasse Task geöffnet ist?
Hier eine funktionierende Variante für Leute die Spring-Data-JPA noch nicht kennen:
```java
package onsite.academy.myworkday.repository;

import onsite.academy.myworkday.model.Task;
import org.springframework.data.jpa.repository.JpaRepository;

public interface TaskRepository extends JpaRepository<Task, Long> {
}
``` 

- Legt eine Klasse `TaskRepositoryTest` an und implementiert diese mit Hilfe von GithubCopilot-Chat. Achtung: Der Chat kann euch eine komplette Implementierung liefern - ihr müsst aber prüfen ob die Implementierung wirklich das Speichern und Laden in der H2-DB testet. Wenn Fehler auftreten, stellt sie dem Chat zur Verfügung. Wenn der generierte Test nicht das testet was ihr testen wollt, konkretisiert eure Intention im im Chat.


## Ergebnisse

- Ihr habt mit einem Test nachgewiesen, dass Task gespeichert und geladen werden kann.