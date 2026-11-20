# Piano Levels

Schritt für Schritt Klavier lernen am Casio SA-46 Mini-Piano: Puls, Rhythmus (mit Rhythmussprache), Töne und Akkorde bis zum Klassenarrangement.

Reine statische Seite (`index.html`), keine Build-Schritte.

## Hinweise
- **Demo:** Adresse mit `?demo` aufrufen oder oben rechts den Knopf «Demo» drücken: alle Level offen.
- **Freigabe:** In `index.html` oben in `CONFIG` einstellen: `approval:'teacher'` (Freigabewort) oder `'self'` (Schüler schalten selbst frei). Freigabewörter und Lehrercode stehen ebenfalls dort.
- **Das Lied «Hemmige»** (Mani Matter) ist nur ein Beispiel für Tests. Vor einer öffentlichen Veröffentlichung durch andere Lieder ersetzen. Deshalb ist dieses Repository privat.

## Firebase Hosting
```
npm i -g firebase-tools
firebase login
firebase init hosting   # public directory: .   (nicht überschreiben: firebase.json existiert)
firebase deploy --only hosting
```
