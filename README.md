# video_h5_demo
h5的video标签使用（各手机浏览器兼容性、加遮盖层等），待补充

video标签在各手机浏览器的兼容性：

浏览器  | 暂停时视频中间是否有继续播放图标 | 是否能在页面加浮层
----|------|----
chrome | 有 | 能
firefox | 没有  | 能
qq浏览器 | 有  | 不能
360浏览器 | 有  | 能
UC浏览器 | 有  | 不能
safari        | 没有 | 能

一般做法：
* 不要自己加暂停时视频中间的继续播放按钮，要使用浏览器默认的。
* 暂停时，页面显示浮层，使用pause事件添加。

播放控制按钮的显示和隐藏：  
css：controls="controls"  
js: document.getElementById('video1').controls = true 或 false  

问题：在iframe中不能全屏播放视频  
解决：将iframe修改成  
```
<iframe … allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true">
```  


