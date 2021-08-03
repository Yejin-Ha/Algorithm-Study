# 재귀함수
- 메소드 혹은 함수 내부에서 자기자신의 메소드 혹은 함수를 다시 호출하는 함수
<br>
<br>

## 재귀함수 활용
1. 재귀함수를 활용한 완전탐색
    ```python
    def recur(index, value):
        # 재귀함수 종료 구분
        if index == len(data):
            result.add(value)
        # 재귀함수 본문
        else:
            recur(index+1, value+data[index])
            recur(index+1, value)
        
    data = [3, 5, 8]
    result = set()

    recur(0, 0)
    print(result)

    ```
2. 팩토리얼
    ```python
    def factorial(n):
        if n == 1:
            return 1
        else:
            return n * factorial(n-1) 
    ```

3. 피보나치 수열
    ```python
    def fibonacci(n):
        if n == 0 or n == 1:
            return 1
        else:
            return fibonacci(n-1) + fibonacci(n-2)
    ```
<br>
<br>

## 재귀함수 깊이
- python에서 maximum 깊이는 1000이다.
