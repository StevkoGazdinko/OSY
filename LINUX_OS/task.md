# Linux na Windows – Analýza možností (WSL, VirtualBox, Boot USB)

## Prehľad
Táto analýza porovnáva tri hlavné spôsoby používania Linuxu na Windows:
- WSL (Windows Subsystem for Linux)
- VirtualBox (virtuálny stroj)
- Bootovateľné USB / Dual Boot

Cieľ:
- zistiť najrýchlejšie riešenie
- najjednoduchšie riešenie
- najvýhodnejšie riešenie
- hardvérové požiadavky

---

## 1. WSL (Windows Subsystem for Linux)

### Charakteristika
WSL umožňuje spúšťať Linux priamo vo Windows bez klasickej virtualizácie ako plnohodnotný virtuálny počítač.

### Výhody
- najrýchlejšia a najjednoduchšia inštalácia
- nízke nároky na systém
- veľmi rýchly štart
- výborná integrácia s Windows
- ideálne pre programovanie a CLI nástroje

### Nevýhody
- obmedzené GUI možnosti
- nie je to plnohodnotný desktop Linux

### Počet krokov
3–5

### Postup inštalácie
1. Otvoriť PowerShell ako administrátor
2. Zadať príkaz:
3. Reštartovať počítač
4. Dokončiť nastavenie (napr. Ubuntu)

### Hardvérové požiadavky
- RAM: minimálne 4 GB (odporúčané 8 GB)
- Disk: 5–10 GB
- CPU: 64-bit s podporou virtualizácie

---

## 2. VirtualBox

### Charakteristika
VirtualBox vytvára virtuálny počítač, v ktorom beží celý Linux systém s GUI.

### Výhody
- plnohodnotný Linux desktop
- bezpečné testovanie
- izolované prostredie
- možnosť snapshotov

### Nevýhody
- vyššia spotreba RAM a CPU
- pomalší výkon ako natívny systém
- viac krokov pri inštalácii

### Počet krokov
10–15

### Postup inštalácie
1. Stiahnuť VirtualBox
2. Stiahnuť Linux ISO (napr. Ubuntu alebo Linux Mint)
3. Vytvoriť nový virtuálny stroj
4. Nastaviť RAM (minimálne 4 GB)
5. Vytvoriť virtuálny disk (20–30 GB)
6. Pripojiť ISO a spustiť VM
7. Nainštalovať Linux podľa inštalátora

### Hardvérové požiadavky
- RAM: minimálne 8 GB
- Disk: 20–30 GB
- CPU: 64-bit s virtualizáciou

---

## 3. Boot USB / Dual Boot

### Charakteristika
Linux beží priamo na hardvéri počítača buď z USB alebo ako druhý operačný systém.

### Výhody
- maximálny výkon
- plnohodnotný Linux
- vhodné na dlhodobé používanie

### Nevýhody
- nutnosť reštartu
- zložitejšia inštalácia
- riziko pri práci s diskami

### Počet krokov
10–20+

### Postup inštalácie
1. Stiahnuť ISO Linuxu
2. Stiahnuť Rufus
3. Vytvoriť bootovateľné USB
4. Reštartovať PC
5. Otvoriť boot menu
6. Vybrať USB
7. Spustiť Live alebo inštaláciu

### Hardvérové požiadavky
- RAM: minimálne 4 GB
- Disk: 20–30 GB (pri dual boot)
- USB: minimálne 8 GB

---

## Porovnanie

| Kritérium            | WSL | VirtualBox | Boot / Dual Boot |
|---------------------|-----|------------|------------------|
| Počet krokov        | nízky | stredný | vysoký |
| Rýchlosť            | veľmi vysoká | stredná | najvyššia |
| Náročnosť           | nízka | stredná | vysoká |
| GUI podpora         | obmedzená | plná | plná |
| Integrácia s Windows| vysoká | stredná | žiadna |

---

## 4. Dual Boot

### Charakteristika
Dual Boot znamená, že na jednom počítači sú nainštalované dva operačné systémy (Windows a Linux) a pri štarte si vyberáš, ktorý spustiť.

### Výhody
- plný výkon hardvéru
- plnohodnotný Linux systém
- stabilné dlhodobé riešenie
- vhodné pre každodenné používanie Linuxu

### Nevýhody
- riziko pri rozdeľovaní disku
- nutnosť reštartu pri prepínaní OS
- zložitejšia inštalácia

### Počet krokov
15–25

### Postup inštalácie
1. Zálohovať dáta
2. Stiahnuť Linux ISO
3. Vytvoriť boot USB (napr. Rufus)
4. Spustiť inštaláciu Linuxu
5. Vybrať “Install alongside Windows”
6. Nastaviť partition diskov
7. Nainštalovať GRUB bootloader
8. Reštartovať a vybrať OS

### Hardvérové požiadavky
- RAM: min. 4–8 GB
- Disk: min. 50 GB voľného miesta
- CPU: 64-bit

---

## 5. Gitpod (cloud Linux)

### Charakteristika
Gitpod je cloudové vývojové prostredie, ktoré spúšťa Linux workspace priamo v prehliadači. Nepotrebuje inštaláciu Linuxu na PC.

### Výhody
- funguje v prehliadači
- žiadna inštalácia
- rýchly štart (sekundy)
- ideálne pre programovanie
- funguje aj na slabých PC

### Nevýhody
- potrebuje internet
- obmedzenia výkonu (cloud zdroje)
- závislé od služby

### Počet krokov
1–3

### Postup používania
1. Otvoriť Gitpod stránku
2. Prihlásiť sa (GitHub/GitLab)
3. Otvoriť projekt alebo repo
4. Automaticky sa spustí Linux workspace

### Hardvérové požiadavky
- žiadne špeciálne požiadavky
- iba internet a prehliadač

---

## Porovnanie

| Kritérium            | WSL | VirtualBox | Boot USB | Dual Boot | Gitpod |
|---------------------|-----|------------|----------|------------|--------|
| Počet krokov        | nízky | stredný | stredný | vysoký | veľmi nízky |
| Výkon               | vysoký | stredný | vysoký | najvyšší | závisí od cloudu |
| Náročnosť           | nízka | stredná | stredná | vysoká | veľmi nízka |
| GUI                 | obmedzené | plné | plné | plné | webové |
| Internet potreba    | nie | nie | nie | nie | áno |

---


## Záver

### Najlepšia voľba celkovo
WSL je najvýhodnejšie riešenie pre väčšinu používateľov:
- najrýchlejšia inštalácia
- najnižšie nároky
- jednoduché používanie

### Najlepšie na učenie Linuxu
VirtualBox je vhodný na:
- testovanie Linux desktopu
- bezpečné experimentovanie

### Najlepší výkon
Boot USB / Dual Boot:
- plný výkon hardvéru
- reálny Linux systém

---

## Odporúčanie

- Začiatočník: WSL + Ubuntu
- Učenie GUI: VirtualBox + Linux Mint
- Pokročilý používateľ: Dual Boot