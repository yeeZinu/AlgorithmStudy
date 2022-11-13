# Insertion sort(삽입 정렬)
## Goal
- Insertion sort에 대해 설명할 수 있습니다.
- Insertion sort 과정에 대해 풀이할 수 있습니다.
- Insertion sort 구현이 가능합니다.
- Insertion sort / Selection sort 차이에 대해 설명이 가능합니다.

## Description
- Selection sort 보다 조금 더 효율적인 알고리즘입니다.
- 최선의 경우 시간복잡도는 O(n)입니다. 따라서 속도가 빠르기 때문에 다른 알고리즘과 병행하는 것이 가능합니다.

## Process
1. 2번째 위치의 값을 `temp` 변수에 저장합니다.
2. `temp` 변수와 이전에 있던 원소들과 값을 비교해 삽입을 수행합니다
3. 2번째 위치의 값을 `temp` 변수에 저장하고, 모든 정렬 수행이 끝날 때까지 반복합니다.

## Codelines
```python
def insertionSort(array):
    for end in range(1, len(array)):
        for i in range(end, 0, -1):
            if array[i - 1] > array[i]:
                array[i - 1], array[i] = array[i], array[i - 1]
```
> 첫 반복문에서 정렬 범위를 n으로 확대해 나아갑니다. 내부 반복문은 이전 값이 이후 값보다 클 경우 `swap`(교대)을 수행하는 방식입니다.


## Time Compexity
1. 최악의 경우(역순으로 정렬되어 있을 경우)
    - $O(n^2)$ 입니다.
    - 평균 시간복잡도도 마찬가지입니다.
2. 최선의 경우
    - $O(n)$ 입니다.
    - 모두 정렬이 되어 있는 경우에도 한번만 비교하므로 $O(n)$ 입니다.

## Space Compexity
- 주어진 배열 안에서 `swap`(교대)을 수행하기 때문에 $O(n)$ 입니다.

## 장점
- 정렬하고자 하는 배열 안에서 `swap`(교대)을 수행하는 방식이라서, 메모리 할당을 추가로 필요로 하지 않습니다.(제자리 정렬)
- 안정적인 정렬(Stable sort) 방식입니다.
- Selection sort, Bubble sort 보다 상대적으로 빠르고 효율적입니다.

## 단점
- 평균 또는 최악의 경우가 $O(n^2)$ 입니다.
- 배열의 길이가 길어질 수록 비효율적인 알고리즘입니다.

## Conclusion
- Insertion sort 수행 방식은 $k+1$ 번째 요소를 배치하는 데 필요한 만큼의 요소만 탐색합니다. 따라서 Selection sort, Bubble sort 보다 효율적으로 수행할 수 있는 알고리즘이라는 것을 알 수 있습니다.