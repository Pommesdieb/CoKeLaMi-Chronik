# Football Domain Model

## NFL

Persistierbare Objektarten:

- `season`
- `team`
- `player`
- `game`
- `standing_snapshot`
- `draft`
- `record`
- `history_event`
- `knowledge_item`

Empfohlene stabile Referenzen verwenden NFL-/Quell-IDs, sofern verifiziert; Namen allein sind keine dauerhafte technische Identität.

## Fantasy Football

Persistierbare Objektarten:

- `league`
- `fantasy_season`
- `manager`
- `fantasy_team`
- `roster_snapshot`
- `fantasy_draft`
- `matchup`
- `fantasy_standing_snapshot`
- `playoff_result`
- `transaction`
- `projection_snapshot`
- `editorial_item`

## Beziehungen

```text
NFL player/team/game
       ^
       | references
       |
Fantasy league -> season -> fantasy team -> roster snapshot
                         -> draft pick ------> NFL player
                         -> matchup ---------> fantasy teams
                         -> projection ------> NFL player/team/game
```

Fantasy-Daten referenzieren allgemeine NFL-Objekte, kopieren deren Stammdaten aber nicht unnötig. Fantasy-spezifische Werte wie Punkte, Lineup-Slot, Projection, Ownership oder Waiver-Vorgang bleiben im Fantasy-Kontext.

## Zeitsemantik

Jedes zustandsbehaftete Artefakt soll mindestens `season` und, wo relevant, `as_of`, `week`, `phase` oder `effective_at` tragen. Historische Zustände sind append-/snapshot-orientiert; spätere Korrekturen werden als Korrektur mit Provenienz dokumentiert, nicht durch unmarkiertes Umschreiben historischer Realität.

## Provenienz

Persistierte Fakten sollen soweit praktisch enthalten:

- `source_id` aus `sources/catalog.yaml`;
- Erfassungs-/Standdatum;
- `fact_type`: `SOURCE_FACT`, `SNAPSHOT`, `DERIVED`, `EDITORIAL`;
- bei Unsicherheit eine explizite Qualifikation statt erfundener Präzision.
