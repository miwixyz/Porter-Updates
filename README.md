<p align="center"><img src="bilder/porter-symbol.png" width="128" alt="Porter-Symbol"></p>

# Porter

Porter ist ein Dateimanager mit zwei Spalten für macOS 27. Links ein Ordner, rechts ein Ordner, und eine Datei wandert mit einem Tastendruck hinüber. Wer früher mit dem Norton Commander oder Total Commander gearbeitet hat, kennt das Prinzip. Gelöscht wird nie endgültig: Alles, was weg soll, landet im Papierkorb.

![Porter im hellen Modus](bilder/porter-hell.png)

## Was Porter kann

### Zwei Spalten
- Tab wechselt die Spalte, ein Klick irgendwo hinein auch. F5 kopiert, F6 verschiebt, F2 benennt um, F7 legt einen Ordner an, F8 wirft in den Papierkorb. Liegt am Ziel schon eine Datei mit dem Namen, fragt Porter vorher.
- Jede Spalte hat Tabs. Die ziehst du mit der Maus in die Reihenfolge, die du willst, und Porter merkt sie sich. Dazu Zurück und Vor und eine Pfadleiste, deren Glieder du anklicken kannst. Die Leertaste öffnet Quick Look.
- In der Seitenleiste stehen deine Favoriten (hineinziehen, umsortieren), die Laufwerke mit Auswerfen-Knopf und iCloud sowie andere Cloud-Ordner. Auch einzelne Dateien kannst du dort ablegen oder per Rechtsklick hinzufügen. Sie stehen dann im Block „Dateien“ und gehen mit einem Klick auf. Wie breit die Leiste ist, stellst du am rechten Rand ein.
- Sortieren per Klick auf den Spaltenkopf, gruppieren nach Art, Datum oder Größe. Jede Spalte merkt sich ihre eigene Ansicht.

### Suchen und entpacken
- command-F öffnet die Suche. Beim Tippen bleiben nur die Dateien stehen, deren Name passt. Im Menü daneben stellst du ein, wie weit Porter sucht: nur im Ordner, im ganzen Ordnerbaum oder auf allen Laufwerken. Die beiden weiten Suchen laufen über Spotlight, die Treffer stehen nach Ordner sortiert untereinander. Laufwerke ohne Spotlight-Index tauchen dabei nicht auf, und frisch angelegte Dateien findet Spotlight erst nach einer Weile.
- Doppelklick auf ein ZIP-, 7z- oder RAR-Archiv, und Porter packt es selbst aus. Ein Finder-Fenster geht dabei nicht auf. Der Inhalt liegt danach neben dem Archiv und ist markiert, auch Archive mit Passwort klappen. Dafür braucht Porter das kostenlose 7-Zip (`brew install sevenzip`).

### Aufräumen

![Duplikate finden](bilder/porter-aufraeumen.png)

- Porter findet Duplikate über die Prüfsumme, die älteste Datei bleibt stehen. Außerdem große Dateien, die du lange nicht geöffnet hast, und leere Ordner.
- Auf Wunsch sortiert Porter einen Ordner in Unterordner, nach Art oder nach Monat.
- Der KI-Vorschlag nutzt Apples Sprachmodell auf deinem Mac. Es sieht nur die Dateinamen, und nichts verlässt den Rechner. Perfekt ist es nicht (im Test landete ein Passwort-Notfallblatt bei den Rechnungen), deshalb siehst du jede Zuordnung vorher und kannst sie ändern.
- Vor jedem Schritt zeigt Porter, was passieren wird. Verschieben lässt sich rückgängig machen, und Gelöschtes holst du aus dem Papierkorb zurück.

### Umwandeln, packen, umbenennen
- Bilder werden zu JPG, PNG, WebP, HEIC oder AVIF, auf Wunsch kleiner gerechnet. Aus Bildern wird SVG oder ein PDF, aus PDF-Seiten werden Bilder.
- Packen geht als ZIP, als ZIP mit Passwort (AES-256) oder als verschlüsseltes DMG. Das Passwort speichert Porter nirgends.
- Viele Dateien auf einmal umbenennen: neuer Name, Suchen und Ersetzen, laufende Nummern, Datum, Kleinschreibung, Unterstriche statt Leerzeichen. Mit Vorschau, und der letzte Durchgang lässt sich zurücknehmen.

### Notizen und Aufgaben
- F4 hängt eine Notiz an die markierte Datei oder den Ordner. Das kann eine Beschreibung sein („Endfassung vom Verleih“) oder eine Aufgabe („Plakat fehlt, Verleih fragen“), die du später abhakst. Ein kleines Symbol hinter dem Namen zeigt, dass es eine Notiz gibt.
- Aus dem Notizfeld heraus legst du auf Wunsch eine Erinnerung in Apples Erinnerungen an: mit Termin, dem Notiztext und einem Link, der die Datei öffnet.
- command-control-N listet alle offenen Aufgaben. Ein Doppelklick bringt dich zur Datei.
- Die Notizen liegen in einer Datei in deinem iCloud Drive, deshalb siehst du sie auf jedem deiner Macs. Benennst du eine Datei in Porter um oder verschiebst sie, kommt die Notiz mit.

### Kleinkram, der im Alltag zählt
- Der Rechtsklick kann, was man vom Finder kennt: Öffnen mit, Teilen, Dienste, Pfad kopieren, Terminal hier öffnen, Informationen.
- Ein Symbol in der Menüleiste führt zu Favoriten und Laufwerken. Wer es nicht mag, schaltet es ab.
- Auf Wunsch übernimmt Porter „Im Finder zeigen“: Klickst du in Safari, Mail oder einer anderen App darauf, öffnet sich Porter mit der markierten Datei. Ganz ersetzen lässt sich der Finder nicht. Schreibtisch, Dock und Ordner, die andere Apps öffnen, bleiben bei ihm, das gibt macOS so vor. Ausschalten im Porter-Menü holt den Finder zurück.
- command-Plus und command-Minus machen die Schrift größer oder kleiner. Porter merkt sich die Größe.
- Ist ein Dateiname zu lang für die Spalte, zeigt Porter ihn beim Darüberfahren ganz.
- Läuft auch auf kleinen Bildschirmen. Getestet an einem Monitor mit 1344 × 504 Punkten: Das Fenster passt drauf, und im Vollbild bleiben die Knöpfe oben erreichbar. Wird das Fenster schmal, wandern Neuer Tab, Orte und Aufräumen in ein „…“-Menü, und wird eine Spalte zu eng für die Namen, rollt sie seitlich. Spalten ziehst du im Spaltenkopf breiter, Porter merkt sich die Breite. Auch die Aufteilung zwischen linker und rechter Spalte lässt sich in der Lücke dazwischen verschieben. Die Leiste mit den F-Tasten unten lässt sich ausblenden (command-control-B), die Tasten wirken dann trotzdem.
- Hell und dunkel, passend zum System.

![Porter im dunklen Modus](bilder/porter-dunkel.png)

## Installieren

1. Unter [Releases](https://github.com/miwixyz/Porter-Updates/releases) die neueste `Porter-vX.Y.Z-macOS.zip` laden.
2. Entpacken und `Porter.app` in den Ordner *Programme* ziehen.
3. Damit Porter in alle Ordner schauen darf: *Systemeinstellungen → Datenschutz & Sicherheit → Festplattenvollzugriff*, dort Porter einschalten.

Porter braucht macOS 27. Die App ist mit einer Apple Developer ID signiert und von Apple notarisiert. Auf Mac-Tastaturen drückst du die F-Tasten zusammen mit fn, außer du hast sie in den Systemeinstellungen als Standardtasten eingestellt.

## Updates

In der App unter **Porter → Nach Updates suchen …**. Beim zweiten Start fragt Porter einmal, ob es selbst nach Updates suchen darf. Jedes Update trägt zwei Signaturen (EdDSA und Apple Developer ID). Porter installiert nur, was beide Prüfungen besteht, und eine veränderte Update-Liste lehnt es ab.

## Datenschutz

Porter schickt nichts über dich oder deine Dateien irgendwohin. Es gibt kein Konto und keine Nutzungsstatistik. Die einzige Verbindung ins Netz ist die Update-Suche hier bei GitHub. Notizen schreibt Porter in eine Datei in deinem iCloud Drive, die iCloud wie jede andere Datei dort zwischen deinen Macs abgleicht. Passwörter und Kontodaten gehören deshalb nicht in eine Notiz. Für Erinnerungen fragt macOS beim ersten Mal nach dem Zugriff. Apple vergibt dafür nur Lese- und Schreibrecht zusammen, Porter legt aber nur an und liest deine Erinnerungen nicht.

## Was in diesem Repo liegt

Nur die fertigen, notarisierten Versionen (unter *Releases*) und die signierte Update-Liste `appcast.xml`. Der Quellcode von Porter ist nicht öffentlich. Die Bilder oben zeigen einen Demo-Ordner.

Alle Rechte vorbehalten © 2026 Michael Wildenauer.
