# 탐색(검색)
- 많은 데이터 속 원하는 데이터를 찾는 것

## 1. 완전 탐색 Exhaustive Search
- Brute Force(브루트 포스)라고도 불리며 컴퓨터의 빠른 계산 성능을 활용하여 가능한 모든 수를 탐색하는 방법
- 효율성 관점에서는 최악의 방법이다.
- 이 방법을 사용하면 풀리지 않는 문제가 없다는 장점이 있다.


- 구현 방법
    1. 반복문
        ```python
        # x(무수한 데이터)중 n의 위치를 찾는 과정
        for i in range(len(x)):
            if x[i] = n:
                return i
        ```

    2. 재귀함수
        - 동적 계획법, 백트래킹, 탐욕법에서도 재귀함수를 통해 구현함
        ```python
        def solution(x, i, n):
            if x[i] == n:
                return i
            else:
                return solution(x, i+1, n)
        ```
        - 다양하게 활용이 가능하지만 쉽게 무한 loop에 빠질 수 있으니 조심하자
        
## 2. 이분 탐색
-
- left : 맨 처음 index
right : 맨 마지막 index
mid = (left + right) / 2

## 3. 깊이 우선 탐색


## 4. 너비 우선 탐색