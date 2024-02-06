# Übung 4

## Aufgabe
- Es soll ein REST-Endpunkt (/nextTask) entstehen, der dem Anwender die nächste zu bearbeitende Aufgabe liefert.
- Die Anwender arbeiten von 9 bis 17 Uhr. Die Schnittstelle liefert die größte Aufgabe, die noch nicht erledigt wurde und die bis EOB bearbeitet werden kann.
- Auch nach 16:00 Uhr soll der Anwender noch eine Aufgabe erhalten, wenn noch nicht alle Aufgaben erledigt sind. In diesem Fall soll die Aufgabe mit dem geringsten Aufwand zurückgegeben werden.

## Experimente

- Legt eine Methode `public Task nextBiggestTaskForToday()` an. Die Methode soll die größte Aufgabe zurückgeben, die noch nicht erledigt wurde und die bis EOB  bearbeitet werden kann. Arbeitet mit präzisen Zeilenkommentaren, damit ihr keine Zeile der Implementierung selbst schreiben müsst. (Beispiele: siehe ganz unten)
- Legt eine Testklasse `TaskServiceTest` an und implementiert diese mit Hilfe von GithubCopilot-Chat. Markiere dazu den Code des Service und gib im Chat das Kommando `/tests`ein. Verfifiziert die Implementierung und passt sie an, wo nötig.
- Überarbeitet den Code, um die Testbarkeit eures Service zu verbessern.  

## Erreichter Zustand

- Ihr habt eine Service-Methode mit Fachlogik erzeugt und dafür Tests erstellt.
- Ihr habt die Testbarkeit eures Service verbessert.

## Beispiele für präzise Zeilenkommentare

```java
// Lade eine Liste von Tasks die noch nicht abgeschlossen sind und sortiere sie absteigend nach Aufwand

// Ermittle die Anzahl ganzer Stunden bis 17:00 Uhr

// Iteriere über die Liste der Tasks und prüfe ob der Aufwand des Tasks kleiner oder gleich der verbleibenden Stunden ist

// Wenn keine passende Task gefunden wurde, es aber noch Tasks gibt, die nicht abgeschlossen sind, gib die Task mit dem geringsten Aufwand zurück

````

