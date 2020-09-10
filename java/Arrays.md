# Arrays 
- import java.util.Arrays;
- 오름차순 '배열'을 2진탐색으로 해당index출력
  Arrays.binarySearch(arr, 26);
- 특정 길이만큼 배열 복사<span class="evidence">길이가 더 길경우 기본값으로 채워짐!</span>  
  int[] arr2 = Arrays.copyOf(arr1, 3);
- 범위만큼 배열 복사 : 2부터 4까지
  int[] arr2 = Arrays.copyOfRange(arr1, 2, 5);
- 자바 배열을 list로 변환  
  List<Integer> list = Arrays.asList(arr);


  
  
