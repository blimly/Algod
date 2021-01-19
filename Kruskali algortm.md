```py
def kruskal(n, m, E, V):
	i, y = 0, 0
	P, Q = {}, {}
	e = None #edge
	sort(E, key=edgeweight)
	F = None
	for v in V:
		makeSet(v)
	while F.edges < n-1:
		e = next edge (with the least weight) from sorted E
		(i, j) = e
		P = Find(i);
		Q = Find(j);
		if(P != Q):
			Union(P, Q)
			F.add(e)
	return F
```