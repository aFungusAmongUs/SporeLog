<p align="center">
  <img src="https://github.com/user-attachments/assets/65c49c9d-a56e-42e5-b095-163485492279" width="550" height="300" >
</p>

<h1 align="center">SporeLog</h1>


<p align="center">
Minimal CLI to log mushroom finds, get look-alike warnings, and export your data.
  </p>

  

  > Heads up: This is **not** an identification tool. Always confirm IDs with multiple trusted sources.


<br>

## Quick start
```bash
python -m venv .venv
. .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
python sporelog.py --help
```

# Examples

## Add a find (auto-warns about toxic look-alikes)
python sporelog.py add --species "Morel" --date 2025-04-20 \
  --lat 38.63 --lon -90.20 --habitat "deciduous" --notes "burn site nearby"

## List recent entries
python sporelog.py list --limit 10

## Stats by species
python sporelog.py stats

## Exports all to CSV
python sporelog.py export --format csv --out exports/forage_log.csv

## Export only 2025 season to GeoJSON (for my maps)
python sporelog.py export --format geojson --out exports/2025.geojson --after 2025-01-01



# Data model
- data/species.json — canonical list of species with edibility, seasons, and look-alikes.
- data/forage_log.jsonl — your personal log; one JSON object per line.

# Safety
- On add, SporeLog surfaces toxic look-alikes if any are listed for the species.
- If you log a species outside its listed season range, you’ll get a “verify” nudge.
- Species data: CC BY 4.0 (feel free to improve)
