# Dictionary, map, associative array
- Mitu nime, sama idee
	- `Data[key]`
	- Andmeid indekseerib **võti**
	- Sarnane massiivile, aga indeks ei pea olema täisarv
	- Võimaldab
		- insert
		- find
		- delete
	- Vähemolulised operatsioonid
		- itereerimine
		- järjestusega seotud operatsioonid
- Implementatsioon Javas
	- **HashSet**
		- Hoiab võtmete hulka, arvud, stringid
	- **HashMap**
		- Sisuliselt dictionary, associateive array
		- Hoiab (võti, objekt) paare
	- **Objekti *hashcode()***
		- Igal objektil on *hashcode*
		- Kui kahe objekti atribuutide väärtused on samad, siis on *hashcode* sama, kui erinevad, siis on erinev ka *hashcode*
		- Sobib mittevõrdususe kontrolliks
- Keerukus 
	- lihtsamad operatsioonid $O(1)$
	- teised operatsioonid $O(n)$

## Otsepöördustabel
*direct-access table*
- üks dictionary implementatsioon
- tavaline massiiv
- Kasutatav kui
	- võtameteks täisarvud $0...K$
	- saame reserveerida mälu $A[K]$
- Operatsioonid $O(1)$
	- Pöördume elemendi A[key] poole
- Mälukasutus võib olla ebaotstarbekas 
	- enamus massiivist on tühi
	- itereerimine ebaeffektiivne
	
