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



  
  
