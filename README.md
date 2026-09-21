# Albarytu NPC SF2E Tables

Work-in-progress name tables for the Starfinder Second Edition (SF2E) NPC tools by albarytu.

The `source` directory contains the input tables in the JSON format expected by [Roll Table Importer](https://foundryvtt.com/packages/roll-table-importer), a Foundry Virtual Tabletop module. The tables in `packs` are the actual module content: a Foundry VTT compendium of RollTables created from the source files with Roll Table Importer.

## Status

This module is under active development. The table collection and naming content are incomplete and may change as the NPC tools develop.

## Directory Structure

```text
source/
  first/  First-name tables
  last/   Last-name tables
  title/  Title and rank tables
packs/
  sf2e-names/  The module's Foundry RollTable compendium
```

## Table Format

Each JSON table includes a name, a dice formula, a description, and result entries with inclusive roll ranges:

```json
{
  "name": "human::first",
  "formula": "1d200",
  "description": "Human first names suitable for science-fiction and fantasy characters.",
  "results": [
    { "range": [1, 1], "name": "Adrian" },
    { "range": [2, 2], "name": "Aela" }
  ]
}
```

The result ranges should cover the formula's full range. For example, a `1d200` table should cover rolls from 1 through 200.

## Building the Compendium

1. Install [Roll Table Importer](https://foundryvtt.com/packages/roll-table-importer) in Foundry VTT.
2. Open the importer from the Rollable Tables sidebar.
3. Select a JSON file from `source` or import a directory of tables.
4. Use the imported tables to create or update the `packs/sf2e-names` compendium.

The `source` files are the editable table definitions. When table content changes, re-import them and update the packaged compendium so the module contents stay in sync.

## Foundry Module

- **Module ID:** `albarytu-npc-sf2e-tables`
- **Display name:** Albarytu NPC SF2E Tables
- **Requires:** `albarytu-npc-tools`
- **Foundry compatibility:** v14+
