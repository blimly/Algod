# Binaarne otsing
- otsimine sorteeritud andmetest
	- võimaldab leida elemendi $O(lg(n))$ keerukusega
	- leida suurima vähima $O(1)$ keerukusega
	- sorteerimine maksab $O(n lg(n))$
- otsimine sorteerimata andmetest
	- järjestikotsing keerukusega $O(n)$
## poolitusmeetod
```python
def binary_search(item, L):
	n = len(list)
	low, high = 1, n
	mid = (low + high) / 2
	while L[mid] != item:
		if L[mid] > x:
			high = mid - 1
		else:
			low = mid + 1
		if low > high:
			return -1
		mid = (low + high) / 2
	return L[mid]
```
- Keerukus $W(n) = \lfloor  lg(n) \rfloor + 1$

## interpoleeriv otsing
- töötab hästi eeldusel, et võtmed on vähima ja suurima võtme vahel jagunenud ühtlaselt
- valib jagamise koha vastavalt otsitavale võtmele
$$mid = low + \left\lfloor \frac{x - S[low]}{S[high] - S[low]} \cdot (high -low) \right\rfloor$$
- halvimal juhul taandub järjestikotsingule
- $A(n) = \Theta(lg(lg(n)))$
- $W(n) = \Theta(n)$

## robustne interpoleeriv otsing
- Määrame minimaalse sammu $gap = \lfloor \sqrt{high - low + 1} \rfloor$
- Jagamise koht $mid = min(high - gap, max(mid, low + gap))$
- $A(n) = \Theta(lg(lg(n)))$
- $W(n) = \Theta(lg(n)^2)$

[[Binaarne Otsingupuu]]