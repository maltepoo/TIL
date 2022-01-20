# 이진 탐색(Binary Search)

### 일반

```python
def binary_search(arr, target):
    start = 0
    end = len(arr)-1
    while end - start >= 0:
        mid = (end + start) // 2
        if arr[mid] == target:
            return True # target 발견
        elif target < arr[mid]:
            end = mid - 1
        else:
            start = mid + 1
         return False # 발견 못함
```

### 재귀

```python
def binary_search_recursion(arr, target, start, end):
    mid = (start + end)// 2
    if arr[mid] == target:
        return True
    elif target < arr[mid]:
        binary_search_recursion(arr, target, start, mid - 1)
    else:
        binary_search_recursion(arr, target, mid + 1, end)
    return False
```