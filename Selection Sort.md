# Selection sort
- Otsi väikseim sorteerimata osast
- Vaheta väikseim esimesega sorteerimata osast
- Võrdluste arv: $O(n^2)$
- Omistuste arv: $O(n)$
- In-place sort

```py
def selection_sort(n, A):
	i, y, smallest = 0, 0, 0
	for i in range(1, n-1):
		smallest = i
		for j in range(i + 1, n):
			if A[j] < A[smallest]:
				smallest = j;
		swap(S[i], S[smallest])
```