# Hash 란?
- 데이터를 다루는 기법 중 하나로 검색과 저장이 아주 유용한 구조
- key와 value 쌍으로 데이터를 저장한다.
- 임의의 길이를 갖는 메시지를 입력받아 고정된 길이의 해시값을 출력하는 함수
<br>
<br>

## Dictionary 삽입
```python
# hash 생성, dict 삽입
hash = dict()
hash[1] = 'apple'
hash['banana'] = 3
hash[(4, 5)] = [1, 2, 3]
hash[10] = dict({1:'a', 2:'b'})

# dictionary 수정
hash[1] = 'melon'

# dict 값 추출
hash.pop(1)         # 'melon'
hash.pop('banana')  # 10
hash.pop((4, 5))    # [1, 2, 3]
hash.pop(10)        # {1:'a', 2:'b'}

# dict 삭제
del hash[1]
del hash['banana']
del hash[(4, 5)]
```
<br>
<br>

#
## hash 불가능 type
- list(배열) []
- set(집합) {}
<br>
<br>

## dict 활용
1. dictionary 루프
    ```python
    hash = dict()
    
    # key 추출
    hash.keys()
    # value 추출
    hash.values()
    # key와 value 추출
    hash.items()
    ```
2. dictionary 정렬
     - sorted() : 언제나 list type을 반환
     ```python
     # 오름차순 정렬
     hash = dict({1:10, 3:12, 5:7, 7:6, 4:5})

     # keys
     sorted(hash.keys(), key=lambda x : x)
     # values
     sorted(hash.values(), key=lambda x : x)
     # keys, values
     sorted(hash.items(), key=lambda x : x)
     # key에 대해 오름차순으로 정렬된다.
     ```
     