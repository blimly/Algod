# Lingitud andmestruktuurid
- Objektid ja struktuurid võimaldavad viidata teisele objektile, mis on tihti sama tüüpi viitama objektiga. Sellist tegevust nimetatakse linkimiseks või viitamiseks
- **Dünammilisus** - objekte saab lihtsalt lisada ja eemaldada
- Lingitud andmestruktuuridena luuakse palju huvitavaid ja vajalikke andmestruktuure
	- lingitud listid
	- mitmesugused puud


## Massiiv
*Array*
Plussid:
- kiire otsepöördumine
Miinused:
- piiratud maht
- aeglane add/delete

## Lingitud list
*Linked list*
Plussid:
- piiramatu maht
- kiire add/delete
Miinused:
- aeglane pöördumine

#### Tavaline lingitud list
```python
class Node:
	item = Data()
	nextnode = Node()
```

#### Topeltlingitud list
```python
class Node:
	item = Data()
	left = Node()
	right = Node()
```

## Dünaamiline massiiv
*ArrayList*
Plussid:
- piiratud maht
muu on samamoodi


---
- [[Otsimine Dünaamilistest andmetest]]
