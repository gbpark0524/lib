# Arrays 
```java
- import java.util.Arrays;
```
- 오름차순 '배열'을 2진탐색으로 해당index출력
```java
Arrays.binarySearch(arr, 26);
  ```
- 특정 길이만큼 배열 복사 `길이가 더 길경우 기본값으로 채워짐!`
```java
int[] arr2 = Arrays.copyOf(arr1, 3);
  ```
- 범위만큼 배열 복사 : 2부터 4까지
```java
int[] arr2 = Arrays.copyOfRange(arr1, 2, 5);
  ```
- 배열 값 채우기
```java
Arrays.fill(arr, 7);
```
- 배열 정렬(오름차순)
```java
Arrays.sort(arr);
```
-  배열이 같은지 비교
```java
Arrays.equals(arr,arr2);
```
- 자바 배열을 arraylist로 변환   '그냥 aslist는 arrays의 private정적 클래스 이므로 add가 없음'
```java
import java.util.ArrayList;
ArrayList<String> arrayList = new ArrayList<String>(Arrays.asList(arr));
```
- 배열의 특정값 확인
```java
Arrays.asList(arr).contains(targetValue);
```
- 배열의 특정값 삭제
```java
import java.util.ArrayList;
import java.util.Iterator;
ArrayList<String> list = new ArrayList<String>(Arrays.asList("a", "b", "c", "d","a","b"));
Iterator<String> iter = list.iterator();
while (iter.hasNext()) {
  String s = iter.next();
  if (s.equals("a")) {
  iter.remove();
  }
}
```
  
