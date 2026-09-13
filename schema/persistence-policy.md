# Football Persistence Policy

## Default

Persistiere Football-Informationen in diesem Repository, wenn sie einen dauerhaften Eigen-, Historien-, Research- oder Beziehungwert besitzen.

### Persistieren

- Fantasy Football Fever und andere relevante Liga-Stammdaten;
- Season-, Draft-, Roster-, Matchup-, Standings-, Playoff-, Result- und Transaction-State;
- historische Snapshots;
- eigene Draft Boards, Rankings, Bewertungen und Research-Artefakte;
- historisch relevante NFL-Daten, Records und kuratierte Knowledge/Trivia;
- dauerhafte Korrekturen und neu verifizierte Beziehungen;
- redaktionelle Fantasy-Inhalte, sofern sie einen Season-/Chronikwert haben.

### Standardmäßig nicht persistieren

- triviale Live-Scores ohne späteren historischen/kontextuellen Wert;
- kurzfristige Injury-/Depth-Chart-/Odds-Lookups;
- aktuelle Standings, wenn sie nur für eine einzelne Antwort abgefragt werden;
- unkuratierte Web-Suchergebnisse.

## Zielauflösung

- allgemeine NFL-Fakten -> `nfl/`;
- liga-/seasongebundener Fantasy-Zustand -> `fantasy/leagues/<league>/seasons/<year>/`;
- abgeleitete Analyse/Rankings -> `research/<year>/` mit Quellenverweis;
- Quellen-/Migrationsnachweis -> `sources/`;
- Legacy-Dateien werden nicht destruktiv verschoben, solange kein verifizierter inhaltlicher Ersatz besteht.

## Current vs Historical

Live-Daten sind **Current** und transient, bis ein Persistenzgrund besteht. Sobald ein Zustand als Snapshot übernommen wird, wird er **Historical** und bleibt reproduzierbar. Ein späterer Current-State überschreibt keinen Historical-State.

## Workspace-Regel

Der Football-Workspace soll diese Policy als kanonische Repository-Persistence-Regel auflösen. Der Conversation Carrier ist keine SSoT. Identity-/Registry-Verweise dürfen erst als verifiziert eingetragen werden, wenn die ORDO/ISAAC-Identity-Reconciliation widerspruchsfrei abgeschlossen ist.

Stand: 2026-09-13
