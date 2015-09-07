# browser test
window.navigator.appName 浏览器名称 不准确<br/>
window.navigator.userAgent 用户代理字符串 表示浏览器信息<br/>
window.navigator.platform 用户所在系统win32 mac unix<br/>

浏览器嗅探器（精确）<br/>
BrowserDetect.browser  浏览器名称<br/>
BrowserDetect.version   浏览器版本<br/>
BrowserDetect.OS          浏览器所在系统<br/>

插件检测<br/>
navigator.plugins 是一个数组，存储浏览器已经安装插件的完整列表<br/>
window.navigator.plugins[i].name         插件名<br/>
window.navigator.plugins[i].filename     文件名<br/>
window.navigator.plugins[i].description   描述信息<br/>

检测非IE浏览器是否存在某插件<br/>
``` python
function hasPlugin(name){<br/>
      var name = name.toLowerCase();<br/>
      for(var i=0; i<window.navigator.plugin.length; i++)
      {
            if(window.navigator.plugins[i].name.toLowerCase().indexOf(name) > -1)
            {
                      return true;  
            }
            else
            {
                      return false;}
      }<br/>
}
```
<br/>
客户端检测：<br/>
能力检测<br/>
例如IE浏览器无法window.innerWidth获取宽度返回underfind<br/>
就可判断是否返回underfind然后再使用适合IE的<br/><br/>


用户代理检测<br/>
window.navigator.userAgent  表示浏览器信息字符串<br/><br/>

浏览器的呈现引擎：用于排版网页和解释浏览器的引擎<br/>
IE -- Trident     IE8 体现出来了，之前的未体现<br/>
Firefox -- Gecko<br/>
Opera -- Presto     旧版本根本无法体现呈现引擎<br/>
Chrome -- WebKit  WebKit是KHTML呈现引擎的一个分支，后独立开来<br/>
Safari -- WebKit<br/>
Konqueror -- KHTML<br/>
