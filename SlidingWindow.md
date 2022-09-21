## Sliding Window Technique

### Prerequisites:
Size of window for computation is fixed throughout the complete nested loop

### How to use:
1) Find size of required window
2) Compute result of first window (i.e. from start of data structure)
3) Use loop to slide the window by 1, and keep computing the result window by window

Example - Given an array of integers of size ‘n’, Our aim is to calculate the maximum sum of ‘k’ consecutive elements in the array.

Explanation - 
1) We compute the sum of first k elements out of n terms using a linear loop and store the sum in variable window_sum.
2) Then we will graze linearly over the array till it reaches the end and simultaneously keep track of maximum sum.
3) To get the current sum of block of k elements just subtract the first element from the previous block and add the last element of the current block .

```
def maxSum(arr, k):
  n = len(arr)
  
  if n < k:
    print("Invalid")
    return -1
  
  window_sum = sum(arr[:k])
  
  max_sum = window_sum
  
  for i in range(n-k):
    window_sum = window_sum - arr[i] + arr[i + k]
    max_sum = max(window_sum, max_sum)
    
  return max_sum
```
