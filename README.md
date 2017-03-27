# note-about-browser
在开发中遇到的一些兼容问题总结

1、flex布局
- IE10以下的浏览器需要添加-ms-前缀
- Android/IOS/Safari的一些老版本需要添加-webkit-前缀
- 解决办法：自动添加CSS前缀处理器(autoprefixer) 通过在webstorm的External Tools进行设置就行了

2、获取,设置标签的内容
- iE和chrome浏览器支持 **innerText**  
- 火狐浏览器支持 **textContent**

3、在IE中是使用event.x 与 event.y，在其他浏览器是event.pageX ，event.pageY

4、复制到剪贴板问题
-  利用clipboard.js来实现这个效果，但是在安卓6以下的webview没有效果，safari没有问题
-  解决办法，调用安卓自己的接口实现这个功能

5、transform样式在比较老的ios系统上失效的办法
- 添加-webkit-前缀
