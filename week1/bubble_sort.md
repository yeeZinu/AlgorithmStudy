# Algorithm Study

## Guidlines

### Title: Bubble_Sort
### Goal: 
<pre>
버블정렬의 정의 및 작동 원리, 어떨 때 사용이 가능한가.
</pre>
### Description: 
<pre>
버블 정렬은 단순하여 이해는 좋으나 성능적 면으로는 좋지않다.
</pre>
### Process: 
<pre>
인접한 두 항복의 값을 일정한 기준을 가지고 반복적으로 교환하여 정렬하는 방식
</pre>
### Codeline: 
기본 형
<pre>
def bubble_sort(arr):
    for i in range(len(arr) - 1, 0, -1):
        for j in range(i):
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
</pre>

+최적화 
<pre>
def bubble_sort(arr):
    for i in range(len(arr) - 1, 0, -1):
        swapped = False
        for j in range(i):
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
                swapped = True
        if not swapped:
            break
</pre>

### 시간 복잡도(Time Complexity):
<pre>
 O(n^2)
</pre>

### 공간 복잡도(Time Complexity): 
<pre>
O(1)
</pre>

### 버블 정렬의 장점: 
<pre>
인접한 두 항복을 비교하는 방식으로 정렬을 하기 때문에 개념이 단순해서 이해와 프로그래밍 하기 편하다.
</pre>
### 버블 정렬의 단점:
<pre>
비교해야할 양이 많아지면 많아질 수록 연산이 오래걸린다는 단점이 있다.
</pre>

### Connclusion: 
<pre>
정렬이라는 개념을 배울때 이해하기는 쉬우나 성능면에서 효과적이지는 않아 실제로 사용이 되지는 않다. 교육에 조금 더 초점이 맞춰진 개념이다.
</pre>