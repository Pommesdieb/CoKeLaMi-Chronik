# CoKeLaMi-Chronik · Football Corpus

Dauerhafte, maschinenlesbare und menschlich nachvollziehbare Wissensbasis für den Football-Komplex: **NFL** plus **Fantasy Football**.

## Scope

- `nfl/`: allgemeines NFL-Wissen, historisch persistierenswerte NFL-Zustände, Teams, Spieler, Games, Standings, Drafts, Records, History und kuratierte Knowledge/Trivia.
- `fantasy/`: liga- und seasongebundener Fantasy-Zustand: Leagues, Managers, Fantasy Teams, Rosters, Drafts, Matchups, Standings, Playoffs, Transactions, Projections und History.
- `research/`: abgeleitete oder kuratierte Research-Artefakte mit Provenienz.
- `sources/`: Quellenregister und Migrations-/Provenienzinformationen.
- `schema/`: Semantik, Objektbeziehungen und Persistenzregeln.
- `data/`: Legacy-Bestand; wird nicht destruktiv gelöscht. Bestehende Pfade bleiben als Provenienz erhalten und werden über Migrationshinweise eingeordnet.

## Kernprinzipien

1. **NFL-Objekt != Fantasy-Zustand.** Ein NFL-Spieler wird allgemein nur einmal fachlich referenziert; seine Zugehörigkeit zu einem Fantasy-Roster ist ein season-/zeitgebundener Fantasy-Snapshot.
2. **Historical != Current.** Historische Snapshots werden nicht durch spätere Zustände überschrieben. Aktueller Live-Zustand wird nur persistiert, wenn er eigenen, historischen oder kuratierten Dauerwert hat.
3. **Source != Derived Fact.** Roh-/Originalquellen bleiben als Provenienz adressierbar. Abgeleitete Aussagen kennzeichnen ihre Quelle und ihren Stand.
4. **Non-destructive migration.** Vorhandene Drive-/Repository-Quellen werden referenziert, nicht stillschweigend ersetzt oder gelöscht.
5. **No blind live mirroring.** Triviale Live-Lookups (Scores, Injury-Status, aktuelle Standings) bleiben standardmäßig transient.

## Aktuell erschlossener Bestand

- bestehender Repository-Legacy-Pfad `data/matchups/2025/regular/`;
- Google-Drive-Ligaquelle `🏈 Fantasy Football Fever 🏈.docx`, Ausgabe 12 / Week 6 / 10.10.2025;
- Google-Drive-Ordner `Fantasy Football/Season 2025` mit `Final_Playoff_Results.png` und `podium.png`;
- Google Sheet `Fantasy Football Draft Big Board` (Tab `2026`) mit 2025er NFL-Receiving-/Separation-Daten als Draft-Research-Basis;
- Google Sheet `Kopie von SmartDraft 2025` mit Draft-Board-/Keeper-/Drafted-/Best-Available-Struktur.

## Navigation

- Liga: `fantasy/leagues/fantasy-football-fever/`
- Season 2025: `fantasy/leagues/fantasy-football-fever/seasons/2025/`
- Research: `research/`
- Quellen: `sources/catalog.yaml`
- Persistenz: `schema/persistence-policy.md`
- Datenmodell: `schema/domain-model.md`

Stand: 2026-09-13
