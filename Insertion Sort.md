# Insertion sort
- Massiivi algus on sorteeritud
- Leia j'rmisele elemendile j]ige koht ja nihuta sorteeritud osa ülejäänud elemente
- Võrdlusete arv $O(n^2)$
- Omistamiste arv $O(n^2)$
- In-place
- Stable


```py
def insertion_sort(A):
	i = 1
	while i < len(A):
		x = A[i]
		j = i - 1
		while j >=0 and A[j] > x:
			A[j + 1] = A[j]
			j -= 1
		A[j + 1] = x
		i += 1
```