# planning — module simple de fusion d'intervalles

## But
Valider, fusionner et exporter des intervalles de planning (disponibilités) en JSON.

## Format d'entrée
Liste d'objets `{ "start": "YYYY-MM-DD HH:MM", "end": "YYYY-MM-DD HH:MM" }`.
Formats ISO `YYYY-MM-DDTHH:MM` et variantes avec secondes sont acceptés.

## Fonctionnalités
- Validation d'entrée (format, start < end)
- Fusion des intervalles qui se chevauchent ou sont adjacents
- Export JSON avec timestamps `YYYY-MM-DDTHH:MM:SS`

## Exécution (Google Colab)
1. Créer `planning.py` et `test_planning.py` (coller le code).
2. Exécuter `python -m unittest -v` pour lancer les tests.
3. Importer `to_json`/`merge_intervals` pour générer du JSON.

## Limitations & améliorations possibles
- Gestion des fuseaux horaires (actuellement naive)
- Support des récurrences (ex : tous les lundis)
- Export ICS / intégration calendar
- API HTTP (FastAPI) si besoin

