# Binary Search Tree
*BST*
- max 2 järglast
- Vasak alampuu < Tipp < Paremalampuu
![[Pasted image 20210110143533.png]]
- Kõik vasakus alampuus on väiksemad kui X
- Ei pea olema täielik puu
	- Halvimal juhul lingitud list
- Samu elemente võivad esitada erinevad puud
- Otsimine sorteeritud andmetest on $O(lg(n))$
- **korduvate võtemetega**
	- võib olla ka korduvata võtmetega
	- siis paugutame võrdse võtame paremasse alampuusse
	- vasak < tipp <=parem
	- hoiame tipus võtme korduste arvu või võtmetega seotud objektide listi
- **Balanseeruvad otsingupuud**
	- *Lisamise ja kustutamise operatsioonid modifitseerivad puud nii, et tasakaal erinevate harude vahel säiliks - harud on ühesügavad või ei erine palju*
	- Red-Black tree
	- AVL tree
	- B-tree
	- Splay tree
	- Treap
	- AA tree
## Sügavus $h$
- Täielikus binaarses puus sügavusega $h$ on $2^h - 1$ tippu
- Kui $n$ on binaarse puu tippude arv ja $h$ on selle puu sügavus, siis $h \geq \lfloor lg(n) \rfloor$




### [[Kuhi]]
*Heap*
- Vanem > Järglane


## Esitus 
- Lingitud struktuur, mille iga tipp on objekt

```py
class Node:
	key = int
	data = Data()
	left = Node()
	right = Node()
	parent = Node()
```

#### Võtme otsimine 
```py
def tree_search(x: Node, k: int):
	if x = None or k = x.key:
		return x
	if k < x.key:
		return tree_search(x.left, k)
	else:
		return tree_search(x.right, k)
```
Keerukus: $O(h)$
*h - puu kõrgus*

#### Min elemendi leidmine
```py
def tree_min(x):
	while. x.left:
		x = x.left
	return x
```
Minimaalne on kõige vasakpoolsem
Keerukus: $O(h)$

#### Max elemendi leidmine
Minimaalne on kõige parempoolsem
```py
def tree_max(x):
	while. x.right:
		x = x.right
	return x
```
Keerukus: $O(h)$

#### Suuruselt järgmine element
*inorder successor*

```py
def tree_successor(x):
	if x.right:
		return tree_min(x.right)
	y = x.parent
	while y and x == y.right:
		x = y
		y = y.parent
	return y
```

#### Elemendi lisamine puusse
```py
def tree_insert(T, z):
	y = None
	x = T.root
	while x:
		y = x
		if z.key < x.key:
			x = x.left
		else:
			x = x.right
	z.parent = y
	if not y:
		T.root = z
	elif z.key < y.key:
		y.left = z
	else:
		y.right = z
```
Keerukus: $O(h)$

#### Elemendi kustutamine
```py
def tree_delete(T, z):
	# Milline tipp kustutada  z  või  z-st järgmine
	if not z.left or not z.right:
		y = z
	else:
		y = tree_successor(z)
		
	# x on y-i laps
	if y.left:
		x = y.left
	else:
		x = y.right
	
	# y eemaldatakse puust
	if x:
		x.parent = y.parent
	if not y.parent:
		T.root = x
	elif y = y.parent.left:
		y.parent.left = x
	else:
		y.parent.right = x
		
	# Kui z-st järgmine kustutati, siis kuopeeri andmed
	if y != z:
		z.key == copy(y.key)
	return y
```

#### Puu läbimine
```py
def inorder_tree_walk(x):
	if x:
		inorder_tree_walk(x.left)
		print(x.key)
		inorder_tree_walk(x.right)
```