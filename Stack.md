# 스택(Stack)

1 스택이란
========
  자료구조의 일종으로 push와 pop이라는 두가지의 기본적인 연산으로 구성된다.
  push: 스택의 가장 윗 자리에 데이터를 넣는다.
  pop: 스택의 가장 윗 데이터의 값을 넘겨주고 해당 데이터를 제거한다.
  
2 스택의 특징
=========
  스택은 한 쪽 끝에서만 자료를 넣거나 뺄 수 있는 선형 구조(LIFO - Last in First Out)으로 되어 있다. 제일 먼저 들어간 데이터가 가장 나중에 나오는 특징을 지닌다.
  https://commons.wikimedia.org/wiki/File:Data_stack.svg
  
3 파이썬으로 스택 구현하기
========
내장 자료형 중에 하나인 리스트형이 스택을 표현하는데 사용된다.
```python
def Main():
    stack = []            # stack create
    stack.append(1)  # same PUSH
    stack.append(2)
    stack.append(3)
    stack.append(4)
    print stack

    while stack:
       print "POP >", stack.pop()

Main()
```

위 예시에서 1, 2, 3, 4가 push하고 4, 3, 2, 1 순으로 pop하는 것을 확인할 수 있다.


4. 참고문헌
* 위키백과: https://en.wikipedia.org/wiki/Stack_(abstract_data_type) (2018년 7월 3일 접속)
* 한걸음씩: http://onestep.tistory.com/39 (2018년 7월 3일 접속)
