- 선택자 셀렉터 
```js
document.querySelector('#Id')
document.querySelectorAll('.Class') //array가 아님의 주의!
```
- data 선택
```js
document.querySelector("#user").dataset.userGender = "man"  //IE11 이상
document.querySelector("#user").getAttribute("data-user-gender")  //IE11 미만
```
- dom을 배열로 변경
```ja
//IE 에서 Array.from() 을 지원 안한다...
var elementList = document.querySelectorAll('.leftMenu_btn');
        
[].forEach.call(elementList, function(element) {
    element.addEventListener('click', function() {
        //function code
    });
});
```
