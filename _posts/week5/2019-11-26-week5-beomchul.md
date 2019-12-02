---
published : true
layout : posts
author : Bumcheol Kim
title : "[범철/week5] 트리의 구현과 순회"
---


# 트리의 구현과 순회

- 트리

  - 계층적 관계를 표현하는 자료구조, 특정한 조건을 지키도록 구성한 트리를 이용하면 배열이나 리스트를 사용하는 것 보다 같은 작업도 더 빠르게 할 수 있다.

    

- 트리순회순서

  - Root를 언제 방문할것인지가 다르다. 방향은 항상 Left를 Right보다 먼저 방문한다.
  - 전위순회 : ROOT -> LEFT -> RIGHT
  - 중위순회: LEFT -> ROOT -> RIGHT: -> 노드가 작은값부터 정렬되어있는 경우 , 작은숫자부터 차례로 출력이가능하다
  - 후위순회: LEFT -> RIGHT -> ROOT



- 트리의 구성요소
  - 자료가 저장된 노드들이 간선으로 서로 연결되어 있는 자료구조
  - 연결된 두 노드 중 상위노드를 부모노드,하위 노드를 자식노드
  - 부모 노드가 같은 노드는 형제 노드
  - 트리에서 한 노드는 여러 개의 자식을 가질 수 있어도 부모는 하나만 가질 수 있다



- 트리의 재귀적 속성
  - 트리에서 한 노드와 그의 자손들을 모두 모으면 그들도 하나의 트리가 구현이된다.
  - 재귀적속성으로 인해 트리를 다루는 코드들을 보통 재귀호출을 이용해 구현한다.





## 이진탐색트리 (Binary Search Tree)



- ​	이진탐색트리란 ?
  - 이진탐색과 연결리스트(linked list)를 결합한 자료구조의 일종이다. 
  - 이진탐색의 탐색능력을 유지하면서 자료의 입력과 삭제를 가능하게끔 만들었다
  - 이진탐색트리를 순회할 때는 중위순회방식을 사용한다.(왼쪽서브트리 - 노드 -오른쪽서브트리 순서)![source: imgur.com](https://i.imgur.com/SSusVoP.png)



- 이진탐색트리의 핵심연산
  - 이진탐색트리의 핵심연산은 검색 , 삽입 ,삭제 세가지가있다.
  - 이진탐색트리의 생성, 삭제, 해당 이진탐색트리가 비어있는지 확인,트리순회등의 연산이있다.



### 우선순위 큐와 힙

- 우선순위큐란
  - 들어간 순서에 상관없이 우선순위가 높은 데이터가 먼저 나오게된다.
  - 우선순위는 사용자가 결정해준다.
  - 우선순위는 사용자가 결정해주며 숫자가 될 수도 문자가 될 수도있고,높은숫자가 우선운위가높을수도 낮은숫자가 우선순위가 낮을수도 있는것이다. 또한, 우선순위가 같은 데이터도 존재할 수 있다.



- 우선순위 큐를 구현방법
  - 배열을 기반으로 구현하는방법
  - 연결리스트를 기반으로 구현하는 방법
  - 힙을 이용하는 방법



- 힙이란?

  - 힙은 이진트리이되 완전 이진트리이다.
  - 루트노드로 올라갈수록 저장된 값이 커지는 완전트리를 최대 힙이라하고 , 루트노드로 올라갈수록 저장된 값이 작아지는 완전트리를 최소 힙이라 한다.

  