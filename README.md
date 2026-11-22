# Piano Levels

Schritt für Schritt Klavier lernen am Casio SA-46 Mini-Piano: Puls, Rhythmus (mit Rhythmussprache), Töne und Akkorde bis zum Klassenarrangement.

Reine statische Seite (`index.html`), keine Build-Schritte.

## Hinweise
- **Demo:** Adresse mit `?demo` aufrufen oder oben rechts den Knopf «Demo» drücken: alle Level offen.
- **Freigabe:** In `index.html` oben in `CONFIG` einstellen: `approval:'teacher'` (Freigabewort) oder `'self'` (Schüler schalten selbst frei). Freigabewörter (Level 2–5) und Lehrercode stehen ebenfalls dort. Level 1 schliesst die App selbst ab (Tipp-Tests).
- **Aufbau:** Übersicht mit «Puls und Rhythmus» (Rhythmussprache, Notenwerte, Zufallsrhythmus, 4/4 und 3/4) und «Mini-Piano kennenlernen». Jedes Lied hat vier Level: 1 Bausteine & Rhythmus (Zeilen wählbar), 2 Ein Ton, 3 Akkordtöne, 4 Zusammen. Lieder mit Melodie (Inhibitions, Scarborough Fair) haben ein fünftes Level «Melodie»: Melodie nach Notenblatt, Begleitung zuschaltbar (Melodien: `HMEL`, `SMEL` in `index.html`). Alles von mir und Granate haben noch keine Melodie. Tempo startet beim Originaltempo des Lieds.
- **Rhythmussprache:** Schritt (Viertel), sta-ah (halbe), sta 2 3 (punktierte halbe), sta 2 3 4 (ganze), paus, und (Achtelpause), Hopp (einzelne Achtel), Laufe (2 Achtel), umerenne (4 Sechzehntel). Neu: Hüpfe (punktierte Achtel + Sechzehntel), Triole (3 Noten pro Schlag), Banane (3 Achtel im 6/8), Trinidad (punktierte Viertel); Auftakt, 2/4 und 6/8 als eigene Bausteine.
- **Neue Lieder:** In `SONGS` ergänzen (Takte als Ereignislisten, `blocks`, `lines`, `bpm`, optional `bpb:3` für den 3/4-Takt).
- **Fortschritt:** Gespeicherter Stand von früheren Versionen (5 Level) wird beim ersten Start auf 4 Level umgerechnet.

- **Drucken:** Knopf «🖨 Drucken» oben (nicht auf der Startseite) druckt die aktuelle Seite als A4 mit Noten und Rhythmussprache, Bedienelemente werden ausgeblendet.

## Veröffentlichung
GitHub Pages (Branch `main`, Ordner `/`). Die App ist als Chrome-/iPad-App installierbar.

## Firebase Hosting (optional)
```
npm i -g firebase-tools
firebase login
firebase init hosting   # public directory: .   (nicht überschreiben: firebase.json existiert)
firebase deploy --only hosting
```

## Lieder und Akkordprojekt
- Lieder (in dieser Reihenfolge): Inhibitions, Scarborough Fair (3/4-Takt), Alles von mir, Granate. Jedes Lied hat ein Emoji (`em` im Lied-Objekt). Granate hat Strophe (zweite Hälfte mit Dm), Refrain, Instrumental (Dm/F, Am/E) und Coda (Gm, Gm, Dm, Dm, Gm, Gm, A7, A7) nach dem Akkordblatt; Rhythmus von Instrumental und Coda: ganze Noten (Vorschlag).
- Akkordprojekt (`view 'akk'`): ① Einführung Dreiklänge (Dur, Moll, vermindert, übermässig, Septakkord; Baukasten und Übungen), ② Grundstellung und Umkehrungen (Übungen, Akkordwechsel nahe beieinander), ③ Lieder nach Schwierigkeit (`AKSONGS`: Himalaya, Shape of You, Havana, Hit the Road Jack) mit Griffen, Akkord-Übung und Begleitung mit Metronom (rechte und linke Hand einzeln stummschaltbar). Übungen: Akkord wird genannt, auf dem Piano drücken, die App sagt richtig/falsch. Alles ist frei zugänglich (keine Sperren, Ziel 70 %). Tasten werden beim Drücken eingefärbt (grün richtig, rot falsch, gelb fehlt). Begleitung läuft in Schleife bis Stopp: Himalaya 90 BPM (Achtel), Shape of You 96 BPM (2 Akkorde pro Takt), Havana 105 BPM (Rhythmus nach Klavierarrangement, 4 Takte: Gm–Es, D7, Gm–Es, D7), Hit the Road Jack 87 BPM (halbes Tempo von 173, Swing; linke Hand Halbe C–B–As–G, rechte Hand auf dem Off-Beat).

## Feedback
Der Knopf «💬 Feedback» öffnet ein externes, anonymes Formular bei Tally (Fehler, Wünsche, Inhalte). Nur dann werden Angaben gesendet – zusammen mit App-Name, Version und Gerätetyp. Namen werden nicht abgefragt.
