# vue-learning
这是vue 总结和学习合集
##### v-for的笔记
```html
<li v-for="n in evenNumbers">{{ n }}</li>
```
```javascript
data: {
  numbers: [ 1, 2, 3, 4, 5 ]
},
computed: {
  evenNumbers: function () {
     return this.numbers.filter(function (number) {
      return number % 2 === 0
    })
  }
}
```
可以将计算属性直接渲染在元素上  

##### vue事件处理  
获取事件的对象或者使用dom原生事件something($event)    
```javascript
(event){
    event.target
}
```
vue 对于自定义事件没有转换，触发的事件名必须完全匹配监听的事件。因此使用kekab-case,即my-event    


