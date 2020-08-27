```python
# Algorithm 
# 1. compares the first two elements, and swaps
# 2. the array might already sorted, but our algorithm does not know if it is completed. 
# The algorithm needs one whole pass without any swap to know it is sorted.
# Bubble Sort

def bubble_sort(n):
    swapped = False
    for i in range(len(n)):
        if i == len(n)-1:            
            if !swapped:
                return n
            else:
                #repeat the same process until not need to swap
                return bubble_sort(n)
        #if value of next index is greater then swap        
        if n[i] > n[i+1]:
            n[i], n[i+1] = n[i+1], n[i]
            swapped = True     
    
el = [50, 20 ,90 ,1 ,6 ,33, 0, -1]
bubble_sort(el)
```




    [-1, 0, 1, 6, 20, 33, 50, 90]




```python

```
