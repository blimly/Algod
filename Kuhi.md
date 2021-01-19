# Binaarne kuhi
- Peaaegu täielik kahendpuu
- Sõlmedes on mingi järjestatud hulga elemendid
- Sõlmedes oleva võtme väärtuse on suurem (väiksem) või võrdne sõlme järglaste võtme väärtusest
- **max-heap** - suurim tipus
- **min-heap** - väiksem tipus
- üks prioriteetjärjekorra implementatsioonidest
- Võimaldab leida dünaamilisel andmehulgal maksimaalset (minimaalset) elementi
	- Lisamine $O(log(n))$
	- Maksimaalse elemendi eemaldamine $O(log(n))$
- Esitab osaliselt sorteeritud andmeid
- **Põhiline prioriteetjärjekorra implementatsioon**
- Lisaks binaarkuhjale on olemas ka teisi kuhjasid
	- Binomiaalne
	- Fibonaci


### Enqueue
*elemendi X lisamine kuhja*
- lisatakse seimesele vabale kohale alumises reas
- vajadusel vahetataskse vanematega, kuni kuhja tingiums on täidetud
![[Pasted image 20210110164238.png]]

### Dequeue
*suurima elemendi välja võtmine*
- võetakse tipmine element
- viimane element selle asemele
- - vahetatakse suurema järglasega kuni kuhja tingimus on rahuldatud


## Kuhja massiivesitus
- Eeldusel, et massiivi esimene element (kuhja tipp) on indeksiga 1:
	- parent(i) = i / 2
	- left(i) = 2i
	- right(i) = 2i+1
	- A[Parent(i)] >= A[i]


## Täielik kahendpuu (*binaarpuu*)
![[Pasted image 20210110163900.png]]
- kõigili sisemiste tippudel on 2 järglast
- kõik lehed asuvad tasemel $d$
- kui puu kõrgus on $d$ siis on puus $2^{d-1} - 1$ sisemist tippu
	- $2^{d-1}$ lehte
	- $2^d -1$ tippu kokku
- puu kõrgus, millel on $n$ tippu on $lg(n + 1)$


## Peaaegu täielik kahendpuu
![[Pasted image 20210110163922.png]]
- täielik kahendpuu tasemeni $d-1$
- $d$ taseme lehed on kõik võimalikult vasakul