# 너비 우선 탐색(Breadth-First Search)
## 1. BFS와 DFS란?
- 대표적인 그래프 탐색 알고리즘
  - 너비 우선 탐색(BFS) : 정점들과 같은 레벨의 노드들(형제 노드)을 먼저 탐색하는 방식
  - 김피 우선 탐색(DFS) : 정점의 자식들을 먼저 탐색하는 방식

## 2. 파이썬으로 그래프를 표현하는 방법
- 파이썬에서 제공하는 딕셔너리와 리스트 자료구조를 활용해서 그래프를 표현할 수 있음

## 3. 알고리즘 구현
1. BFS
   - 자료구조 `큐`를 활용함
   - need_visit 큐와 visited 큐, `두 개의 큐`를 생성한다.
   ```python
   def bfs(graph, start_node):
       visited = list()
       need_visit = list()

       need_visit.append(start_node)

       while need_visit:
           node = need_visit.pop(0)
           if node not in visited:
               visited.append(node)
               need_visit.extend(graph[node])
       return visited
   ```
2. DFS
     - 자료구조 `스택`을 활용함
    ```python
    def dfs(graph, start_node):
        visited, need_visit = list(), list()
        need_visit.append(start_node)

        while need_visit:
            node = need_visit.pop()
            if node not in visited:
                visited.append(node)
                need_visit.extend(graph[node])
        return visited
    ```



## 4.시간 복잡도
- 일반적인 BFS 시간 복잡도
  - 노드 수 : V
  - 간선 수 : E
    - 위 코드에서 while need_visit는 V + E 번 만큼 수행함
  - 시간 복잡도 : O(V + E)
- 일반적인 DFS 시간 복잡도
  - 노드 수 : V
  - 간선 수 : E
    - 위 코드에서 while need_visit는 V + E 번 만큼 수행함
  - 시간 복잡도 : O(V + E)
- BFS, DFS는 pop의 위치 차이라서 복잡도는 똑같다.
