# Game Tracker — Product Charter

## 1) Problem
Ich will meine gespielten Games und Spielzeiten zentral tracken und bewerten. Später sollen Daten optional aus Plattformen wie Steam angereichert/importiert werden (Beschreibung, Cover, Achievements, Stunden, Reviews).

## 2) Zielgruppe
Ich und Freunde. Account-basiert. User können Profile/Stats anderer User ansehen, wenn freigegeben.

## 3) MVP muss können
- Account + Login (Registrieren/Anmelden/Abmelden)
- Game-Library manuell pflegen: Spiel hinzufügen/bearbeiten/löschen inkl. Plattform, Status (Backlog/Playing/Completed), Bewertung (z.B. 1–10), Notiz
- Übersicht/Filter: Liste mit Suche/Filter (Plattform/Status/Tag) und Sortierung (zuletzt gespielt, Bewertung)
- Basic Stats: Gesamtspielzeit pro Spiel + „zuletzt gespielt“ (pro User)
- Freundesystem / Sichtbarkeit:
  - User kann jemanden als Freund hinzufügen (Invite/Accept)
  - Danach kann man Stats & Bewertungen des Freundes ansehen

## 4) Erfolgskriterien
- MVP-Workflow funktioniert end-to-end: User kann 10 Spiele anlegen und 20 Sessions erfassen, ohne Bugs/Workarounds
- Qualität/Engineering: CI baut automatisch und Tests laufen grün (z.B. >30% Code-Coverage als Startziel oder „mind. 20 sinnvolle Tests“)
- Performance/UX-Basis: Game-Liste lädt bei 200 Einträgen in < 1 Sekunde lokal (oder definierter Grenzwert)

## 5) Annahmen & Risiken
- Steam API / Rate Limits / Auth: Integration ist zeitintensiv (OAuth/Key, Limits, Datenqualität)
- Datenmodell wird schnell komplex (Games, Plattformen, Sessions, Bewertungen, Bilder, Reviews)
- Scope Creep: „nur schnell Achievements/Friends/Sync“ sprengt den MVP
- Security: Account-basiert heißt Passwort-Handling, Session/Token, Datenschutz. Risiko: unsauber umgesetzt

## 6) Tech/Constraints
- UI: Web
- Offline nötig? Nein
- Wichtigstes Qualitätsziel: Clean Code / Lernziel
- Zeitbudget pro Tag (realistisch): 2 Stunden
