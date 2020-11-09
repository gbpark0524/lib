#Stack
- 선언 
```java
Stack stack = new Stack();
//Deque<Integer> st = new ArrayDeque<Integer>();
```
- 메소드
```java
stack.push();
stack.peek();
stack.pop();  //반환 및 제거
stack.empty() == true;
stack.search(6) //위에서 몇번째인지(start = 1)
```
#Queue
- 선언
```java
Deque<Integer> qu = new ArrayDeque<Integer>();
```
- 메소드
```java
// 값이없을시 예외를 던짐
qu.add();
qu.remove();
qu.element();
// 값이없을시 false 반환
qu.offer();
qu.poll(); //반환 및 제거
qu.peek();
```
#Priority Queue
- 선언
```java
//int형 priorityQueue 선언 (오름차순, 내림차순)
PriorityQueue<Integer> priorityQueue = new PriorityQueue<>();
PriorityQueue<Integer> priorityQueue = new PriorityQueue<>(Collections.reverseOrder());
```
- 초기화
```java
priorityQueue.clear();
```
