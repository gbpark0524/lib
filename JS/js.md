## JS
- [모듈](https://github.com/gbpark0524/lib/blob/master/JS/modules.md)

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
