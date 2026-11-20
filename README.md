# Piano Levels

Schritt für Schritt Klavier lernen am Casio SA-46 Mini-Piano: Puls, Rhythmus (mit Rhythmussprache), Töne und Akkorde bis zum Klassenarrangement.

Reine statische Seite (`index.html`), keine Build-Schritte.

## Hinweise
- **Demo:** Adresse mit `?demo` aufrufen oder oben rechts den Knopf «Demo» drücken: alle Level offen.
- **Freigabe:** In `index.html` oben in `CONFIG` einstellen: `approval:'teacher'` (Freigabewort) oder `'self'` (Schüler schalten selbst frei). Freigabewörter (Level 2–4) und Lehrercode stehen ebenfalls dort. Level 1 schliesst die App selbst ab (Tipp-Tests).
- **Aufbau:** Übersicht mit «Puls und Rhythmus» (Rhythmussprache, Notenwerte, Zufallsrhythmus, 4/4 und 3/4) und «Mini-Piano kennenlernen». Jedes Lied hat vier Level: 1 Bausteine & Rhythmus (Zeilen wählbar), 2 Ein Ton, 3 Akkordtöne, 4 Zusammen. Tempo startet beim Originaltempo des Lieds.
- **Rhythmussprache:** Schritt (Viertel), sta-ah (halbe), sta 2 3 (punktierte halbe), sta 2 3 4 (ganze), paus, und (Achtelpause), Hopp (einzelne Achtel), Laufe (2 Achtel), umerenne (4 Sechzehntel).
- **Neue Lieder:** In `SONGS` ergänzen (Takte als Ereignislisten, `blocks`, `lines`, `bpm`, optional `bpb:3` für den 3/4-Takt).
- **Fortschritt:** Gespeicherter Stand von früheren Versionen (5 Level) wird beim ersten Start auf 4 Level umgerechnet.

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
- Lieder (in dieser Reihenfolge): Inhibitions, Alles von mir, Granate, Scarborough Fair (3/4-Takt). Jedes Lied hat ein Emoji (`em` im Lied-Objekt).
- Akkordprojekt: eigene Ansicht (`view 'akk'`). Akkorde lernen (Griffe in `AK_CH`), abhaken, passende Lieder aus `AK_SONGS` mit Akkorden, Tempo, Rhythmus und Metronom. Weitere Lieder werden in `AK_SONGS` ergänzt.

