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
- 서로소
```java
Collections.disjoint(mylist1, mylist2); //서로소 이면 true반환
```
- collector 복사
```java
Collections.copy(copiedList, List); //복사 대상의 사이즈가 더 크거나 같아야 함. shallowCopy 이미 다른값이 들어있는 col에 덮을때 사용
copiedList.addAll(List); //모든항 추가

```

