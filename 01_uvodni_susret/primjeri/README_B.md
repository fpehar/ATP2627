# Tjednik

Tjednik iz CSV datoteke s obvezama ispisuje raspored za tekući tjedan u terminalu. Namijenjen je studentima koji rokove vode u tablici, a žele brz pregled tjedna bez otvaranja kalendara.

## Preduvjeti

- Python 3.10 ili noviji. Provjeri verziju naredbom `python --version`.
- Osnovno snalaženje u terminalu: otvaranje mape i pokretanje naredbe.

Tjednik je provjeren na Windowsu 11, macOS-u 14 i Ubuntuu 24.04.

## Instalacija

1. Preuzmi projekt i otvori terminal u mapi `tjednik`.
2. Instaliraj Tjednik:

    ```bash
    pip install .
    ```

3. Provjeri instalaciju:

    ```bash
    tjednik --version
    ```

    Očekivani rezultat: `tjednik 1.2.0`

## Uporaba

Tjednik čita CSV datoteku s tri stupca: datum, kolegij i obveza.

```csv
datum,kolegij,obveza
2026-10-14,ATP,Vježba 1
2026-10-16,Programiranje,Zadaća 2
```

Pokreni ga ovako:

```bash
tjednik obveze.csv
```

Očekivani rezultat:

```text
Tjedan 12. 10. – 18. 10. 2026.
  sri 14. 10.  ATP            Vježba 1
  pet 16. 10.  Programiranje  Zadaća 2
```

## Rješavanje problema

| Problem | Mogući uzrok | Rješenje |
|---|---|---|
| `tjednik: command not found` | Mapa s Pythonovim programima nije u varijabli PATH. | Pokreni `python -m tjednik obveze.csv`. |
| `Neispravan datum u retku 3` | Datum nije u obliku GGGG-MM-DD. | Ispravi datum, npr. `2026-10-14`. |
| Ispis je prazan | U CSV-u nema obveza za tekući tjedan. | Dodaj obvezu s datumom iz ovog tjedna. |

## Licenca i kontakt

Tjednik je objavljen pod licencom MIT. Pogreške prijavi kao *issue* u ovom repozitoriju i navedi operacijski sustav, verziju Pythona i cijelu poruku o pogrešci.
