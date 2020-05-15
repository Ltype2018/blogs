### 移动端页面布局
##### 1px的处理
+ window.devicePixelRatio = 物理像素/css像素,所以因该设置viewport的scale值
+ 
 + 根据html的font-size来决定，要先动态设置html的font-size
 ```javascript
     (function() {
        var deviceWidth = document.documentElement.clientWidth;
        deviceWidth = deviceWidth < 320 ? 320 : deviceWidth > 640 ? 640 : deviceWidth;
        document.documentElement.style.fontSize = deviceWidth / 7.5 + 'px';
    })();
 ```
```javascript
          var viewport = document.querySelector("meta[name=viewport]");
          //下面是根据设备像素设置viewport
          if (window.devicePixelRatio == 1) {
              viewport.setAttribute('content', 'width=device-width,initial-scale=1, maximum-scale=1, minimum-scale=1, user-scalable=no');
          }
          if (window.devicePixelRatio == 2) {
              viewport.setAttribute('content', 'width=device-width,initial-scale=0.5, maximum-scale=0.5, minimum-scale=0.5, user-scalable=no');
          }
          if (window.devicePixelRatio == 3) {
              viewport.setAttribute('content', 'width=device-width,initial-scale=0.3333333333333333, maximum-scale=0.3333333333333333, minimum-scale=0.3333333333333333, user-scalable=no');
          }
          var docEl = document.documentElement;
          var fontsize = 32* (docEl.clientWidth / 750) + 'px'; //rem
```
参考链接：[移动端1px解决方案](https://juejin.im/post/5d19b729f265da1bb2774865#heading-13)   
        [viewport移动端适配](https://juejin.im/post/5bfa99e0e51d4555557d26c6#heading-0)
##### 移动端适配

