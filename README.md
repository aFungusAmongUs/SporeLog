<p align="center">
  <img src="https://github.com/user-attachments/assets/65c49c9d-a56e-42e5-b095-163485492279" width="550" height="300" >
</p>

<h1 align="center">𓍊𓋼𓍊𓋼𓍊𓍊𓋼𓍊𓋼𓍊𓍊𓋼𓍊𓋼𓍊𓍊𓋼𓍊𓋼𓍊𓍊𓋼𓍊 SporeLog 𓍊𓋼𓍊𓋼𓍊𓍊𓋼𓍊𓋼𓍊𓍊𓋼𓍊𓋼𓍊𓍊𓋼𓍊𓋼𓍊𓍊𓋼𓍊</h1>


<p align="center">
Minimal CLI to log mushroom finds, get look-alike warnings, and export your data.
  </p>
<br>
  

  > Heads up: This is **not** an identification tool. Always confirm IDs with multiple trusted sources.

<br>




## Quick start
```bash
python -m venv .venv
. .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
python sporelog.py --help
```


# Data model
- data/species.json — canonical list of species with edibility, seasons, and look-alikes.
- data/forage_log.jsonl — your personal log; one JSON object per line.

# Safety
- On add, SporeLog surfaces toxic look-alikes if any are listed for the species.
- If you log a species outside its listed season range, you’ll get a “verify” nudge.
- Species data: CC BY 4.0 (feel free to improve)



<p align="center">
  <img src="https://github.com/user-attachments/assets/c413a576-619c-4ab7-9f5b-ab73a39cb07a" width="1000" height="1000" >
</p>

