```py
def dijkstra(n, W, F):
	i, vnear = 0, 0
	edge = None
	touch = [] # [2...n]
	distance = [] # [2...n]
	
	F = None
	for i in range(2, n):
		touch[i] = 1
		distance[i] = W[1][i]
	for _ in range(n-1):
		min = 10000000000000000
		for i in range(2, n):
			if distance[i] < min and not selected[i]:
				min = distance[i]
				vnear = i
		e = edge(touch[vnear], vnear)
		F.add(e)
		
		for i in range(2, n):
			if distance[vnear] + W[vnear][i] < distance[i]:
				distance[i] = distance[vnear] + W[vnear][i]
				touch[i] = vnear
		selected[vnear] = 1
```