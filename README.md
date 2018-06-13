#demo1
>点击键盘上的按钮，按钮样式改变，发出声音
##关键JS代码
```js
const audio = document.querySelector(`audio[data-key="${event.keyCode}"]`);
const key = document.querySelector(`div[data-key="${event.keyCode}"]`);
```
```js
keys.forEach(key => key.addEventListener('transitionend', removeTransition));// 添加 transition 事件监听
    window.addEventListener('keydown', playSound);//添加 键盘点击 事件点击监听
```
#demo2
##关键JS代码
```js
function setDate() {
        const date = new Date();
        const second = date.getSeconds();
        const secondDeg = (90 + (second / 60) * 360);

        const min = date.getMinutes();
        const minDeg = (90 + (min / 60) * 360);

        const hour = date.getHours();
        const hourDeg = (90 + (hour / 12) * 360 + (min / 12 / 60) * 360);// 加入分钟所占的时间，使时针可以缓慢地移动


        secHand.style.transform = `rotate(${ secondDeg}deg)`;
        minHand.style.transform = `rotate(${ minDeg}deg)`;
        hourHand.style.transform = `rotate(${ hourDeg}deg)`;

        console.log(`${hour}:${min}:${second} - ${hourDeg}:${minDeg}:${secondDeg}` );

    }
```
#demo3
##关键JS代码
```js
const inputs = document.querySelectorAll('.controls input');
    function handleUpdate() {
        const suffix = this.dataset.sizing || '';
        document.documentElement.style.setProperty(`--${this.name}`, this.value + suffix);
    }

    inputs.forEach(input => input.addEventListener('change', handleUpdate));
    inputs.forEach(input => input.addEventListener('mousemove', handleUpdate));
```