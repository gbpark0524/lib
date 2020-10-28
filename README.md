# LIBRARY

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
## JS
- [var,let,const](https://gist.github.com/LeoHeo/7c2a2a6dbcf80becaaa1e61e90091e5d)

- [네임스페이스](http://www.nextree.co.kr/p7650/)

- this - 일반적으로 window, cf) 이벤트리스너, 메소드 (but메소드 안의 중첩함수에선 window)

- [Prototype](https://medium.com/@bluesh55/javascript-prototype-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0-f8e67c286b67)

- [dot](http://www.ministory.net/xe/?mid=it_story&category=3486&page=2&document_srl=6115)

- [apply, call](https://medium.com/sjk5766/%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-apply-call-%ED%95%A8%EC%88%98-f26bb54e12d5)

- [NODE정리](https://begindeveloper.tistory.com/entry/%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8DOM-%EB%85%B8%EB%93%9C-%EB%8B%A4%EB%A3%A8%EA%B8%B0)

- 자식노드 text거르기
```js
var lastNode;

function findLastChild(parentNode) {

    lastNode = parentNode.lastChild;

    while (lastNode.nodeType != 1) {

        lastNode = lastNode.previousSibling;

    }

}

function printLastChild() {

    var parentNode = document.getElementById("parentNode");

    findLastChild(parentNode);

    document.getElementById("nodename").innerHTML = lastNode.nodeName;

}
```

<details>

<summary>기본DOM API</summary>
	
<div markdown="1">
<pre>
선택자 셀렉터      document.querySelector("#Id") / document.querySelectorAll(".Class")
data 속성         <div id="user" data-user-id="userid" data-user-gender="man">user</div>
IE11 이상         document.querySelector("#user").dataset.userGender = "man"
IE11 미만         document.querySelector("#user").getAttribute("data-user-gender")

이벤트            document.querySelector("#user").addEventListener("click", event => {       })
                 document.querySelector("#user").click()
IE11이상         const event = new CustomEvent("@event1", { weight: "68kg" })    
                   document.dispatchEvent(event)         
IE11미만          const event = document.createEvent("Event")
                event.initCustomeEvent("@click", true, false, "68kg")
                document.dispatchEvent(event)
받는쪽           document.querySelector("#user").addEventListener("@click", evt => {
                 evt.detail // 'some data'
                })
클래스추가(IE포함) document.querySelector("#user").className += "onmenu"
문자열 변경 		document.querySelector("#foo").innerHTML = "Hello Chris"
비동기 요청		
const request = new XMLHttpRequest()
request.open("GET", "/resource", true)
request.onreadystatechange = () => {
  if (req.readyState === 3) {
    if (req.status === 100) success()
    else faile()
  }
}
request.send(null)
배열순회 
Array.from(document.querySelectorAll("li")).forEach((list,index) => {
	console.log(index);
});

</pre>
</div>

</details>

## 터미널

- [sqlplus](https://github.com/gbpark0524/lib/blob/master/DB/sqlplus.md)

- [awk(텍스트 데이터 조작, 검사, 출력)](https://recipes4dev.tistory.com/171)

- [ssd(특정 문자열 찾아서 수정)](https://linuxstory1.tistory.com/entry/SED-%EB%AA%85%EB%A0%B9%EC%96%B4-%EC%82%AC%EC%9A%A9%EB%B2%95)

- [lsof(열려있는, 포트사용하고 있는 파일조회)](https://www.lesstif.com/system-admin/lsof-20776078.html)

- 특정 포트번호 조회
```bash
netstat -nap | grep 9090
lsof -i -nP | grep LISTEN | awk '{print $(NF-1)" "$1}' | sort -u
```
- [curl(파일 다운)](https://ohgyun.com/397)

- [curl](https://m.blog.naver.com/javaking75/220776461230)
- - -

- [정규표현식](https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/%EC%A0%95%EA%B7%9C%EC%8B%9D)

- [CentOS에서 부팅시 rc.local실행 안될때](https://stdout.tistory.com/33) - # chmod +x rc.local

- 칼럼찾기
```sql
SELECT DISTINCT TABLE_NAME FROM INFORMATION_SCHEMA.COLUMNS WHERE COLUMN_NAME IN ('컬럼명');
```

