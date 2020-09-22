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
