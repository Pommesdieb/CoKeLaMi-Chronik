# Football Corpus Migration · 2026-09-13

## Repository pre-image

Before this migration the repository contained only:

`data/matchups/2025/regular/2025-W01-REG-HEX-vs-HHD.json`

The file was 1 byte and is preserved in place as legacy provenance.

## Resolved external source stock

1. Google Drive: `🏈 Fantasy Football Fever 🏈.docx` — readable Week-6 editorial snapshot (2025-10-10).
2. Google Drive: `Fantasy Football/Season 2025` — historical playoff-result and podium image artifacts.
3. Google Sheets: `Fantasy Football Draft Big Board` — 2026 board backed by observed 2025 receiving/separation research data.
4. Google Sheets: `Kopie von SmartDraft 2025` — draft-tool structure including Draft Board, Auction Draft Board, Keepers, Drafted and Best Available.
5. Existing GitHub legacy matchup placeholder.

Searches also covered `Fantasy Football`, `Fantasy Football Fever Week`, `Hercynian Hagazussa` and the accessible File Library; no additional high-confidence Football/Fantasy corpus source was positively resolved in those searches.

## Migration choices

- verified structured facts were normalized into league/season/matchup records;
- source artifacts that could not be semantically read (notably the two Season-2025 images) were registered as provenance without inventing champion/podium facts;
- research tables were documented by schema/purpose instead of bulk-copying changing spreadsheet data;
- legacy repository data was retained;
- no current NFL live feed was snapshotted merely to populate empty folders.

## Identity note

Repository persistence is independent from claiming a resolved ORDO Workspace Identity. During the same refresh, the Entity Registry showed `MI-012` as NFL while the active Identity Relations table simultaneously contained `MI-012 MOVE VE-001`; this is an unresolved canonical-identifier collision. Therefore repository policy deliberately does not encode `MI-012` as a verified canonical identity until ORDO/ISAAC reconciliation is completed.
