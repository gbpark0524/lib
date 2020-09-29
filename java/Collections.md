#Collections
- 나만의 규칙 sort
```java

```
```java
Collections.sort(list, (a, b) -> {
  String as = String.valueOf(a), bs = String.valueOf(b);
  return -Integer.compare(Integer.parseInt(as + bs), Integer.parseInt(bs + as));
 });
```
- 내림차순 sort
```java
Collections.sort(list, Collections.reverseOrder());
```
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
qu.add();
qu.peek();
qu.poll(); //반환 및 제거
qu.remove();
```
