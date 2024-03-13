# Übung 6

## Aufgabe

Euer Dashboard soll ein Bild als Hintergrund fensterfüllend anzeigen. Das Bild soll von einem online-Dienst wie z.B. Flickr geladen werden. 

## Infos vorab

- Ihr werdet ein API-Token für den Zugriff auf die Flickr-API benötigen. Ihr erhaltet es von euren Trainern. Dieses wird nicht eingecheckt! Für die ersten Versuche steht es noch im Klartext in der URL auf die ihr zugreift...


## Experimente

- Nutzt den Chatbot von GithubCopilot. Was muss getan werden, um ein Bild von Flickr zu laden und als Hintergrund anzuzeigen?
- Iteriert so lange, bis ihr zufrieden seid. Füllt das Bild das Browserfenster aus? Ist das Bild scharf und hochaufgelöst? 
- Denkt daran, dass die relevanten Dateien geöffnet sein müssen, damit GithubCopilot brauchbare Verbesserungsvorschläge machen kann.
- Wird immer das selbe Bild angezeigt? Wie könnt ihr das ändern?
- Was müsst ihr tun, damit das API-Token benutzt werden kann, aber nicht commited wird?
- Kann man die Lösung einfacher oder besser gestalten? Testet `/simplify`.


## Erreichter Zustand

- Euer Dashboard zeigt ein Bild von Flickr als Hintergrund an.
- Das Bild füllt das Browserfenster aus und ist scharf und hochaufgelöst (bei einer Bildschirmauflösung von 1920x1080).
- Das API-Token ist in eurem Code nicht sichtbar und wird nicht commited.

````	




















````

## Hilfestellung

- Wenn ihr mit der Qualität der Bildes unzufrieden seid, könnt ihr die URL anpassen um Bilder eines spezifischen Flickr-Users zu laden (Trainer fragen). Allgemeiner Aufbau: 
`https://api.flickr.com/services/rest/?method=flickr.people.getPublicPhotos&api_key=${API_KEY}&user_id=${USER_ID}&format=json&nojsoncallback=1&extras=url_o`

