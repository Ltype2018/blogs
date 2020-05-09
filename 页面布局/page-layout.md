### 页面布局    
##### margin 的使用   
在脱离文档流(absolute,fixed)的定位元素中,则margin百分比值是最近一个有定位设置(relative,absolute,fixed)   
的父级对象进行绝对定位父元素的width 计算的,若对象父级没有设置定位属性(absolute,fixed,relative),则 margin    
百分比值是依据 body的 width 计算的  
参考:[margin详解](https://juejin.im/entry/58c6132f570c3500583b095c)   
##### margin重叠  
 + 触发BFC  
   + 只要元素满足下面任一条件即可触发 BFC 特性：  
 body 根元素(根元素什么情况下才会产生BFC呢？经过测试发现，只有同时给html，body都加上overflow : hidden，才能触发BFC，又或者给body加上display : inline-block，display : table，position : absolute也可以触发BFC)[BFC相关](https://www.cnblogs.com/diantao/p/6025547.html)  
   + 浮动元素：float 除 none 以外的值  
  + 绝对定位元素：position (absolute、fixed)  
 + display 为 inline-block、table-cells、flex  
 + overflow 除了 visible 以外的值 (hidden、auto、scroll)  
- margin 详解  
[相邻的margin](https://juejin.im/entry/56cd377c2e958a69f941f802)  
[BFC详解](https://juejin.im/post/59b73d5bf265da064618731d#heading-12)

##### 高度，height, margin,width
- width margin 如margin-left不影响横向布局  
+ height  
  + 不触发BFC ： margin-top 和父元素融合，影响父元素和外界布局  
  + 触发BFC: 添加overflow:hidden position:absolute,float:left,right 等，不影响父元素和外界布局  
  + margin 只影响父元素的上界，不影响下界
##### float  
- 通过设置父元素overflow:auto来将子元素中的float元素包裹  
- 设置相邻元素overflow:hidden 与邻近float 分开应用于两列布局  




