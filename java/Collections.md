#Collections
- 나만의 규칙 sort
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
- 최대, 최소 요소
```java
System.out.println(Collections.max(arr));
System.out.println(Collections.min(arr));
```
- 랜덤섞기
```java
Collections.shuffle(arr);
```
- 이진적색 알고리즘 검색-> index반환 (정렬된 상태의 indexOf)
```java
System.out.println(Collections.binarySearch(arr, 44));
//정확한 값이 없을 경우 사이의 값을 -로 반환(-1,-2,-3,-4...)
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
