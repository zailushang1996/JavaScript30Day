#demo1
>点击键盘上的按钮，按钮样式改变，发出声音
##关键代码
```js
const audio = document.querySelector(`audio[data-key="${event.keyCode}"]`);
const key = document.querySelector(`div[data-key="${event.keyCode}"]`);
```
```js
keys.forEach(key => key.addEventListener('transitionend', removeTransition));// 添加 transition 事件监听
    window.addEventListener('keydown', playSound);//添加 键盘点击 事件点击监听
```
