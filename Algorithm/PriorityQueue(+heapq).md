# Priority Queue(+heapq)

작성일시: September 24, 2021 1:48 AM
최종 편집일시: September 24, 2021 3:07 AM

## 우선순위 큐란?

- 다른 자료형인 Queue(FIFO)나 Stack(FILO)과 비슷하지만, 모든 원소들이 우선순위를 갖는다는 점에서 다르다. 우선순위가 높은 원소는 낮은 우선순위의 원소보다 먼저 처리된다. 같은 우선순위를 갖는 다면 먼저 들어온 원소가 우선으로 처리된다.
- 우선순위 큐는 힙(heap) 자료형을 통해 구현할 수 있다.
- 두 가지 연산으로 구현된다.
    - push: 한 개의 원소를 우선순위와 함께 추가
    - pop: 가장 높은 우선순위의 원소를 큐에서 제거하고 반환

## Heap이란?

- 완전 이진 트리(Complete Binary Tree). 항상 부모 노드의 값이 자식 노드들의 값보다 크거나(Max Heap), 작아야(Min Heap)한다. 힙은 우선순위 큐를 구현하거나, 힙 정렬을 하는데 사용된다.
- 루트 노드에 있는 값이 최대값 혹은 최소값이다.
- 자식 노드는 직접 연결된 부모 노드와의 크기만 비교하면 된다.
- 형제끼리는 비교하지 않아요 🔥

### Max Heap

![Untitled](Priority%20Queue(+heapq)%20d45d1214fca54a629764b45017bd1f9f/Untitled.png)

### Min Heap

![Untitled](Priority%20Queue(+heapq)%20d45d1214fca54a629764b45017bd1f9f/Untitled%201.png)

## 우선순위 큐의 push

- 오른쪽에 push된다.

![https://i.imgur.com/VeuoJbK.png](https://i.imgur.com/VeuoJbK.png)

## 우선순위

- 우선순위가 가장 높은 값 루트 노드를 삭제한다.

![https://i.imgur.com/6dimHpq.png](https://i.imgur.com/6dimHpq.png)

## Python

### Priority Queue

```python
from queue import PriorityQueue

q = PriorityQueue()
q_m = PriorityQueue(maxsize = 7) 

q.put(1) # push
q.put(3)

q_m.put((1, 'one')) # 우선순위, 값

q.get() # pop
q_m.get()[1] # return 'one'
```

### Heapq

- Min Heap

    ```python
    import heapq

    q = []
    heapq.heappush(q, 1)
    heapq.heappush(q, 3)
    heapq.heappush(q, 2)

    heapq.heappop(q) #1
    heapq.heappop(q) #2
    ```

- Max Heap

    ```python
    import heapq

    q = []
    heapq.heappush(q, -1)
    heapq.heappush(q, -3)
    heapq.heappush(q, -2)

    -heapq.heappop(q) #3
    -heapq.heappop(q) #2
    ```

- Heapify
    - list 자료형을 O(n) 시간에 heap으로 변환시켜준다.

    ```python
    import heapq

    data = [1, 3, 5, 7, 9, 2, 4, 6, 8, 0]
    print(data) # [1, 3, 5, 7, 9, 2, 4, 6, 8, 0]
    heapq.heapify(data)
    print(data) # [0, 1, 2, 6, 3, 5, 4, 7, 8, 9]
    ```

    - 마지막 0이 들어오기 전 리스트 [1, 3, 2, 6, 9, 5, 4, 7, 8]에서 0이 들어오고 3이 자식 노드와 순위 비교를 할 때 둘 중 더 큰 9의 자리를 가져간다.

## 참고

- [https://chanhuiseok.github.io/posts/ds-4/](https://chanhuiseok.github.io/posts/ds-4/)
- [https://velog.io/@mein-figur/Python우선순위-큐-heapq](https://velog.io/@mein-figur/Python%EC%9A%B0%EC%84%A0%EC%88%9C%EC%9C%84-%ED%81%90-heapq)