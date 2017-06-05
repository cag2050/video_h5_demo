# video_h5_demo

* video标签在各手机浏览器的兼容性：

浏览器  | 暂停时视频中间是否有继续播放图标 | 是否能在页面加浮层
----|------|----
chrome | 有 | 能
firefox | 没有  | 能
qq浏览器 | 有  | 不能
360浏览器 | 有  | 能
UC浏览器 | 有  | 不能
safari        | 没有 | 能

* 一般做法：
1. 不要自己加暂停时视频中间的继续播放按钮，要使用浏览器默认的。
2. 暂停时，页面显示浮层，使用pause事件添加。

* 播放控制按钮的显示和隐藏：  
css：controls="controls"  
js: document.getElementById('video1').controls = true 或 false  

* 问题：在iframe中不能全屏播放视频  
解决：将iframe修改成  
```
<iframe … allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true">
```  

* 重要：
h5的video标签，修改source的src地址，必须采用动态插入source元素的形式，否则浏览器不会重新请求播放资源。
jquery 代码例子：

```
var sourceDom = $("<source type='video/mp4' src='xxx.mp4'>");

$("#h5video").append(sourceDom);
```


