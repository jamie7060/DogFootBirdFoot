큐(Queue)
=====

1 특징
======
큐는 추상적 자료형의 일종으로 먼저 집어 넣은 데이터가 먼저 나오는 FIFO(First In First Out) 구조로 저장하는 형식을 말한다.
데이터를 집어넣는 enqueue와 dequeue 연산으로 이루어지는데 이들 연산의 시간 복잡도는 O(1)이다.

2 장점
======
데이터가 입력된 시간 순선대로 처리해야할 필요가 있는 상황에 유리하다.
크기가 제한적이라는 단점이 있는데 이를 해결하기 위하여
선형 큐 → 원형 큐 → 덱 순으로 발전하였다.

3 용도
=====
수강신청 사이트 같이 온 순서대로 처리하는 경우 사용된다.

4 구현
=====
파이썬 리스트 자료형을 활용하여 큐를 구현할 수 있다.
```python
class Queue:
    def __init__(self):
        self.items = []

    def isEmpty(self):
        return self.items == []

    def enqueue(self, item):
        self.items.insert(0,item)

    def dequeue(self):
        return self.items.pop()

    def size(self):
        return len(self.items)
        
    def front(self):
        return self[0]
        
    def back(self):
        return self[-1]
```

출처: http://interactivepython.org/courselib/static/pythonds/BasicDS/ImplementingaQueueinPython.html
다만, 백준 문제에서 요구하는 front와 back을 추가하였다.
