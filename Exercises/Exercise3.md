# Übung 3

## Aufgabe

- TaskService soll Controller und Repository verbinden. Später wird dieser Service die Fachlogik enthalten.

## Erste Schritte

- Legt ein Package `onsite.academy.myworkday.service` und eine Klasse `TaskService` an.

## Experimente

- Arbeitet mit den Vorschlägen von GithubCopilot und eurer Entwiklungsumgebung. Versucht den Service mit den CRUD-Methoden in eure Anwendung zu integrieren, ohne eine Zeile Code selbst zu tippen. Löschen von vorhandenem oder generiertem Code ist natürlich erlaubt!


## Erreichter Zustand

- Der TaskService wurde als Schicht zwischen Controller und Repository integriert.
- Mit einem REST-Client habt ihr ein paar Testdaten in die Datenbank eingefügt.

## Beispiele für Tasks die per POST-Request im System angelegt werden können

````
POST http://localhost:8080/tasks
Content-Type: application/json

{
  "description": "Decidalo-Profil aktualisieren und FK bescheid geben",
  "effort": "ONE_HOUR"
}

###

POST http://localhost:8080/tasks
Content-Type: application/json

{
  "description": "Meinen Beitrag für das Gildentreffen vorbereiten",
  "effort": "TWO_HOURS"
}

###

POST http://localhost:8080/tasks
Content-Type: application/json

{
  "description": "REACT-Tutorial abschließen",
  "effort": "FOUR_HOURS"
}

###

POST http://localhost:8080/tasks
Content-Type: application/json

{
  "description": "ZEWIS-Forecast für März erfassen",
  "effort": "ONE_HOUR",
  "isCompleted": true
}


````

