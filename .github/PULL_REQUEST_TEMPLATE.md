## Co a proč

Stručný popis změny a odkaz na související issue (např. `Closes #12`).

## Důkaz funkčnosti

- Výsledek lintu, typové kontroly a testů (případně popis ručního ověření / screenshot).

## Merge danger (podle pracovní dohody)

Vyber kombinaci vratnosti a dopadu (*blast radius*):

- **Vratnost:**
  - [ ] Vratné (*two-way door* – změnu lze bezpečně vrátit)
  - [ ] Nevratné (*one-way door* – např. ztráta dat, migrace databáze, odeslané e-maily)
- **Dopad chyby:**
  - [ ] Malý dopad
  - [ ] Velký dopad

**Pravidlo kontroly před merge:**
- Vratné + malý dopad → stačí důkaz funkčnosti v PR.
- Vratné + velký dopad → druhý z týmu proklikne a zkusí rozbít.
- Nevratné + malý dopad → druhý z týmu zkontroluje.
- Nevratné + velký dopad → kontrolujeme oba důkladně před merge.

## Checklist

- [ ] Žádná osobní data (pacientů, rodičů, klientů, jednatelů), žádná neanonymizovaná data z pilotu, žádné tajné klíče ani `.env`
- [ ] Prošly automatické kontroly (lint, typy, testy)
- [ ] Pokud přibyl nový pojem nebo těžko vratné rozhodnutí, je zapsáno v `CONTEXT.md` / `docs/adr/`
