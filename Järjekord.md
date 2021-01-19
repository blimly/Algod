# Järjekorra tüüpi andmestruktuurid
- Võimaldavad
	- andmeid lisada (teoreetiliselt piiranguta)
	- andmeid eemaldada vastavalt kohale järjekorras
	- kontrollida andmete olemasolu
	- puudub andmetele otsepöörumise võimalus - andmetele ligipääsu järjekord sõltub andmestruktuurist
- **Andmestruktuurid** 
	- Stack - *magasin*
		- LIFO - last in first out
		- `push(x)` - $O(1)$
		- `pop()` - $O(1)$
		- Võimalik implementeerida nii massiivi kui lingitud listi põhisena
	- Queue - *järjekord*
		- FIFO - first in first out
		- `enqueue(x)` - $O(1)$
		- `dequeue()` - $O(1)$
		- `isEmpty()`
	- Priority queue - *prioriteetjärjekord*
		- lineaarne järjekord, kus saab sisestatud andmeid kätte prioriteedi järjekorras
		- Scheduline ülesanded
		- ![[Pasted image 20210110164532.png]]
	- Deque - *kahe otsaga järjekord* (Stack + Queue)

## Dünaamiline massiiv
*ArrayList*
- Tavalise massiivi probleemiks on mälu piirang
	- suurus tuleb määrata enne kasutamist
- Dünammiline massiiv muudab ise mälukasutust sõltuvalt vajadusest
- Säilib kiire otsepöördumine