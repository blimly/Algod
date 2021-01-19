# Graafid
- naabruslist
	- efektiivsem mälukasutus käredate graafide korral
		- mälu $\Theta(|V| + |E|)$
	- Tipu Kõigi naabrite leidmine on proportsionaalne naabrite arvuga
	- Kahe tipu vahelise serva kontroll on ebaeffektiivne $O(|V|)$
- naabrusmaatriks
	- Võib olla ebaefektiivne hõredate graafide korral
		- mälu $\Theta(|V|^2)$
	- Tipu kõigi naabrite leidmine on proportsionaalne kõigi tippude arvuga
	- Efektiivne kahe tipu vahelise serva kontroll 
- **Tugevalt sidusad komponendid (*Strongly Connected Component*)**
	- Suunatud graaf on tugevalt sidus, kui igast tipust on olemas tee igasse tippu
	- Suunatud graafi tugevalt sidus komponent **SCC** on maksimaalen tippude hulk $C$ nii et iga tippude paari $u,v \in C$ jaoks on olemas tee $u \rightarrow v$ ja $v \rightarrow u$
- **Komponentgraaf**
	- on tipp iga SCC kohta
	- on serv $U \rightarrow V$, kui graafi komponendi $U$ mõnest tipust läheb serv komponendi $V$ mõne tipuni
	- on DAG
- **Transponeeritud graaf** 
	- servade suunad on ümber pööratud
	
## Sügavuti läbimine
*DFS*
keerukus: $O(|V| + |E|)$
- nimetatakse ka tagasivõtmisega (*backtracking*) algoritmiks

## Laiuti läbimine
*BFS*
keerukus: $O(|V| + |E|)$

## Suunata tsükliteta graaf
*Directed Acyclic Graphs - DAGs*
- esitab osalist järjestust
