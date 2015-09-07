browser test

window.navigator.appName 浏览器名称 不准确
window.navigator.userAgent 用户代理字符串 表示浏览器信息
window.navigator.platform 用户所在系统win32 mac unix

浏览器嗅探器（精确）
BrowserDetect.browser  浏览器名称
BrowserDetect.version   浏览器版本
BrowserDetect.OS          浏览器所在系统

插件检测
navigator.plugins 是一个数组，存储浏览器已经安装插件的完整列表
window.navigator.plugins[i].name         插件名
window.navigator.plugins[i].filename     文件名
window.navigator.plugins[i].description   描述信息

检测非IE浏览器是否存在某插件
function hasPlugin(name){
      var name = name.toLowerCase();
      for(var i=0; i<window.navigator.plugin.length; i++)
      {
            if(window.navigator.plugins[i].name.toLowerCase().indexOf(name) > -1)
            {
                      return true;  
            }
            else
            {
                      return false;
            }
      }
}

客户端检测：
1）能力检测
例如IE浏览器无法window.innerWidth获取宽度返回underfind
就可判断是否返回underfind然后再使用适合IE的

2）怪癖检测 不建议
通过bug检测
var box = {
    toString : function(){}
};
for(var o in box){
     alert(o);
}
由于IE的一个BUG，未弹框，可判断IE 

3）用户代理检测
window.navigator.userAgent  表示浏览器信息字符串

浏览器的呈现引擎：用于排版网页和解释浏览器的引擎
IE -- Trident     IE8 体现出来了，之前的未体现
Firefox -- Gecko
Opera -- Presto     旧版本根本无法体现呈现引擎
Chrome -- WebKit  WebKit是KHTML呈现引擎的一个分支，后独立开来
Safari -- WebKit
Konqueror -- KHTML
