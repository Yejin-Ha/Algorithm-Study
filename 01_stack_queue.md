# Stack
- 쌓다라는 의미
- 목록 혹은 리스트에서 접근이 한 쪽으로만 가능한 구조
    - LIFO(last-in, first-out) 가 기본 원리
- push, peek, pop

## 직접 구현
```python
class Stack(list):
    push = list.append

    def peek(self):
        return self[-1]

```