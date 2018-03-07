#Heap Sort
--------------------
Heap은 최댓값 및 최솟값을 찾아내는 연산을 빠르게 하기 위해 고안된 완전 이진트리를 기본으로 한 자료구조

Heap Sort에는 1. 구조조건, 2. 순서조건을 만족한다. 

부모 노드의 키 값이 자식 노드의 키 값보다 항상 큰 힙을 '최대 힙'

부모 노드의 키 값이 자식 노드의 키 값보다 항상 작은 힙을 '최소 힙'

## 구조 조건
완전 이진트리를 배열로 구현했을 때의 장점은 인덱스로 '바로' 접근 가능합니다.

![예시1](https://github.com/Taeksu89/Heap-Sort/blob/master/image01.png)

흰색 : 데이터

빨간색 : 인덱스

노드 i의 부모 노드 인덱스 :   i/2, (단, i > 1)

노드 i의 왼쪽 자식 노드 인덱스 : 2 x i

노드 i의 오른쪽 자식 노드 인덱스 : (2 x i) + 1

**만약 입력이 배열이라면 힙의 구조 조건을 따로 만족해줄 필요없이 순서 조건만 만족시켜주면 됩니다.** 


## 순서 조건

1단계 : 주어진 배열을 최대힙/최소힙으로 만든다.

2단계 : delete를 통해 정렬을 한다.

2.1단계 : 맨 마지막 노드와 루트 노드를 교환한다.

2.2단계 : 현재 루트 노드에 대해 다운 힙을 진행한다.


![예시2](https://github.com/Taeksu89/Heap-Sort/blob/master/image02.png)

1단계 과정

![예시3](https://github.com/Taeksu89/Heap-Sort/blob/master/image03.png)

![예시4](https://github.com/Taeksu89/Heap-Sort/blob/master/image04.png)

2.1단계 과정

![예시5](https://github.com/Taeksu89/Heap-Sort/blob/master/image05.png)

2.2단계 과정

![예시6](https://github.com/Taeksu89/Heap-Sort/blob/master/image06.png)

![예시7](https://github.com/Taeksu89/Heap-Sort/blob/master/image07.png)

![예시8](https://github.com/Taeksu89/Heap-Sort/blob/master/image08.png)

이는 하나의 과정을 진행한 것이고, 데이터 정렬이 순차적으로 배열될 때까지 2~2.2단계를 반복하여야 합니다.

**완료**

![예시09](https://github.com/Taeksu89/Heap-Sort/blob/master/image09.png)


##시간 복잡도

최대 힙을 만드는 과정 : n

다운 힙 과정 : 2log(2)2

**즉, 힙 정렬의 시간 복잡도는 2nlog(2)2+n입니다.**
