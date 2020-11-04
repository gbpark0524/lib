## JAVA
- [Collections](https://github.com/gbpark0524/lib/blob/master/java/Collections.md)

- [Arrays](https://github.com/gbpark0524/lib/blob/master/java/Arrays.md)

- int배열->String배열 : String[] a=Arrays.toString(nums).split("[\\[\\]]")[1].split(", ");	/	import java.util.Arrays;

- [pstmt - bind 변수](https://blog.sting.pe.kr/112)

- JAVA 유니코드 공백제거 - String str =originalString.replaceAll("\\p{Z}", "");  
  trim() - String str =originalString.replaceAll("(^\\p{Z}+|\\p{Z}+$)", "");
  
- [int를 자릿수 배열로 분할](https://zetawiki.com/wiki/%EC%9E%90%EB%B0%94_int%EB%A5%BC_%EC%9E%90%EB%A6%BF%EC%88%98_int_%EB%B0%B0%EC%97%B4%EB%A1%9C_%EB%B6%84%ED%95%A0)

- [JAVA매크로작업](https://okky.kr/article/270141)

- [Enum 활용](https://woowabros.github.io/tools/2017/07/10/java-enum-uses.html)

- 긴 문자열을 붙여야 할 경우 --> StringBuilder가 효과적 
```java
StringBuilder sb = new StringBuilder();
sb.append("ABC");
sb.append("DEF");
```
