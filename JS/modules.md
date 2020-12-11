```js
function allDisplayNone(querySelector) {
    var nodes = document.querySelectorAll(querySelector);
    
	Array.prototype.forEach.call(nodes, function(e, i){
		e.style.display = "none";
	});
}
```
```js
function giveTooltipTitle(querySelector) {
    var nodes = document.querySelectorAll(querySelector);
    
	Array.prototype.forEach.call(nodes, function(e, i){
		e.setAttribute('title', e.innerText);
	});
}
```
