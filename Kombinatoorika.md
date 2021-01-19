# Kombinatoorne optimiseerimine
- Leida parim lahendus lõplikust võimalike lahendusete hulgast, mis võib olla väga suur
	- lühim tee, minimaalne aluspuu
	- parim paigutus, minimaalne materjalikulu
- Lahenduse annab mingi parameetrite kombinatsioon - **konfiguratsioon**
- Igal hulgal suurusega $n$ on $2^n$ alamhulka, $n!$ permutatsiooni
	- sellest tuleneb eksponentsiaalne või suurem keerukus

Konfiguratsioonipuu keerukus
	- üldjuhul $O(k^n)$
	- kui igal tasemel 2 alternatiivi siis $O(2^n)$
	- kui 1. tasemel on $n$ alternatiivi, igal järgneval 1 vähem siis $O(n!)$