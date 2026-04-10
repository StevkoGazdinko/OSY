3. Reštartovať počítač
4. Dokončiť nastavenie (napr. Ubuntu)

### Hardvérové požiadavky
- RAM: min. 4 GB (odporúčané 8 GB)
- Disk: 5–10 GB
- CPU: 64-bit s virtualizáciou

---

## 2. VirtualBox

### Charakteristika
VirtualBox simuluje celý počítač, v ktorom beží Linux ako samostatný operačný systém.

### Výhody
- Plnohodnotný Linux (GUI aj CLI)
- Bezpečné testovanie
- Izolované prostredie

### Nevýhody
- Vyššia spotreba RAM a CPU
- Pomalší výkon
- Viac krokov pri inštalácii

### Počet krokov
10–15

### Postup inštalácie
1. Stiahnuť VirtualBox
2. Stiahnuť Linux ISO (napr. Ubuntu alebo Linux Mint)
3. Vytvoriť nový virtuálny stroj
4. Nastaviť RAM (min. 4 GB)
5. Vytvoriť virtuálny disk (min. 20 GB)
6. Pripojiť ISO a spustiť inštaláciu
7. Prejsť inštalátorom Linuxu

### Hardvérové požiadavky
- RAM: min. 8 GB
- Disk: 20–30 GB
- CPU: 64-bit s virtualizáciou

---

## 3. Boot USB / Dual Boot

### Charakteristika
Linux beží priamo na hardvéri, buď z USB alebo nainštalovaný vedľa Windows.

### Výhody
- Najvyšší výkon
- Plnohodnotný Linux systém
- Možnosť testovania bez inštalácie

### Nevýhody
- Nutnosť reštartovania
- Zložitejšia inštalácia
- Riziko pri práci s diskami

### Počet krokov
10–20+

### Postup inštalácie
1. Stiahnuť Linux ISO
2. Stiahnuť nástroj Rufus
3. Vytvoriť bootovateľné USB
4. Reštartovať počítač
5. Spustiť boot menu
6. Vybrať USB zariadenie
7. Zvoliť "Try" alebo "Install Linux"

### Hardvérové požiadavky
- RAM: min. 4 GB
- Disk: 20–30 GB (dual boot)
- USB: min. 8 GB

---

## Porovnanie

| Kritérium            | WSL        | VirtualBox | Boot / Dual Boot |
|----------------------|-----------|------------|------------------|
| Počet krokov         | nízky     | stredný    | vysoký           |
| Výkon                | vysoký    | stredný    | maximálny        |
| Náročnosť            | nízka     | stredná    | vysoká           |
| GUI                  | obmedzené | plné       | plné             |
| Integrácia s Windows | vysoká    | stredná    | žiadna           |

---

## Záver

### Najlepšie celkovo
WSL je najvýhodnejšie riešenie pre väčšinu používateľov:
- najrýchlejšia inštalácia
- najnižšie nároky
- najjednoduchšie používanie

### Najlepšie na učenie
VirtualBox je vhodný na:
- testovanie Linuxu
- učenie GUI prostredia

### Najlepší výkon
Boot USB / Dual Boot:
- maximálny výkon
- najbližšie k reálnemu Linuxu

---

## Odporúčanie

- Začiatočník: WSL
- Študent / experimentovanie: VirtualBox
- Pokročilý používateľ: Dual Boot