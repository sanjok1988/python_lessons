```python
# Binary Search
# Algorithm
# 1. select middle emement of data set
# 2. compares it against a target value
# 3. if value match it will return success
# 4. if the target value is lower then the value 
#.   it will perform the operation against the lower half
# 5. It will continue with each iteration until the value 
#.   has been found or until it can no longer split the data set.

def binarySearch(n, ar = []):
    if(not ar):
        return "not in the list"
#     ar = sorted(ar)
#     without using inbuild sorted method
    ar = sortList(ar)
    print(ar)
    mid = round(len(ar)/2)
    if(ar[mid] == n):
        return ar[mid]
    else:
        if(n > ar[mid]):            
            ar = ar[mid+1:]
            return binarySearch(n, ar)
        else:
            ar = ar[:mid]         
            return binarySearch(n, ar)
    
# sort list
def sortList(ar):   
    length =len(ar)    
    for x in range(length):        
        for i in range(x,length-1):
            if ar[x] > ar[i+1]:
                ar[x], ar[i+1] = ar[i+1], ar[x]
                
    return(ar)
      
        
ar = [1, 6, 2, 50,3, 96, 9, 8, 25, 30, 2]
binarySearch(6, ar)
```

    [1, 2, 2, 3, 6, 8, 9, 25, 30, 50, 96]
    [1, 2, 2, 3, 6, 8]
    [6, 8]
    [6]





    6


