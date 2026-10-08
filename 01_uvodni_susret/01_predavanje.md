---
author: Franjo Pehar
title: Akademsko i tehničko pisanje
subtitle: "1. Pisanje u informacijskim tehnologijama: čitatelj, svrha i odgovornost"
date: 8. listopada 2026.
---

# Prije nego što išta kažem…

## Uzmite papir i olovku

Za dvije minute svi ćete crtati **isti lik**.

Ja ću ga opisati. Vi crtate. Bez pitanja.

. . .

> „Nacrtaj kvadrat. Na njega stavi krug. U kvadratu je trokut. Dodaj crtu.”

## Usporedite crteže sa susjedom

::: incremental

- Jesu li isti?
- Gdje je krug? Koliko je velik?
- Kamo gleda trokut?
- Odakle kreće crta i koliko je duga?

:::

## Ovo sam imao na umu

<svg viewBox="0 0 360 220" width="520" role="img" aria-label="Kvadrat; krug čije je središte u gornjem desnom kutu kvadrata; trokut upisan u kvadrat s vrhom na sredini gornje stranice; vodoravna crta iz središta kruga udesno">
  <rect x="60" y="50" width="140" height="140" fill="none" stroke="#1f4e79" stroke-width="4"/>
  <polygon points="60,190 200,190 130,50" fill="none" stroke="#c0504d" stroke-width="4"/>
  <circle cx="200" cy="50" r="35" fill="none" stroke="#2e7d32" stroke-width="4"/>
  <line x1="200" y1="50" x2="340" y2="50" stroke="#555" stroke-width="4"/>
</svg>

. . .

Vi niste krivo crtali. **Ja sam loše pisao.**

## Drugi pokušaj: isti lik, bolje upute

1. Na sredini papira nacrtaj **kvadrat** stranice oko 6 cm.
2. Nacrtaj **krug** čije je središte u **gornjem desnom kutu** kvadrata. Promjer kruga jednak je polovini stranice kvadrata.
3. U kvadrat upiši **trokut**: osnovica mu je cijela donja stranica kvadrata, a vrh je točno na sredini gornje stranice.
4. Iz središta kruga povuci **vodoravnu crtu udesno**, dugu koliko i stranica kvadrata.

. . .

**Što se promijenilo?** Redoslijed, mjere, točke oslonca, jedna radnja po koraku.

## Ono što ste upravo doživjeli

```mermaid
flowchart LR
    A["Autor zna<br/>što misli"] -->|tekst| B["Čitatelj zna<br/>samo ono što piše"]
    B --> C{"Je li dovoljno?"}
    C -->|da| D["Čitatelj uspije"]
    C -->|ne| E["Čitatelj nagađa"]
    E --> F["Pogreška, gubitak vremena,<br/>odustajanje"]
```

**Tehničko pisanje** je umijeće zatvaranja razmaka između onoga što autor zna i onoga što čitatelj treba.

# Zašto IT stručnjak mora znati pisati?

## 23. rujna 1999.

NASA gubi letjelicu **Mars Climate Orbiter** pri ulasku u Marsovu orbitu.

. . .

Što mislite — što je bio uzrok?

. . .

::: incremental

- Jedan program računao je impuls u **funta-sila · sekundama** (lbf·s).
- Drugi je očekivao **njutn-sekunde** (N·s).
- Pogreška u putanji: faktor **4,45**.
- Specifikacija sučelja (**dokument!**) propisivala je metričke jedinice — **ali se nije poštivala**.

:::

## Kvar nije bio u raketi, nego u komunikaciji

```mermaid
flowchart TB
    S["Specifikacija sučelja: impuls u N·s"]
    T1["Zemaljski softver šalje lbf·s"]
    T2["Navigacijski softver čita kao N·s"]
    X["Putanja pogrešna 4,45 puta – letjelica izgubljena"]
    S -.->|"nije poštivana"| T1
    T1 -->|"datoteka bez provjere jedinica"| T2
    T2 --> X
```

Upozorenja navigatora o odstupanjima u putanji nisu dovela do akcije.

<small>Izvor: Mars Climate Orbiter Mishap Investigation Board, *Phase I Report*, 10. 11. 1999.</small>

## Brojke koje se tiču vas

:::: columns

::: column

### 93 %

sudionika istraživanja zajednice otvorenog koda susrelo se s **nepotpunom ili zastarjelom dokumentacijom**.

<small>GitHub Open Source Survey, 2017.</small>

:::

::: column

### 83,9 %

programera uči programirati iz **tehničke dokumentacije** — više nego iz ijednog drugog mrežnog izvora.

<small>Stack Overflow Developer Survey, 2024.</small>

:::

::::

. . .

Dokumentaciju ćete **čitati svaki dan**. Pitanje je samo hoćete li je znati i **pisati**.

## Ruke gore

::: incremental

- Tko je ikada odustao od instalacije igre, moda ili programa zbog loših uputa?
- Tko je ikada kopirao naredbu s interneta, a da nije znao što radi?
- Tko je ikada pitao AI za pomoć i dobio odgovor koji nije radio?

:::

## Upit AI-ju je tehnički tekst

:::: columns

::: column

**Upit A**

> napiši mi kod za stranicu

:::

::: column

**Upit B**

> Napiši HTML stranicu s obrascem za prijavu na radionicu. Polja: ime, e-mail, odabir termina (3 ponuđena). Bez vanjskih biblioteka. Obrazac mora provjeriti je li e-mail ispravan prije slanja.

:::

::::

. . .

Upit B ima **čitatelja, cilj, ograničenja i očekivani rezultat**. To su upravo elementi dobre tehničke specifikacije.

**AI ne ukida pisanje. Pisanje postaje način na koji upravljate alatima.**

# Što je tehničko, a što akademsko pisanje?

## Dvije vrste, ista disciplina

| | Tehničko pisanje | Akademsko pisanje |
|---|---|---|
| **Pitanje** | Kako to napraviti? | Što znamo i kako to znamo? |
| **Čitatelj** | korisnik koji želi postići cilj | stručnjak koji želi razumjeti i provjeriti |
| **Uspjeh** | čitatelj je **uspio** | čitatelj je **uvjeren** |
| **Primjeri** | README, upute, prijava problema, izvještaj | seminar, stručni članak, završni rad |
| **Ključno** | jasnoća, točnost, provjerljivost | argument, dokaz, izvori |

. . .

Obje traže isto: **znati kome pišeš, zašto pišeš i kako će čitatelj provjeriti da si u pravu.**

## Pisanje je proces, ne trenutak

```mermaid
flowchart LR
    P["Priprema<br/>čitatelj, svrha"] --> W["Pisanje<br/>prvi nacrt"]
    W --> C["Provjera<br/>radi li? je li jasno?"]
    C --> R["Revizija<br/>popravak"]
    R -->|ponovno| C
    R --> O["Objava"]
```

Prvi nacrt nikad nije gotov tekst. **Ni kod profesionalaca.**

# Kako ćemo raditi ovaj semestar

## Dva projekta i jedno čvorište

```mermaid
flowchart TB
    I["DOKUMENTACIJSKI IZAZOV<br/>5. tjedan: Pandoc i MkDocs<br/>samo prema službenoj dokumentaciji"]
    P1["P1: Moj razvojni priručnik<br/>terminal, Git, Python, VS Code<br/>objava na webu"]
    P2["P2: Stručni analitički tekst<br/>problemsko pitanje, izvori, IEEE"]
    I -->|"rješavanje problema,<br/>kriteriji za testiranje"| P1
    I -->|"studija slučaja"| P2
```

## P1: na kraju semestra imat ćete vlastitu web-stranicu

```mermaid
mindmap
  root((Moj razvojni<br/>priručnik))
    Početna i README
    Prvi koraci u terminalu
    Upute
      Git i GitHub
      Python i prvi program
    Rješavanje problema
    Moj razvojni sustav
      dijagram
      usporedna tablica
    Pojmovnik
    Alat po izboru
    Dnevnik promjena
```

Pisano u **Markdownu**, verzionirano u **Gitu**, objavljeno na **GitHub Pages**. Testira ga **kolega iz klupe**.

## Put kroz semestar

```mermaid
gantt
    dateFormat YYYY-MM-DD
    axisFormat %d. %m.
    section Temelji
    Čitatelj, stil, terminal, Git      :a1, 2026-10-08, 21d
    section Korisnik
    Upute i tutorial                   :a2, 2026-10-29, 7d
    Dokumentacijski izazov             :crit, a3, 2026-11-05, 7d
    Rješavanje problema                :a4, 2026-11-12, 7d
    section P1
    Opis, vizuali, objava              :a5, 2026-11-19, 14d
    Testiranje u paru                  :a6, 2026-12-03, 7d
    Izvještaj i kolokvij               :crit, a7, 2026-12-10, 7d
    section P2
    Izvori i problemsko pitanje        :a8, 2026-12-17, 21d
    Citiranje i argument               :a9, 2027-01-07, 14d
    Prezentacije                       :crit, a10, 2027-01-21, 4d
```

## Kako se dolazi do ocjene

```mermaid
pie showData
    title Ukupno 100 bodova
    "P1 – priručnik, testiranje, prezentacija" : 35
    "P2 – stručni analitički tekst" : 25
    "Praktični kolokvij (bez AI-a)" : 20
    "Dokumentacijski izazov" : 10
    "Zadaci na vježbama" : 10
```

Prag: **50 %** na izazovu, P1, P2 i kolokviju. Ne broje se riječi, broji se **koliko je tekst korisniku stvarno pomogao**.

# Pravila igre

## AI: smijete, ali otvoreno

| Razina | Što smijete | Primjer |
|---|---|---|
| **1** | ništa | ulazna dijagnostika, kolokvij |
| **2** | ideje i struktura | problemsko pitanje za P2 |
| **3** | povratna informacija | „Je li ovaj korak jasan?” |
| **4** | suradnja uz dokumentiranje | rješavanje tehničkog problema |

Uz svaki veći rad: **izjava o korištenju AI-a**. Izmišljeni izvor ili neprovjerena naredba — **vaša su odgovornost**, ne AI-jeva.

## Akademsko poštenje u jednoj rečenici

**Uvijek mora biti jasno što ste napravili vi, a što netko drugi** — kolega, autor knjige, Stack Overflow ili AI.

. . .

Teška povreda (prepisivanje, izmišljeni izvori, skriveni AI) **ne može se nadoknaditi bodovima**.

## E-mail nastavniku je vaš prvi tehnički tekst

:::: columns

::: column

**Ovako ne:**

> bok profesore kad je kolokvij i jel moram doc na vjezbe jer radim
>
> *Poslano s mog iPhonea*

:::

::: column

**Ovako da:**

- jasan **predmet** poruke
- pozdrav i **tko ste**
- **što trebate**, u jednoj rečenici
- kontekst, ako je potreban
- potpis i fakultetska adresa

:::

::::

# Danas na vježbama

## Plan vježbi

1. **Ulazna dijagnostika** (25 min, bez AI-a, ne ocjenjuje se)
2. **Dvije README datoteke**: koja vam pomaže, a koja ne — i zašto?
3. **Visual Studio Code i prva Markdown datoteka**
4. **Plan rada** na predmetu: svi rokovi na jednom mjestu
5. **Profesionalni e-mail**

## Za kraj: tajna ovih slajdova

Ova prezentacija nije napravljena u PowerPointu.

. . .

```markdown
## Ruke gore

- Tko je ikada odustao od instalacije igre zbog loših uputa?
- Tko je ikada kopirao naredbu s interneta, a da nije znao što radi?
```

. . .

To je **obična tekstna datoteka** u **Markdownu**, pretvorena u slajdove alatom **Pandoc**.

Za mjesec dana i vi ćete pisati ovako.
