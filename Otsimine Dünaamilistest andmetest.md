
# Dünaamiliste andmete hoidmine ja otsimine
 andmestruktuur| find | insert | delete
 :---|---|---|--
 Sorteerimata massiiv | $O(n)$ | $O(1)$ | $O(Find)+O(n)$
 Sorteeritud massiiv | $O(lg(n))$ | $O(n)$ | $O(Find)+O(n)$
 Lingitud list | $O(n)$ | $O(1)$ | $O(Find)+O(1)$
 
 
 ## Staatiline otsing
 - Otsinguruum ei muutu (*on staatiline*)
 - Binaarne otsing sorteeritud andmetest

## Dünaamiline otsing
- Otsinguruum muutub pidevalt
- Elemente lisatakse või kustutatakse töö käigus
- Nt
	- Lendude otsing
	- Lennupiletite reserveerimine
- Binaarne otsing nõuab massiivi järjestatud elementitdega
- Uue elemendi lisamine või kusutamine sorteeritud massiivist on **keeurline** $O(n)$
- [[Binaarne otsing]] ei sobi h'sti dünaamilise otsingu probleemide lahendamiseks
