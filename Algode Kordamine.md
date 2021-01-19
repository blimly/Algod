# Algoritmid
## Algoritmide loomise paradigmad
- jaga ja valitse algoritmid 
- ahtned algoritmid 
- **tagasivõtmisega algoritmide**
- [[hargne ja kärbi algoritmid]]
- **metaheuristilised meetodid**
- [[Dünaamiline Planeerimine]]

## Käsitletud algoritmid
- [[Fibonacci arvutamine]] (memoization and recursion)
- [[Binaarne otsing]]
- K-selsect *- vali suurusel k-s element*
- [[Sorteerimine]]
	- [[Selection Sort]]
	- [[Insertion Sort]]
	- [[Heapsort]]
	- Mergesort
	- [[Quicksort]]
	- Mitte võrdlusel põhinevad ==L6 22==
		- [[Counting sort]]
		- [[Radix sort]]
		- [[Bucket sort]]
- Graaf 
	- Minimaalne aluspuu
		- Prim'i algoritm
		- [[Kruskali algortm]]
	- Lühim tee (ahned)
		- Laiuti läbimine - lühim tee kaaludeta graafis
		- [[Dijkstra]]  - lühim tee kaaludega graafis
		- A* - lühim tee punktist punktini
- [[Kombinatoorika]]
	- [[Knapsack]]
# Andmestruktuurid
- listid
- puud
- [[Graafid]]
- [[Dictionary, map, associative array]]
- [[Paisksalvestus]]
- [[Järjekord]]
- [[Konteiner]]

[[Dünaamilised andmed]]
### Millal kasutada
- ArrayList - dünaamiline massiiv
	- Kiire otsepöördus
- LinkedList - lingitud list
	- Kiire lisamine ja kustutamine algusest ja keskelt
	- addFirst, getFirst, removeFirst, addLast, getLast, removeLast, clone
- TreeSet, TreeMap
	- järjestatud ligipääs, min, max - $O(log(n))$
- HashSet, HashMap
	- Kiire pöördumine, insert, remove
	- järjestus pole oluline
- LinkedHashSet, LinkedHashMap
	- Efektiivne itereerimine lisaks eelmisele

# Keerukuse hindamine
## Asümtootiline keerukus
`asymptotic - approacthing a given value as an expression containing a variale trends to infinity`
ehk põhioperatsioonide arvu sõltuvusfunktsioon $K(n)$ sisendite suurusest $n$ 
põhioperatsioon pole üheselt defineeritav
miski mis on riistvaras tehtav piiratud arvu sammudega
- aritmeetika tehe, võrdlus, omistus
- mõnikod valitakse üks pühioperasioon ja loetakse selle arvu näiteks tsüklitingimuse võrdlus
- mõnikord kasutatakse ridade arvu
- **ei sõltu põhioperatsioonide valikust**

$$f(n) \in O(g(n)) \quad f \leq g$$
$$f(n) \in \Omega(g(n)) \quad f \geq g$$
$$f(n) \in \Theta(g(n)) \quad f = g$$
$$f(n) \in o(g(n)) \quad f < g$$
$$f(n) \in \omega(g(n)) \quad f > g$$

[[O notatioon]] eesmärk on lihtsustada analüüsi, jättes ebaolulised detailid arvestamata
![[Pasted image 20210110190646.png]]

#### Rekurentsete lahenduste keerukused
![[Pasted image 20210110190951.png]]