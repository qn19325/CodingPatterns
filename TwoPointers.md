# Two Pointers Technique

Typically used for searching pairs in a sorted array.

Example - Given a sorted array A (sorted in ascending order), having N integers, find if there exists any pair of elements (A[i], A[j]) such that their sum is equal to X.
```
def isPairSum(A, N, X):
  i, j = 0, N-1
  
  while i < j:
    if A[i] + A[j] == X:
      return True
    elif A[i] + A[j] < X:
      i += 1
    else:
      j -= 1
      
  return 0
```

Could be:
```
while i < j:
while i < len(A)
```
